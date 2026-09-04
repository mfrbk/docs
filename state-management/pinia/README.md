# Pinia 学习系列:读懂 Vue 响应式上的 Store

> 状态管理学习笔记的 Pinia 线:以「读懂一个状态库」的六问为分析轴,读 Pinia 如何把 store 建在 Vue 响应式系统之上。姊妹线见 [Zustand 学习系列](../zustand/README.md);公共坐标系见 [方法论篇](../landscape.md)。· [← docs 索引](../../README.md)

## 阅读路径

| 篇目 | 文章                                    | 一句话重点                                                                                          | 前置                     |
| ---- | --------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------ |
| 前置 | [坐标系与方法论](../landscape.md)       | 四类状态分类 / 五派库谱系 / "读懂一个状态库"的解剖问题单(本系列各章的分析轴)                        | 无                       |
| 一   | [内核:与 Vue 响应式结合](./core.md)     | store 为何是 reactive / getter 为何自动缓存 / createPinia / defineStore / createSetupStore          | 前置                     |
| 二   | [进阶:补丁与订阅体系](./advanced.md)    | $patch / $subscribe(deep watch) / $onAction / 插件注入 / options vs setup 双形态                    | 一                       |
| 延伸 | [对位:双引擎对照与选型](../contrast.md) | 与 Zustand 逐维对照 / 差异根源 = 渲染绑定;选谁由生态决定                                          | 一二(完整对比另读 Zustand 线) |
| 延伸 | [Server State 分水岭](../server-state.md) | 请求数据是"缓存"不是状态;TanStack Query 的 key·stale·GC·乐观更新 / 与 store 协作边界            | 前置                     |

> 官方文档:vuejs.org(响应式原理)、pinia.vuejs.org。默认版本:pinia@^4.0。
