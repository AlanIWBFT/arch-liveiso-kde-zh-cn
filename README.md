# 具有中文 KDE 桌面环境的 Arch Linux Live ISO
## 特点
* 对新手友好的轻量 KDE 桌面环境，可在图形界面下完成联网等基本操作（已默认启用 NetworkManager），并安装有 GParted/KDE 分区管理器方便后续安装
* 作为桌面环境正常运行的基本要求，默认用户为 `liveuser`。可以使用 `sudo` 或者 `su` 来执行权限命令。（也算是其他发行版的标配了）
* 具有中文本地化支持（微调了 CJK 字形防止部分汉字显示为日文字形），并已经将镜像源设置为国内
## 使用方法
直接使用 release 中的 iso 启动
## 本地构建
需求 Arch Linux 或其容器环境
1. 克隆本仓库
2. 安装 `archiso`
3. 在本仓库的上一级目录中运行 `sudo mkarchiso -rv -o . arch-liveiso-kde-zh-cn`
4. 得到名称类似于 `archlinux-2025.11.02-x86_64.iso` 的镜像
## 注意
为了防止在N卡上出现图形界面严重卡顿的现象，本镜像默认带有 `nvidia` 包，可最多支持至40系显卡。如果你使用的是20系图灵架构之后的显卡，可按照 Arch Wiki 将其替换为 `nvidia-open` 来支持更新的显卡
