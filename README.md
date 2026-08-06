# Grouped Interface

基于 [CSM（可通信状态机）](https://nevstop-lab.github.io/CSM-Wiki/) 框架的分组可折叠用户界面的 LabVIEW 模块。

A LabVIEW module for grouped and foldable user interface built on the CSM (Communicable State Machine) framework.

## 功能

- 分组管理程序中的功能按钮
- 折叠及展开各个分组
- 调用各功能按钮的功能

## 模块架构

| 文件 | 说明 |
| --- | --- |
| `Grouped Interface.vi` | 模块主VI |
| `Grouped Interface.lvlib` | 模块组（Library） |
| `Utilities` | 支持组（文件夹） |
| `Pictures` | 图标符号文件夹 |
| `UI Setting.ini` | 界面定义文件 |
| `Grouped Interface.md` | [模块接口文档](./Grouped%20Interface.md) |

## 开发环境

- **LabVIEW 2020** 或更高版本
- **操作系统**：Windows

## 依赖

- [Communicable-State-Machine](https://github.com/NEVSTOP-LAB/Communicable-State-Machine)（必须）
- [CSM-API-String-Arguments-Support](https://github.com/NEVSTOP-LAB/CSM-API-String-Arguments-Support)（必须）

## 快速开始

请参阅 [Grouped Interface.md](./Grouped%20Interface.md) 中的完整接口文档和使用示例。

## 许可

本项目采用 Apache License 2.0 发布。详见 [`LICENSE`](./LICENSE) 和 [`NOTICE`](./NOTICE)。

## 贡献

欢迎贡献！请参阅 [`CONTRIBUTING.md`](./CONTRIBUTING.md) 了解贡献指南。

---

- _CSM Wiki：<https://nevstop-lab.github.io/CSM-Wiki/>_
- _CSM 模块仓库模板：<https://github.com/NEVSTOP-LAB/CSM-Module-Repo-Template>_
