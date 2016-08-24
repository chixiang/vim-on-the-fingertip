# 指尖上的 Vim

## 第一部分 基础

### 初识 Vim

#### 工具控

“控”，来源于英文单词 complex 的前三个字母 [com] 的发音，其中的一个含义是“情节”，也就是这里所说的“控”。我们常说的“某某控”，就是对某种事物有着特殊情结，或者强烈热情的人。比如美食控，就是喜欢美食的人。 我是一个喜欢一切美好事物的人，严格来说有对美好事物有一些洁癖，这类人有一个特点，对细节有着近乎变态的苛刻，追求极致。HIFI领域往往这类人多一些，称为发烧友，我们的世界也许其他人不懂，比如追求一根电源线带来的音质差别，这在旁人眼中也许是不可思议的事情。

毫不掩饰的说，我是一名工具控，对所有工具类的东西有着特别的喜好。

#### Vim 简介

#### 同类编辑器比较

##### Emacs

##### Sublime Text

##### Atom

##### MS Code

> HHKB

### Vim 安装

#### Windows

#### Mac OS

Mac OS 系统自带 Vim，如果你只是在命令行模式下使用 Vim 的话，这一步可以跳过。不过建议你安装第三方的终端软件来使用，比如 iTerm。完善各方面的配置后，比系统自带的终端要好用多了。如果你习惯了 Windows 系统，对命令行模式比较陌生，仍然想使用图形界面的话，Mac OS 下需要安装 MacVim。

![屏幕快照 2016-08-24 21.13.07.png](http://ww1.sinaimg.cn/large/006y8lVagw1f755a5eggrj30ce0600sz.jpg)

首先去官网下载安装介质：[http://macvim-dev.github.io/macvim](http://macvim-dev.github.io/macvim)，选择 “Download Latest Binary Release” 后跳转到下载页面，这里我们只进行简单的安装使用，因此选择 “MacVim.dmg” 下载。

![屏幕快照 2016-08-24 20.58.23.png](http://ww2.sinaimg.cn/large/006y8lVagw1f754v5vf8nj30m4050dg4.jpg)

> 本书在编写时，最新版本是 snapshot-106，基于 Vim patch 7.4.2196

接下来需要安装，双击 dmg 文件挂载后打开，将其中的 MacVim.app 直接拖动到 Application 目录的快捷方式中，安装完成。

![屏幕快照 2016-08-24 21.18.46.png](http://ww1.sinaimg.cn/large/006y8lVagw1f755g11ka8j309503nglq.jpg)

当然，如果你系统自带的 Vim 版本比较老，你想在命令行模式下也使用这个 MacVim 包含的命令行版本，需要将 vi 或者 vim 命令重定义。需要将下面两行添加到用户的配置文件中去，然后重新打开 shell 窗口后生效：

```
alias vi='/Applications/MacVim.app/Contents/MacOS/Vim'
alias vim='/Applications/MacVim.app/Contents/MacOS/Vim'
```

> 注意：使用的 shell 版本不同，用户的配置文件也不同。例如：bash 的默认配置文件是 ~/.bashrc，zsh 的默认配置文件是 ~/.zshrc。
>
> 以上两行需要根据具体情况添加到正确的配置文件中。

到这里，MacVim 窗口模式和命令行模式就安装完成了。

#### Linux/Unix

#### 其它

### Vim 中文帮助文档安装

### Vim 配置文件

### Vim 基本操作

> 场景举例，用一段代码举例，包括常用操作

#### 模式

#### 移动

> 俄罗斯方块

#### 编辑

## 第二部分 进阶

## 第三部分 插件

## 第四部分 IDE

## 第五部分 技巧
