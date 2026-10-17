# 通知权限伪装 · SpoofNotify

从「虚拟权限」插件独立出来的通知权限伪装插件。

使关闭了通知权限的 App 认为已开启通知，不再出现建议开启通知权限的弹窗。App 正常开启通知权限时不会被拦截，通知提醒正常放行。

当前版本：`1.0.0`

## 下载

| 环境 | 文件 | 说明 |
|---|---|---|
| Rootless | [`SpoofNotify_1.0.0_arm64.deb`](downloads/SpoofNotify_1.0.0_arm64.deb) | Dopamine、palera1n 等 rootless 环境 |
| RootHide | [`SpoofNotify_1.0.0_arm64e.deb`](downloads/SpoofNotify_1.0.0_arm64e.deb) | RootHide / roothide 环境 |
| 注入 | [`SpoofNotify.dylib`](downloads/SpoofNotify.dylib) | 巨魔注入或证书自签，arm64 |

也可以从 [官网](https://tongzhi.goforit.si/) 或 [Releases](https://github.com/5hux1n/spoofnotify/releases) 下载。

插件源：<https://apt.mjh.im>（已发布 `1.0.0`，在 Sileo 中添加源后搜索「通知权限伪装」）。

## 兼容

- iOS 15 及以上版本越狱
- rootless
- roothide
- 巨魔注入
- 证书自签

## 使用方法

- **越狱环境**：安装插件后，在桌面找到「通知权限伪装」，打开图标进行配置。
- **巨魔 / 自签环境**：直接把 dylib 注入目标 App 即可生效，默认伪装已开启通知权限，无需配置。

两个 DEB 的二进制均包含 arm64 与 arm64e 切片，文件名对应安装环境。

## 说明

- 只影响 App 读取到的通知权限状态，不修改系统真实通知设置。
- 已经允许的通知仍可能投递；要停止接收，请在系统设置中关闭该 App 的通知。
- 注入版 dylib 为 arm64，不包含设置界面；扩展不会自动生效。
- 不要同时在「虚拟权限」中对同一个 App 开启通知虚拟。

## 反馈

- Telegram：<https://t.me/manjunhong>
- GitHub Issues：<https://github.com/5hux1n/spoofnotify/issues>

## 源码

本仓库只发布安装包与说明，不包含插件源码。
