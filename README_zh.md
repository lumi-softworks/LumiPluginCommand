# LumiPluginCommand

📖 English | [中文版](README_zh.md)

Lumi 及其兄弟应用共用的命令超级插件。

本包导出 `PluginCommand` product 与 module，使既有宿主可继续使用：

```swift
import PluginCommand
```

它提供：

- `CommandManager` —— `CommandProviding` 的默认实现，聚合全应用内由插件注册的
  命令分组；
- `CommandPlugin` —— 内核超级插件，负责安装命令 Provider 与内置 Debug 菜单；
- 本地化的 Debug 菜单项（打开 App Support / Container / Documents / Database
  目录）；
- 在 macOS 上贡献的 DocsView "关于" 页面。

插件标识符默认为 `com.coffic.lumi.plugin.command`。拥有自有命名空间的宿主
可通过传入自定义 bundle ID 保留该标识：

```swift
CommandPlugin(bundleID: "com.coffic.gitok.plugin.command")
```

## 系统要求

- macOS 14+ / iOS 17+
- Swift 6.0

## 安装

```swift
.package(url: "https://github.com/lumi-softworks/LumiPluginCommand.git", from: "1.0.0")
```

## 许可证

GPL-3.0
