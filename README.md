# 指尖上的 Vim

## 第一部分 基础

### 初识 Vim

#### 工具控

“控”，来源于英文单词 `complex` 的前三个字母 `com` 的发音，`complex` 其中的一个含义是“情节”，也就是这里所说的“控”。我们常说的“某某控”，就是对某种事物有着特殊情结，或者强烈热情的人。比如美食控，就是喜欢美食的人。 

#### Vim 简介

#### 同类编辑器比较

##### Emacs

##### Sublime Text

##### Atom

##### MS Code

> HHKB Pro2

### Vim 安装

#### Windows

#### Mac OS

Mac OS 系统自带 Vim，如果你只是在命令行模式下使用 Vim 的话，这一步可以跳过。不过建议你安装第三方的终端软件来使用，比如 iTerm。完善各方面的配置后，比系统自带的终端要好用多了。如果你习惯了 Windows 系统，对命令行模式比较陌生，仍然想使用图形界面的话，Mac OS 下需要安装 MacVim。

![屏幕快照 2016-08-24 21.13.07.png](http://ww1.sinaimg.cn/large/006y8lVagw1f755a5eggrj30ce0600sz.jpg)

首先去官网下载安装介质：[http://macvim-dev.github.io/macvim](http://macvim-dev.github.io/macvim)，选择 “Download Latest Binary Release” 后跳转到下载页面，这里我们只进行简单的安装使用，因此选择 “MacVim.dmg” 下载。

![屏幕快照 2016-08-24 20.58.23.png](http://ww2.sinaimg.cn/large/006y8lVagw1f754v5vf8nj30m4050dg4.jpg)

> 本书在编写时，最新版本是 snapshot-106，基于 Vim patch 7.4.2196

接下来需要安装，双击 dmg 文件挂载后打开，将其中的 `MacVim.app` 直接拖动到 `Applications` 目录的快捷方式中，安装完成。

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

### Vim 基本操作

#### 模式

介绍 Vim 的基本操作，首先要从模式说起。其他常见编辑器，比如 Windows 中的记事本，只有一种“输入模式”，你在键盘上输入的可见字符都会被当作输入的文本内容。而 Vim 是一种多模式编辑器，处于不同的模式下，按下键盘时的响应是不同的。举个例子，在普通模式下，按下键盘上的 `x` 键，你会发现光标处的字符被删除了。而在插入模式下，按下 `x` 键会在编辑器中输入一个字符 `x` ，这就是 Vim 的多模式。

Vim 中一共有 6 种基本模式和 6 种附加模式，不用担心这么多模式太复杂，掌握基本模式就足以成为 Vim 高手了，也不用被“模式”这个名词吓到，使用中在各种模式间切换是非常自然的，你不必刻意的关注。在本书中只为大家介绍 6 种基本模式，下面一起来看一下。

**基本模式：**

- 普通模式（Normal-mode）

  普通模式也叫做命令模式，是 Vim 启动后的默认模式，也是和其他编辑器最大的不同，这时你在键盘上的输入都被当作编辑器命令来触发。

- 可视模式（Visual-mode）

  在可视模式下，会将光标移动的区域高亮选中，键盘触发的编辑器命令只会对选中区域生效。

- 选择模式（Select-mode）

  在选择模式下，键入的字符会替换所有选中的字符，并进入插入模式。

- 插入模式（Insert-mode）

  插入模式和其他编辑器一样，是最常用的编辑模式，你在键盘上输入的可见字符都会被当作内容输入。

- 命令行模式（Command-line-mode）

  顾名思义，你可以在窗口底部输入命令，比如 Ex 命令，查找命令和过滤命令。

- Ex 模式（Ex-mode）

  在普通模式下输入 `gQ` 进入 Ex 模式，执行完一条命令后会继续停留在 Ex 模式。

>  **附加模式：**
>
>  - 操作符等待模式（operator-pending）
>  - 替换模式（replace）
>  - 虚拟替换模式（virtual replace）
>  - 插入普通模式（insert normal）
>  - 插入可视模式（insert visual）
>  - 插入选择模式（insert select）

#### 移动

> 俄罗斯方块

#### 编辑

### Vim 配置文件

### Vim 帮助文档

#### 查看帮助文档

和其他绝大多数软件一样，Vim 自带帮助文档。Vim 的帮助文档非常详细，全面的介绍了 Vim 的使用方式，以至于大部分内容你可能在平时的使用过程中都用不到，或者说无法牢记并活用。这也是就是本书的意义，帮助你更简单更有效的上手 Vim，并逐步提高。要查看帮助，在 Vim 中输入：

```
:help
```

就可以启动帮助文档。如果想直接查看某个命令的用法，比如查看 a 命令，输入：

```
:help a
```

默认情况下，帮助文档是英文版，如果你的英文水平对于读懂这些说明没问题，那么请跳过这一节。如果你想查看中文版本，请跟我继续，下面将带领大家安装中文版的说明文档。

#### 安装中文版帮助文档

#####  Windows

#####  Mac OS

安装之前，首先需要下载帮助文档的中文版本，可以从这里下载：[http://vimcdoc.sourceforge.net](http://vimcdoc.sourceforge.net)

![屏幕快照 2016-08-26 23.21.51.png](http://ww2.sinaimg.cn/large/006y8lVagw1f77k97qd56j30ou06qtax.jpg)

这里我们选择下载压缩包版本，点击上图中的 `tarball` 下载，下载完成后解压：

![屏幕快照 2016-08-26 23.26.34.png](http://ww3.sinaimg.cn/large/006y8lVagw1f77kdw7g2yj30oi0f8429.jpg)

将其中的 `doc` 目录拷贝到用户主目录的 `.vim` 目录下：

```bash
$ cd vimcdoc-1.9.0
$ cp -r doc ~/.vim/
```

拷贝完成之后，再打开 Vim，输入 `:help` 看看，帮助文档是不是已经变成中文了？

> 这里只是安装了中文版本的帮助文档，英文文档并没有被覆盖或者丢失，可以在 Vim 中输入下面的命令来将帮助文档切换回英文：
>
> ```
> :set helplang=en
> ```
>
> 同样，想再切换回中文可以输入：
>
> ```
> :set helplang=cn
> ```

## 第二部分 进阶

## 第三部分 插件

## 第四部分 IDE

## 第五部分 技巧
