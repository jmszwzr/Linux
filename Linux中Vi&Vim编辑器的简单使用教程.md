# Linux中Vi&Vim编辑器的简单使用教程

Vi编辑器是所有Unix及[Linux](https://www.nuo-yan.xin/archives/tag/linux)系统下标准的编辑器，它的强大不逊色于任何最新的文本编辑器，这里只是简单地介绍一下它的用法和一小部分指令。由于对Unix及[Linux](https://www.nuo-yan.xin/archives/tag/linux)系统的任何版本，Vi编辑器是完全相同的，因此您可以在其他任何介绍Vi的地方进一步了解它。Vi也是[Linux](https://www.nuo-yan.xin/archives/tag/linux)中最基本的文本编辑器，学会它后，您将在[Linux](https://www.nuo-yan.xin/archives/tag/linux)的世界里畅行无阻。

Vi与Vim一样都是编辑器，不同的是Vim更高级一些，可以理解是Vi的高级 版本。Vi就像Windows中的计事本，而Vim则可以算的上是 Office中的Word。Vi主要用来编辑一些文件，Vim是程序员的好工具。

虽然Vi是系统自带的，但是一些情况下使用并不习惯，所以我们把它升级成Vim。

### Debian/Ubuntu

```
apt-get install vim
```

### Centos

```
yum install vim
```

然后设置一下：

```
set nocp
# 禁止使用VI兼容模式
set ru
# 显示标尺
set nu
# 显示行号
set sw=2
# 自动缩进2字符(为了和emacs默认的值对应)
set ts=2
# tab宽度2字符(同上)
```

\#号的是注释，不需要输入，一行一行输入，没反应是正常的。

### Vi的基本概念

基本上vi可以分为三种状态，分别是命令模式（command mode）、插入模式（Insert mode）和底行模式（last line mode），各模式的功能区分如下：

1. - 命令行模式（command mode）

控制屏幕光标的移动，字符、字或行的删除，移动复制某区段及进入Insert mode下，或者到 last line mode。

1. - 插入模式（Insert mode）

只有在Insert mode下，才可以做文字输入，按「ESC」键可回到命令行模式。

1. - 底行模式（last line mode）

将文件保存或退出vi，也可以设置编辑环境，如寻找字符串、列出行号……等。

不过一般我们在使用时把vi简化成两个模式，就是将底行模式也算入命令行模式。

首先用vi打开要编辑的文件，命令是`vi 例子.XX`，这时候是命令行模式，这种情况下可以通过各种命令修改文件。

然后按下`"I"键`就切换到了插入模式`（这时候左下角会出现一个-- INSERT --）`，这时候就可以输入文字了，用方向键可以控制光标的移动。

```
注意：这时候如果按下方向键等按键出现字母或者其他情况，那就请执行上面的升级VIM的步骤。还有就是不要用小键盘输入数字和符号！
```

这时候就可以更改文件了，鼠标右键可以粘贴（如果在命令行模式下右键粘贴，就自动切换到了插入模式）。如果要复制的话需要切换到命令行模式然后鼠标选中要复制的文本按下`"Y"键`复制。

如果过程中有输入错误的，也可以按下`"U"键`撤销，多次按键可以多次撤销！

更改完毕之后就按下`"Esc"键`退出插入模式，然后输入`“:wq”`来保存并退出VIM编辑器（`“:w”`是保存但不退出VIM编辑器，`“:q”`退出VIM编辑器但是不保存，`“:q!”`是强制退出VIM编辑器）。

### Vim常用命令示意图

![Linux中Vi&Vim编辑器的简单使用教程](https://www.nuo-yan.xin/wp-content/uploads/2016/08/e7299955038bc4e1.png)



---------

## 资料来源：

https://www.nuo-yan.xin/archives/197.html

