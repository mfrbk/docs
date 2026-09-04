# Zustand 学习系列:读懂「订阅 + 桥」的 Store

> 状态管理学习笔记的 Zustand 线:以「读懂一个状态库」的六问为分析轴,逐篇解剖 Zustand 的 vanilla 内核与 React 渲染绑定。姊妹线见 [Pinia 学习系列](../pinia/README.md);公共坐标系见 [方法论篇](../landscape.md)。· [← docs 索引](../../README.md)

## 阅读路径

| 篇目 | 文章                                | 一句话重点                                                                                        | 前置                     |
| ---- | ----------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------ |
| 前置 | [坐标系与方法论](../landscape.md)   | 四类状态分类 / 五派库谱系 / "读懂一个状态库"的解剖问题单(本系列各章的分析轴)                      | 无                       |
| 一   | [内核:存储与订阅](./core.md)        | createStoreImpl:setState 浅合并 / Set 订阅 / 全量通知,约 20 行的框架无关内核                      | 前置                     |
| 二   | [× React:渲染绑定](./react.md)      | useSyncExternalStore 桥 / selector 引用稳定 / useShallow / 并发下为何不撕裂 / 无需 Provider       | 一                       |
| 三   | [扩展:中间件](./middleware.md)      | 中间件 = 重写 set 与 api:persist / immer / devtools / subscribeWithSelector                       | 一                       |
| 延伸 | [对位:双引擎对照与选型](../contrast.md) | 与 Pinia 逐维对照 / 差异根源 = 渲染绑定;选谁由生态决定                                        | 一二三(完整对比另读 Pinia 线) |
| 延伸 | [Server State 分水岭](../server-state.md) | 请求数据是"缓存"不是状态;TanStack Query 的 key·stale·GC·乐观更新 / 与 store 协作边界      | 前置                     |

> 官方文档:react.dev(useSyncExternalStore)、zustand.docs.pmnd.rs。默认版本:zustand@^5。
