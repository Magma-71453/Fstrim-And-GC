---

Android Fstrim-F2FS GC 自动优化模块



简介（中文）

本模块适用于使用 F2FS 文件系统 的 Android 设备，能够在系统开机或通过定时任务自动执行磁盘 TRIM 优化 与 垃圾回收（GC）操作，维持闪存性能，延长设备寿命。

特性

开机自动执行 Trim

支持 cron 定时执行维护任务

自动判断设备是否为 F2FS 分区，非 F2FS 自动退出

自动挂载 /data 分区为 background_gc=on

BusyBox 支持，Apatch 模块结构

操作结束后自动恢复挂载与 SELinux 状态


注意事项

模块依赖 BusyBox，请确保已安装

仅支持 F2FS 文件系统

非 F2FS 用户请勿启用本模块


Introduction (English)

This module is designed for Android devices using the F2FS (Flash-Friendly File System). It automatically performs disk TRIM and garbage collection (GC) on boot or at scheduled intervals to maintain flash performance and extend device lifespan.

Features

Automatically run trim at startup

Optional cron-based scheduled execution

Automatically detects F2FS filesystem, exits if not detected

Mounts /data with background_gc=on

BusyBox required, Apatch module compatible

Restores SELinux and mount settings after operation


Requirements

BusyBox must be installed

Only supports devices with F2FS on /data

Do not use this module if your device uses EXT4



---

作者 / Authors: Mozixun & Magma
开源协议 / License: GNU Lesser General Public License v3.0

> 本项目基于 LGPL v3 开源协议发布。你可以自由使用、修改并用于商业项目，但必须保留原始作者署名，并在分发衍生作品时采用相同协议。




---
