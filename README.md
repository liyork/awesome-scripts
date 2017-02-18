awesome-scripts [![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)
----
[![GitHub stars](https://img.shields.io/github/stars/superhj1987/useful-scripts.svg?style=social&label=Star&)](https://github.com/superhj1987/useful-scripts/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/superhj1987/useful-scripts.svg?style=social&label=Fork&)](https://github.com/superhj1987/useful-scripts/fork)

本项目fork自<https://github.com/oldratlee/useful-scripts/>，现已经用于公司运维环境中，基于原项目所做更新如下:

- 自安装脚本的修改：[self-installer](self-installer)
- Linux守护进程模板: [tpl/run-cmd-tpl](tpl/run-cmd-tpl)
- 检查当前系统是否运行在虚拟机上: [check-vm](bin/check-vm)
- 改变当前git项目的origin remote的url: [change_git_origin_remote](bin/change_git_origin_remote)
- 增加脚本统一入口：[opscripts](opscripts)

此外，原项目中以下为本人所贡献代码：

- [show-cpu-and-memory](bin/show-cpu-and-memory)
- [monitor-host](bin/monitor-host)

------

## 运行/安装环境

- Linux
- git1.7+

## 安装

三种方法

- `curl -s "https://raw.githubusercontent.com/superhj1987/awesome-scripts/master/self-installer.sh" | bash -s`
- Download the source and `make install`
- Download the source and set `bin` to the System Path to use the common usage shells

## 卸载

opscripts uninstall

## 使用

* `opscripts`
> show system command

* `opscripts list`
> show command list

* `opscripts update`
> update opscripts

* `opscripts uninstall`
> uninstall opscripts 

## 命令列表及文档

### :coffee: [`Java`相关脚本](docs/java.md)

1. [show-busy-java-threads](docs/java.md#beer-show-busy-java-threadssh)  
    用于快速排查`Java`的`CPU`性能问题(`top us`值过高)，自动查出运行的`Java`进程中消耗`CPU`多的线程，并打印出其线程栈，从而确定导致性能问题的方法调用。
1. [show-duplicate-java-classes](docs/java.md#beer-show-duplicate-java-classes)  
    找出`jar`文件和`class`目录中的重复类。用于排查`Java`类冲突问题。
1. [find-in-jars](docs/java.md#beer-find-in-jarssh)  
    在目录下所有`jar`文件里，查找类或资源文件。

### :shell: [`Shell`相关脚本](docs/shell.md)

1. [c](docs/shell.md#beer-c)  
    原样命令行输出，并拷贝标准输出到系统剪贴板，省去`CTRL+C`，`CTRL+V`操作。
1. [colines](docs/shell.md#beer-colines)  
    彩色`cat`出文件行，方便人眼区分不同的行。
1. [a2l](docs/shell.md#beer-a2l)  
    按行彩色输出参数，方便人眼查看。
1. [ap & rp](docs/shell.md#beer-ap-and-rp)  
    批量转换文件路径为绝对路径/相对路径，会自动跟踪链接并规范化路径。
1. [echo-args](docs/shell.md#beer-echo-argssh)    
    输出脚本收到的参数，在控制台运行时，把参数值括起的括号显示成 **红色**，方便人眼查看。用于调试脚本参数输入。
1. [console-text-color-themes](docs/shell.md#beer-console-text-color-themessh)  
    显示`Terminator`的全部文字彩色组合的效果及其打印方式。
1. [tcp-connection-state-counter](docs/shell.md#beer-tcp-connection-state-countersh)   
    统计各个`TCP`连接状态的个数。用于方便排查系统连接负荷问题。
1. [parseOpts](docs/shell.md#beer-parseoptssh)   
    提供命令行选项解析函数`parseOpts`，支持选项的值有多个值（即数组）。
1. [xpl and xpf](docs/shell.md#beer-xpl-and-xpf)    
    在文件浏览器中 打开/选中 指定的文件或文件夹。
1. [show-cpu-and-memory](docs/shell.md#beer-show-cpu-and-memorysh)    
    显示当前cpu和内存使用状况，包括全局和各个进程的。
1. [monitor-host](docs/shell.md#beer-monitor-hostsh)    
    监控当前的内存、cpu、io以及网络状况，写入相应的log文件,建议使用crontab，定时调用此脚本。
1. [tpl/run-cmd-tpl](docs/shell.md#beer-tplrun-cmd-tplsh)    
    linux下后台执行守护程序的模板shell脚本,修改文件中几个选项的值为需要执行的程序即可使用。
1. [check-vm.py](docs/shell.md#beer-check-vmpy)    
    检查当前linux是否是在虚拟机上，包括openvz/xen、pv/uml、VmWare。
1. [get-pip.py](docs/shell.md#beer-get-pippy)    
    安装pip, 将pip程序封装在了文件中，可以避免网络安装pip过慢。

### :watch: [`VCS`相关脚本](docs/vcs.md)

1. [swtrunk](docs/vcs.md#beer-swtrunksh)  
    自动`svn`工作目录从分支（`branches`）切换到主干（`trunk`）。
1. [svn-merge-stop-on-copy](docs/vcs.md#beer-svn-merge-stop-on-copysh)  
    把指定的远程分支从刚新建分支以来的修改合并到本地`svn`目录或是另一个远程分支。
1. [cp-svn-url](docs/vcs.md#beer-cp-svn-urlsh)  
    拷贝当前`svn`目录对应的远程分支到系统的粘贴板，省去`CTRL+C`操作。
1. [change_git_origin_remote](change_git_origin_remote)  
    改变当前git项目的origin remote的url。
