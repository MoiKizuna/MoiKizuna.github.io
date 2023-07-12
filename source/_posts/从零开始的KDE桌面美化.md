---
title: 从零开始的KDE桌面美化
date: 2023-06-28 23:57:28
updated: 2023-07-12 14:11:28
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

ps: 由于未知原因，设置屏幕缩放为125%时，Dolphin不会变成透明



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



## Shell配置

### 终端应用程序

终端就使用 Konsole，我觉得挺好用的w

打开终端，设置->管理配置方案

![常规](Konsole1.png)

![字体，大小](Konsole2.png)

![配色方案，透明度](Konsole3.png)

最后取消显示菜单栏，完成.



### zsh主题和插件配置

#### zsh和oh-my-zsh安装和主题配置

首先安装zsh：

```
sudo apt install zsh
```

然后安装oh-my-zsh，详见[官网](https://ohmyz.sh/#install)，或者输入：

```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

安装后会发现`.zshrc`更新了.

接下来安装zsh的主题，配置一下常用的插件即可。主题推荐使用[powerlevel10k](https://github.com/romkatv/powerlevel10k)，因为我们用的是Oh My Zsh，所以安装方法也用Oh My Zsh对应的方法，引用下项目的README中的安装方法：

> **Oh My Zsh**
>
> ```
> git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
> Copy
> ```
>
> Users in mainland China can use the official mirror on [gitee.com](http://gitee.com/) for faster download.
> 中国大陆用户可以使用 [gitee.com](http://gitee.com/) 上的官方镜像加速下载.
>
> ```
> git clone --depth=1 https://gitee.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
> Copy
> ```
>
> Set ZSH_THEME=“powerlevel10k/powerlevel10k” in ~/.zshrc.

安装完成后打开终端即可进入配置页面.

**注意：**root用户和普通用户的`.zshrc`文件不在一起，需要分开配置：

前者在`/root/.zshrc`, 而后者在`/home/username/.zshrc`下.



#### 配置插件

至于插件，只需要`autojump`, `zsh-autosuggestions`和`zsh-syntax-highlighting`就行，安装方法可以参照另一个博主的[这篇文章](https://www.zrahh.com/archives/167.html).



三个zsh插件功能如下：

- **autojump** 任何位置使用`j xxx`即可跳转到对应的目录，而且不用写全目录名称。前提是这个目录之前访问过，用的时间越久越智能.

  ```
  sudo apt install autojump
  ```

  安装完成后，你需要在 `.zshrc` 文件中添加以下内容来激活它：

  ```
  [[ -s /usr/share/autojump/autojump.zsh ]] && . /usr/share/autojump/autojump.zsh
  ```

  最后`source`一下，配置完成.

  

- **zsh-autosuggestions** 会记住之前的命令输入历史，在输入命令时自动显示出过去输入过的命令，按右方向键`>`即可自动填充.

  在 Ubuntu 22.04 中，你可以通过克隆 `zsh-autosuggestions` 的 GitHub 仓库来安装它. 首先，使用以下命令克隆仓库：

  ```
  git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
  ```

  然后在 `.zshrc` 文件中添加以下内容来激活它：

  ```
  source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
  ```

  最后，重新加载 `.zshrc` 文件或者重新打开终端窗口即可使用 `zsh-autosuggestions`. 当你输入命令时，你会看到一个灰色的补全建议出现在光标后面。你可以通过设置 `ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE` 变量来更改建议的样式.

  

- **zsh-syntax-highlighting** 会给输入的命令高亮，输错了的命令会显示成红色。

  首先，克隆仓库：

  ```
  git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.zsh/zsh-syntax-highlighting
  ```

  在 `.zshrc` 文件中添加以下内容来激活它：

  ```
  source ~/.zsh/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
  ```

  最后，重新加载 `.zshrc` 文件或者重新打开终端窗口即可.

  ![zsh插件预览](zsh.png)

  
  
  
  
  至此配置结束，之后随缘更新~
