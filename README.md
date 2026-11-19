# stardash-releases — 待发布文件（本地已备好，未上传）

Monty 建好公开仓库 https://github.com/xiaoming9988/stardash-releases 后，
把本目录的 3 个文件传上去即可（另需把 1.0.15 APK 一起传到仓库根目录）：

1. `version.json` — 自建更新通道的版本文件。1.0.4 / 1.0.5 / 1.0.6 的代码拉的都是
   `https://raw.githubusercontent.com/xiaoming9988/stardash-releases/main/version.json`，
   比对 versionCode。2026-11-19 已更新到 1.0.15：versionCode 16，apkUrl 指向
   同仓库根目录的 `StarDash-NineWorlds-1.0.15.apk`（59,233,519 字节，56.5 MB，
   sha256 1ad231eb5a8977efdb38de93da56bde4341fcba87d4172597025888cfc39d9b9）。
   传上去后，装着 1.0.14 及以下（versionCode ≤15）的手机点“检查更新”会收到 1.0.15，
   点确认即走完“下载→系统安装器”全程——这就是 Monty 要先落实的自建更新
   端到端验证；装着 1.0.15 的手机点检查会显示“已经是最新版本”（证明通道通了，
   而不是现在的 404 报错）。
   注意：1.0.15 的 APK 是 56.5 MB，超过 GitHub 网页上传的 25 MB 限制，
   不能用浏览器上传按钮传，只能走 git push / API 上传。Monty 把仓库加进
   token 的授权范围后，Muse 可以替他推上去。
2. `StarDash-NineWorlds-1.0.15.apk` — 从
   `~/workspace/stardash/android-release-v115/StarDash-NineWorlds-1.0.15.apk`
   复制过来（本目录未存放 APK 本体，只备好了 version.json）。
3. `privacy_policy_en.html` — 英文隐私政策 v1.1（2026-11-18），
   与中文版 v1.1 逐条对应：只说明了“检查更新”这唯一联网行为，
   其余仍为离线、不收集数据。传上去并在仓库 Settings → Pages
   启用 GitHub Pages 后，Play 商店可用的公开链接就是
   `https://xiaoming9988.github.io/stardash-releases/privacy_policy_en.html`。
   同一个公开仓库同时解决“自建更新”和“隐私政策托管”两个卡点，
   不用再另建一个 stardash-privacy 仓库。

注意：这个仓库只放版本文件、安装包和隐私政策，不放源码、不放密钥，
也不是上架 Play 商店。

小瑕疵（下一版顺手改）：更新弹窗里写的是“下载约 40 MB”，1.0.5 实际是 48.1 MB。
