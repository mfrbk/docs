# 文档索引

> 个人前端知识库:接口与工程规范、构建 / 框架原理学习笔记汇总。每个学习系列自带「总纲」入口,从入口按「前置依赖」逐篇递进。

<!-- TODO: 功能库文档(@mzy1120/http 的 http-request.md / http-orchestrator.md)是否纳入本仓库待定;restful-api.md 内对应引用已标 TODO -->

## 接口与工程规范

| 文档                                                 | 内容                                                                       |
| ---------------------------------------------------- | -------------------------------------------------------------------------- |
| [RESTful API 对接规范](./restful-api.md)             | 资源设计 / 方法语义 / 状态码 / 统一响应信封;`@mzy1120/http` 即按此语义封装 |
| [pnpm Monorepo 使用手册](./monorepo.md)              | pnpm workspace 基本概念 / 常用操作命令 / FAQ                               |
| [Husky + Changesets 工程流程](./husky-changesets.md) | 提交质量检查 + 版本 / CHANGELOG 发布                                       |

## 学习笔记系列

| 系列                                             | 覆盖内容                                                                                                      | 入口                                  |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| [React 原理笔记](./react-hooks-scheduling.md)    | Hooks 链表与闭包机制 / 常用 Hook / 并发调度四阶段                                                              | 单篇                                  |
| [Webpack 学习系列](./webpack/README.md)          | 核心配置 → 性能优化 → 底层原理 → 工程化;专题:HMR、Module Federation                                            | [总纲](./webpack/README.md)           |
| [Vite 学习系列](./vite/README.md)                | 双引擎架构 → 工程化配置 → 插件与 TS → 生态对比                                                                 | [总纲](./vite/README.md)              |
| [Rollup 学习系列](./rollup/README.md)            | 库打包机制 → 配置实战 → 插件与 JS API → 生态对比                                                               | [总纲](./rollup/README.md)            |
| [微前端 qiankun 学习系列](./qiankun/README.md)   | 应用模型 / HTML Entry / JS 沙箱 / 样式隔离 / 通信 / 接入实战 / 选型                                            | [总纲](./qiankun/README.md)           |
| [状态管理学习系列](./state-management/README.md) | 方法论 → Zustand 内核·React·中间件 → Pinia 内核·进阶 → 双引擎对照 → Server State                              | [总纲](./state-management/README.md)  |

> 维护提示:新增文档时在此索引追加一行,并确保文档内 `[← 返回 docs 索引](./README.md)` 回链存在。
