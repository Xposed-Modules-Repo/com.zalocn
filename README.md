# Zalo 汉化（com.zalocn）

> 把 Zalo 界面从**越南语 / 英文**翻译成**简体中文**的 Xposed 模块。

---

## 📌 本仓库是「分发镜像」，请优先访问源码仓库

**源码、Issue、更新日志、最新版本，全部在 👉 [guoxpeng/zalo-cn](https://github.com/guoxpeng/zalo-cn)**

| | 源码仓库（推荐） | 本仓库 |
|---|---|---|
| 地址 | [guoxpeng/zalo-cn](https://github.com/guoxpeng/zalo-cn) | `Xposed-Modules-Repo/com.zalocn` |
| 作用 | 源码、构建脚本、翻译词表、Issue 讨论 | 供 LSPosed / Vector 模块列表收录与下载 |
| 更新 | 由维护者提交 | **跟随源码仓库，同步后版本才会变动** |
| 反馈 | 提 Issue 请到这里 | 仅作分发，不处理 Issue |

> 本仓库不做独立开发。代码和词表都是**从源码仓库同步过来**的，
> 同步动作由维护者手动执行，所以这里的版本号、文件内容可能会比源码仓库**滞后一段时间**。
> 想要最新的翻译修正，请直接去源码仓库的 [Releases](https://github.com/guoxpeng/zalo-cn/releases) 下载。

---

## 功能

- **12000+ 条翻译**，覆盖设置、隐私、聊天、群组、动态、日历、通知、我的文档、钱包等页面
- **越南语 → 保持越南语，英文 → 中文**：自动跟随 Zalo 内建的语言开关，不会把越南语界面也翻成中文
- **服务器下发的文本也能翻**（ZInstant 动态 UI，如安全检查页、小程序分类）
- **纯 UI 翻译**：只替换屏幕显示文字，不改 Zalo 本体、不碰网络请求与账号数据，模块不联网、翻译全在本地离线可用

## 支持版本

- 实测 **Zalo 26.10.01（26.10.1）**，Android 14 真机验证
- hook 的是系统层方法，不依赖具体版本号，26.x 新老版本大概率通用
- 系统要求：**Android 8.1+**，需 Root + **LSPosed / Vector**

## 安装

1. 到本页右侧 **Releases** 下载最新 APK（包名 `com.zalocn`，应用名「Zalo 汉化」）
   —— 或直接去[源码仓库 Releases](https://github.com/guoxpeng/zalo-cn/releases) 拿更新的版本
2. 打开 LSPosed / Vector Manager → 启用模块 → **作用域勾选 Zalo（`com.zing.zalo`）**
   （这步漏了不生效）
3. **强制停止 Zalo 再重开**（模块只在进程新建时注入）

> 两个仓库发的 APK 是**同一个构建、同一个签名**，可以互相覆盖安装，也可以直接覆盖旧版本升级。

## 版本号怎么读

本仓库的 Release 标签格式是 **`<versionCode>-<versionName>`**，例如 `17-2.6.1`：

- 模块管理器靠 `versionCode` 比对，判断要不要提示你更新
- 标签只在维护者同步源码仓库时才新增，所以**这里没新标签 ≠ 项目停更**，
  最新进度请看[源码仓库的提交记录](https://github.com/guoxpeng/zalo-cn/commits/main)

## 常见问题

**装了没效果？**
九成是作用域没勾 Zalo，或改完没强制停止 Zalo。重启手机基本能解决。

**切到越南语后界面还有中文？**
不应出现。模块检测到越南语会整体停止翻译。

**会封号吗？**
风险极低但不是零 —— 模块只改显示文本，不发修改请求、不碰服务器通信。介意就用小号先试几天。

**有页面还是英文？**
去[源码仓库](https://github.com/guoxpeng/zalo-cn/issues)提 Issue，附页面截图，针对性补翻译。

## 已知限制

- 钱包的 Activity（交易记录）、Card（卡）页面是 Zalo 服务器下发的 H5 网页，仍为英文
- 极少数写死在自定义控件里的文本（如聊天列表里的「My Documents」会话名）可能漏翻

## 免责声明

- 仅供个人学习交流，请勿用于商业用途；使用修改版客户端可能违反 Zalo 服务条款，**风险自负**
- 本项目与 Zalo（VNG Corporation）无任何关联
- 作者不对使用本模块造成的任何直接或间接损失负责

## 开源协议

[MIT](LICENSE)

---

**再次提醒：源码、最新版本、问题反馈都在 👉 [guoxpeng/zalo-cn](https://github.com/guoxpeng/zalo-cn)**
