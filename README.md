# scoop-package

## 添加 Bucket

```powershell
scoop bucket add my-bucket https://github.com/altman08/scoop-package
```

## 安装应用

```powershell
scoop install my-bucket/picoclaw
scoop install my-bucket/piliplus
scoop install my-bucket/ncmdump-go
scoop install my-bucket/ncmdump
scoop install my-bucket/watch
scoop install my-bucket/wireguard
scoop install my-bucket/webd
scoop install my-bucket/foobar2000
scoop install my-bucket/yesplaymusic
scoop install my-bucket/utorrent
scoop install my-bucket/chromium-clang-avx
scoop install my-bucket/chromium-clang-avx2
scoop install my-bucket/chromium-clang-avx512
scoop install my-bucket/goutoujunshi-jev-chat
scoop install my-bucket/spartanport
```

## 特定应用说明

### SpartanPort

SpartanPort 用于在 Windows 上运行 PS4 版《战神 III 重制版》。Scoop 会下载并安装 SpartanPort。游戏本体需要从自己的 PS4 导出，包括 `eboot.bin`、`sce_module` 和 `sce_sys`。[上游使用说明](https://github.com/FelipePrado0/SpartanPort/blob/windows-v3.2.1/README.md#download-and-play)

首次启动时，从开始菜单打开 **SpartanPort**。如果已有完整的游戏目录，在 **Game → Game folder → Browse** 中选中含有 `eboot.bin` 的文件夹，点击 **Save**，再点击 **PLAY**。启动器会用本地文件准备游戏镜像。

如果希望由 Scoop 一并管理游戏文件，可将它们放入默认游戏目录，让 `eboot.bin` 直接位于 `game` 下。以下路径均相对于 Scoop 安装根目录。

| 内容 | 默认路径 |
| --- | --- |
| 游戏文件 | `persist\spartanport\source\game` |
| 存档 | `persist\spartanport\source\user\savedata` |
| 启动器配置 | `persist\spartanport\source\settings.json` |

- `scoop uninstall spartanport` 保留持久化目录，重装后可继续使用原有存档和配置。
- `scoop uninstall --purge spartanport` 删除整个 `persist\spartanport` 目录，包括其中的游戏文件和存档。另行选定的外部游戏目录会保留。
