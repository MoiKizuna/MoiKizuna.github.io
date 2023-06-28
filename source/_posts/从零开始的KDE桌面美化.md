---
title: 从零开始的KDE桌面美化
date: 2023-06-28 23:57:28
tags: [linux-themes]
index_img: /img/canva_loli.jpg
---



折腾的东西太多了，怕自己记不住于是简单记录一下ww



# 参考链接

- 一篇比较详细的KDE安装教程：[How to install KDE Plasma on Ubuntu 22.04 Jammy JellyFish](https://linux.how2shout.com/how-to-install-kde-plasma-on-ubuntu-22-04-jammy-jellyfish/ )

- AcherStyx的KDE美化指南：[KDE桌面美化指南 Part1](https://acherstyx.github.io/2020/06/30/KDE%E6%A1%8C%E9%9D%A2%E7%BE%8E%E5%8C%96%E6%8C%87%E5%8D%97/)

  ​                                                [KDE桌面美化指南 Part2](https://acherstyx.github.io/2021/02/20/KDE%E6%A1%8C%E9%9D%A2%E7%BE%8E%E5%8C%96%E6%8C%87%E5%8D%97-2/) 

- IITII的KDE美化指南：[KUbuntu20.04 美化](https://iitii.github.io/2020/08/19/1/ )
- THGLG的KDE美化指南：[KDE美化](https://libhitchhiker.eu.org/solution/eyecandy/eyecandy-kde/#%E6%95%88%E6%9E%9C%E9%A2%84%E8%A7%88)



# 安装KDE

### 1. 更新软件包

```
sudo apt update && sudo apt upgrade
```

### 2. 在 Ubuntu 22.04 LTS 上安装 KDE Plasma

#### Minimal

只会安装 KDE 核心 GUI 软件包以及一些重要的程序.

```
sudo apt install kde-plasma-desktop
```

#### Standard

KDE Plasma GUI 核心包以及一些常见的日常应用程序，例如浏览器、电子邮件客户端、音乐播放器等.

```
sudo apt install kde-standard
```

#### Full

来体验成熟的 KDE Plasma 桌面及其所有应用程序和优点！

```
sudo apt install kde-full
```

### 3. 选择显示管理器

![Select-SSDM-display-manager](/_posts/从零开始的KDE桌面美化/Select-SSDM-display-manager.png)

gdm3是GNOME的显示管理器，kdm或者sddm适用于KDE. 这里选择sddm.

### 4. 重启

```
reboot
```

**注意**：如果使用的是 Ubuntu 22.04，并且重新启动后出现大键盘屏幕，请按**Ctrl+Alt+F5**，然后在终端里登录并创建一个文件：

```
sudo vim /etc/sddm.conf
```

**添加以下两行：**

```
[General]
InputMethod=
```

按**ESC**，按**：**键，然后输入**wq**，**ENTER**退出.

