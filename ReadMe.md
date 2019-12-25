# iGEM 2020 后端学习计划

> 这次的iGEM后端仍然计划延续前几年的习惯，主要使用Python/Django进行开发，并大部分时间在

以下为后端大概率会用到的知识点，这些内容不仅对于我们在后端组开发中有用，对于以后我们对计算机的日常使用和学习也是十分有帮助的

## 文档、搜索引擎、提问

// TODO

## 基础知识

### 了解并熟悉以下的概念

- CPU, 内存(Memory), 文件系统(File System)

- 文件系统权限。了解chmod，chown等命令

- 终端(Terminal)。以及可能的近义词Command Line, Console, Shell

- 命令行参数

- 命令行脚本

- 进程与线程。这两者的区别

- 环境变量

- 网络相关的名词。如TCP/IP Protocol、HTTP Protocol、Socket, URL

- 字符编码。了解ANSI、Unicode、UTF-8的联系与区别

### 可选了解

- 管道(Pipe)

- 异步(Asynchronous)与同步(Synchronous)

- 阻塞(Blocking)与非阻塞(Non-Blocking)

- 并发

- 锁(Locks)、信号量(Semaphore)、临界区(Critical Section)

- 进程间通信(Inter-Process Commucation)

- 协程(Coroutine)。比较其与线程、进程

- 负载均衡(Load Balancing)

- WebSocket Protocol

## Linux

如果没有特殊情况，我们的后端开发以及部署都将在Linux下进行

有几种可选的建议:

- 如果正在使用Windows，可以通过安装WSL(Windows Subsystem for Linux)的方式，以最小的代价运行起一个可用的Linux

- 使用VirtualBox或者VMware Player(Workstation)，以虚拟机的形式运行起Linux。相比起WSL的方法，虚拟机有更好的io性能(如果微软还没有修好的的话)，并且在WSL2之前的WSL1并不能运行Docker

- 在电脑上安装双系统，在每年的春季的LUG Linux 101课程上有学长手把手教学

## Git

Git 是一个版本控制工具可以追踪、记录对⽂件的修改，并且⽅便多⼈协作。一般可以用 Git 管理代码和文档等。iGEM 官方会要求相关队伍将自己的项⽬转移⾄官⽅的 GitHub Organization 中，所以使⽤ Git 是必备的技能

使用Git，你需要知道:

- 各个名词的含义: Working directory, Staging Area, Git Repository, Remote Repository

- Commits, Branches

- 用`.gitignore`忽略指定文件

- 阅读`diff`的输出。

- 使用`clone`, `add`, `rm`, `mv`, `commit`, `push`, `pull`, `status`, `diff`等git简单命令。

- 使用`merge`, `rebase`等命令，懂得如何处理在这些命令中发生冲突时的处理方法。 

在后端开发中，我们将使用GitHub进行代码托管，对于GitHub，你应该知道:

- `clone`, `push`, `pull`, `fetch`来进行与远程仓库的交互

- 提交Pull Requests。(Fork并改动本仓库后，可以向这个仓库发起Pull Requests的测试)

- (可选)发起一个issue

参考教程:

- [https://git-scm.com/book/zh/v2](Pro Git)

- 交互式Git教程[https://learngitbranching.js.org](Learn Git Branching)

- GitHub给出的官方教程[https://guides.github.com/introduction/git-handbook/](Git Handbook)

## Python

// TODO

## Docker(可选)

// TODO

## Database

// TODO

## Task

// TODO
