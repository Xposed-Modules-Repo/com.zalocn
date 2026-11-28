# Zalo中文增强模块（com.zalocn）· 分发镜像

> 本仓库供 LSPosed / Vector 模块列表收录与 APK 下载。**源码、更新日志、问题反馈都在主仓库 [guoxpeng/zalo-cn](https://github.com/guoxpeng/zalo-cn)。**

**当前版本：v3.0.11**

## 这个版本

消息翻译稳定性重构：译文改用 Zalo 原生译文槽，原文/译文独立双行显示；进入任何会话都自动补翻当前可见消息；点消息强制重翻；11 种目标语言全部正确工作；设置面板暗色模式。详见主仓库 [RELEASE_NOTES_v3.0.11.md](https://github.com/guoxpeng/zalo-cn/blob/main/RELEASE_NOTES_v3.0.11.md)。

## 下载

- 正式版：[主仓库 Releases](https://github.com/guoxpeng/zalo-cn/releases)
- 每次源码 push 后，本仓库 Actions 也会自动构建同名 APK 产物（Actions 页面下载）。

## 安装

覆盖安装即可（与主仓库同签名，无需卸载）。装后 LSPosed / Vector 启用模块并勾选 Zalo 作用域，强制停止 Zalo 再重开。

## 自动构建

本仓库 `.github/workflows/build.yml` 与主仓库一致：每次 push 到 main 自动构建签名 APK 并上传产物；签名 secrets 已配置，产物与主仓库签名一致，可直接互相覆盖。

## 协议

MIT。
