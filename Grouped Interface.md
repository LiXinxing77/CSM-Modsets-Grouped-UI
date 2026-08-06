# `Grouped Interface` — CSM 模块接口文档

---

## 功能简述

`Grouped Interface` 是一个 CSM 模块，用于创建可分组折叠的用户导航界面。

---

## 模块信息

| 属性           | 值                                              |
| -------------- | ----------------------------------------------- |
| LabVIEW 版本   | ≥ 2020                                          |
| 支持的操作系统 | Windows                                         |
| 支持 RT        | ❌ 不支持                                       |
| 支持 64-bit    | ✅ 支持                                         |
| 所属模块组     | Grouped Interface.lvlib                              |

---

## 依赖项

| 依赖                                                                                                | 类型 |
| --------------------------------------------------------------------------------------------------- | ---- |
| [Communicable-State-Machine](https://github.com/NEVSTOP-LAB/Communicable-State-Machine)             | 必须 |
| [CSM-API-String-Arguments-Support](https://github.com/NEVSTOP-LAB/CSM-API-String-Arguments-Support) | 必须 |

---

## API 接口（消息接口）

以下是外部调用者可以发送给本模块的消息。

### `API: Register Window`

将窗口名称注册到模块内部窗口列表中。

- **参数**：`APIString` — `String`：窗口名称
- **响应**：N/A

### `API: Unregister Window`

将窗口名称从模块内部窗口列表取消注册。

- **参数**：`APIString` — `String`：窗口名称
- **响应**：N/A

### 参数类型说明

| 类型        | 说明                                                                                              |
| ----------- | ------------------------------------------------------------------------------------------------- |
| `APIString` | 支持嵌套键值对的纯文本字符串，需要 CSM API String Arguments Support 插件                          |

## 调用限制与注意事项

> [!IMPORTANT]
>
> - 本模块为**单例**——同一时间不可运行多个实例。
> - 本模块中的项+分组的名称不允许出现重复，即不允许出现相同的分组名，同一分组中不允许出现相同的项名。
> - 本模块通过 "Action: Launch Function"分支来处理各按钮的操作，各按钮项的行为在这里进行编程。

---

## 使用示例

### 基本生命周期

1. 启动后按照UI Setting.ini文件的配置生成导航界面

2. 关闭窗口时退出程序

---

## 备注

- 本模块生成的界面由UI Setting.ini文件定义。
  - ICON组中的Icon Path项定义了图标文件所在文件夹的相对路径（相对于应用程序文件夹）。
  - ICON组之后的各组名即为导航界面的分组名称，各项名为导航界面组中各项的名称，各项的值则为本项的图标文件名前辍，后辍统一默认为.png。
- 如需修改本模块中各项的图标，可以替换Pitures文件夹下的图片文件，图片大小为16x16，格式为PNG。

---

- _完整 CSM 语法参考：<https://github.com/NEVSTOP-LAB/Communicable-State-Machine/blob/main/.doc/Syntax.md>_
- _CSM Wiki：<https://nevstop-lab.github.io/CSM-Wiki/>_
- _CSM 模块仓库模板：<https://github.com/NEVSTOP-LAB/CSM-Module-Repo-Template>_
