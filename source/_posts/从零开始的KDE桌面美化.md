---
title: 从零开始的KDE桌面美化
date: 2023-06-28 23:57:28
tags: [linux-themes]
index_img: /img/canva_loli.jpg
---



折腾的东西太多了，怕自己记不住于是简单记录一下ww



# 参考链接

- 一篇比较详细的KDE安装教程：[How to install KDE Plasma on Ubuntu 22.04 Jammy JellyFish](https://linux.how2shout.com/how-to-install-kde-plasma-on-ubuntu-22-04-jammy-jellyfish/ )

- AcherStyx的KDE美化指南：

  [KDE桌面美化指南 Part1](https://acherstyx.github.io/2020/06/30/KDE%E6%A1%8C%E9%9D%A2%E7%BE%8E%E5%8C%96%E6%8C%87%E5%8D%97/)

   [KDE桌面美化指南 Part2](https://acherstyx.github.io/2021/02/20/KDE%E6%A1%8C%E9%9D%A2%E7%BE%8E%E5%8C%96%E6%8C%87%E5%8D%97-2/) 

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

![Select-SSDM-display-manager](Select-SDDM-display-manager.png)

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



# 开始配置

## 速通：

- 添加小组件：**Plasma Customization Saver**

![saver](saver.png)

- 下载备份压缩包：[KDE设置备份](https://github.com/MoiKizuna/MoiKizuna.github.io/blob/main/source/_posts/%E4%BB%8E%E9%9B%B6%E5%BC%80%E5%A7%8B%E7%9A%84KDE%E6%A1%8C%E9%9D%A2%E7%BE%8E%E5%8C%96/2023.6.28.tar.gz)
- 在小组件里导入压缩包，完成.



## 配置主题

### 全局主题

使用**WhiteSur-dark**, 同时下载**Sweet-Mars**.

### Plasma视觉风格, 颜色

使用**WhiteSur-dark**.

### 图标

使用**Tela dark**.

### 光标

[Bibata Modern Ice](https://store.kde.org/p/1197198)

安装之后大小改为**40**.

### 字体

[安装Fira Code](https://github.com/tonsky/FiraCode/releases/download/6.2/Fira_Code_v6.2.zip)



## 工作区行为

### 桌面特效

安装窗口管理器特效：**Kinetic Animations**

![桌面特效(1)](桌面特效1.png)

![桌面特效(2)](桌面特效2.png)

![桌面特效(3)](桌面特效3.png)

![桌面特效(4)](桌面特效4.png)



### 输入设备

#### 键盘

延迟 **250** ms, 速度 **40** 重复数/s

#### 鼠标

![鼠标设置](鼠标设置.png)

#### 触摸板

打开 **反向滚动（自然滚动）**



## 配置Kvantum

安装 **Kvantum Manager** ：

```
sudo apt install kvantum qt5-style-kvantum qt5-style-kvantum-l10n qt5-style-kvantum-themes
```

然后安装McMojave主题，从[KDE Store下载](https://store.kde.org/p/1304957)。

将下载下来的`tar.xz`压缩包解压，然后打开Kvantum Manager，选择这一个文件夹，安装主题.

![Kvantum配置](Kvantum配置.png)

然后在 **外观** / **应用程序风格** 里切换成 **Kvantum** , GTK应用程序风格改为**Mojave-Dark-alt**.



## 桌面Dock和插件配置

```
sudo apt install latte-dock
```

安装完成之后 **右键** ， **编辑停靠栏** ，**高级** 

#### 外观

![latte外观配置](latte外观配置.png)

#### 特效

![latte特效配置](latte特效配置.png)

#### 预览

![latte](latte.png)



## 顶栏

![topline](top.png)

面板高度： **38**



