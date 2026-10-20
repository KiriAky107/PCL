# Plain Craft Launcher (PCL) KiriAky 修改版

基于 [Meloong-Git/PCL](https://github.com/Meloong-Git/PCL) 的个人第三方修改版，由 KiriAky107 独立维护和发布。保留 Minecraft 本体下载、实例修改与整合包安装功能。

**[下载本修改版](https://github.com/KiriAky107/PCL/releases/latest)** · [全部发行版](https://github.com/KiriAky107/PCL/releases) · [上游项目](https://github.com/Meloong-Git/PCL)

## 下载与使用

1. 打开本仓库的 [Releases](https://github.com/KiriAky107/PCL/releases/latest)，下载名称以 `PCL-KiriAky-` 开头的 Windows 便携压缩包。
2. 解压到独立文件夹，运行 `Plain Craft Launcher (PCL) KiriAky.exe`。需要 Windows 和 .NET Framework 4.8。
3. 在启动器内选择已有的 Minecraft 文件夹，或通过“下载”安装游戏。

软件包附带使用说明、原项目许可及 SHA256 校验信息，不包含 Minecraft 游戏文件、Java 或个人账号配置。以后更新本修改版，请从本仓库 Releases 下载。

## 本修改版的行为

- 保留 Minecraft 本体下载、实例修改和本地/在线整合包安装入口，`RestrictMcDownload` 固定为 `False`。
- 沿用 Mojang 官方源与 BMCLAPI 镜像源，并保留原有文件校验；具体来源由下载源设置和可用性决定。
- Minecraft 版本列表通过网络获取，后续版本通常会自动出现在列表中。若将来游戏的安装格式或启动方式改变，可能需要适配新版启动器。
- 新配置默认关闭启动器更新提示，继续保留开源版原有的空更新与联网公告实现，不会自动用官方 PCL 程序覆盖自身。
- 当前没有本 fork 的自动升级器，升级通过 Releases 手动完成。手动覆盖程序或同步上游源码时，需要保留本 fork 的修改。

## 开源构建的功能说明

本发行包从开源代码构建。微软正版登录需要自己的 `PCL_MS_CLIENT_ID`（微软应用客户端 ID），CurseForge 访问需要自己的 `PCL_CURSEFORGE_API_KEY`。可通过同名环境变量提供，或在自行构建时配置。未配置凭据时，对应服务不可用。

其他功能沿用上游开源版；主题切换、部分联机及百宝箱等功能受开源实现范围限制。游戏版本列表的更新和启动器自身的更新相互独立。

## 自行构建

使用仓库 [Build 工作流](https://github.com/KiriAky107/PCL/actions/workflows/build.yml)，从运行结果的 Artifacts 获取 Debug 或 Release 产物。首次独立发行使用已通过 Debug / Release 构建及下载入口检查的 Release 产物。

源码包含 `MeloongCore` 子模块，本地克隆时使用：

```powershell
git clone --recurse-submodules https://github.com/KiriAky107/PCL.git
```

## 原作者与许可

PCL 原作者为 **龙腾猫跃**，协力开发者为 HerobrineXia。感谢原作者和社区贡献者；[赞助原作者](https://meloong.com/afd/a/LTCat)。本修改版保留原项目署名、关于页面及正版购买与赞助劝导。

源码与分发约定见 [LICENCE](LICENCE)，其中包含《PCL 分发有限许可》的引用及《PCL 存储库合理使用指南》。本项目继续公开修改后的源码，发行包附带该许可文件。

相关资源：[上游帮助文档库](https://github.com/LTCatt/PCL2Help) · [上游功能投票](https://github.com/Meloong-Git/PCL/discussions/2)。
