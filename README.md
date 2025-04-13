# Android Fstrim-F2FS GC 自动优化模块

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC--BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

## 简介（中文）

本模块适用于使用 **F2FS 文件系统** 的 Android 设备，能够在系统开机或通过定时任务自动执行磁盘 **TRIM 优化** 与 **垃圾回收（GC）操作**，维持闪存性能，延长设备寿命。

### 特性

- 开机自动执行 F2FS 垃圾回收（GC）
- 支持 cron 定时执行维护任务
- 自动判断设备是否为 F2FS 分区，非 F2FS 自动退出
- 自动挂载 `/data` 分区为 `background_gc=on`
- BusyBox 支持，Apatch 模块结构
- 操作结束后自动恢复挂载与 SELinux 状态

### 注意事项

- 模块依赖 BusyBox，请确保已安装
- 仅支持 **F2FS 文件系统**
- 非 F2FS 用户请勿启用本模块

## Introduction (English)

This module is designed for Android devices using the **F2FS (Flash-Friendly File System)**. It automatically performs **disk TRIM** and **garbage collection (GC)** on boot or at scheduled intervals to maintain flash performance and extend device lifespan.

### Features

- Auto-run F2FS garbage collection on boot
- Optional cron-based scheduled execution
- Automatically detects F2FS filesystem, exits if not detected
- Mounts `/data` with `background_gc=on`
- BusyBox required, Apatch module compatible
- Restores SELinux and mount settings after operation

### Requirements

- BusyBox must be installed
- Only supports devices with **F2FS** on `/data`
- Do **not** use this module if your device uses EXT4

---

**作者 / Authors:** Mozixun & Magma  
**开源协议 / License:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

> 你可以自由分享与修改本项目，但不得用于商业用途，且必须署名原作者，并在相同许可证下开源再发布。
