# iGEM 2020 后端学习计划

**基于2018及2019后端学习任务修改，原作者hsfzxjy及taoky**

> 这次的iGEM后端仍然计划延续前几年的习惯，主要使用Python/Django进行开发，并大部分时间在Linux下进行。

以下为后端大概率会用到的知识点，这些内容不仅对于我们在后端组开发中有用，对于以后我们对计算机的日常使用和学习也是十分有帮助的

## 文档、搜索引擎、提问

没有人可以刚开始就胜任前后端的开发工作，从网络上找到合适的学习资料是一个十分重要的技能。

### 文档

⼀⻔优秀的技术通常会附有同样优秀的⽂档。⽂档包括官⽅教程（Get started）、示例（Example）以及 API 列表等。

文档通常只有英文，少部分有由社区推动的中文翻译。但相对而言，中文文档的时效性落后于英文文档，因此英文文档是第一选择。

本文后面提到的大多数技术都附有官方文档。

### 搜索引擎

搜索引擎可以快速帮助你找到问题的解决方案，也可以帮助你定位相关技术在其对应文档中的位置。

在大部分常见的技术上，你所遇到的问题一般已经有人遇到过了，在网络上常常可以找到相应的解决方案。

在搜索时，请注意：

- 首先确定并非是低级错误，如typo、语法错误等。

- 尽量不要使用完整的自然语句，而是使用关键字。如“xxx错误”是一个比“为什么发生xxx错误”更好的搜索内容。

- 如果使用中文无法找到，可以翻译为英文再尝试。

> 避免用中文搜索还可以避开许多SEO（Search Engine Optimization）的站点，如代码日志（codeday.me）这些仅仅使用机器翻译Stackoverflow的回答，并且翻译质量极差，还不给出原链接的网站。

- 有条件尽量使用Google，必应国际版使用英文搜索亦可。尽量避免用百度搜索计算机相关的知识。

- 善用搜索引擎的语法。如在搜索内容后加上“site:stackoverflow.com”可以限制搜索的网站为Stackoverflow。

### 提问

如果在网络上并没有找到合适的解答，可以向Stackoverflow这样的问答类网站提出自己的问题。

在提出问题前，建议通读一遍《提问的智慧》([中](https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way/blob/master/README-zh_CN.md))([英](http://www.catb.org/~esr/faqs/smart-questions.html))，让你的提问更明确，节省大家的时间。

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
- 服务端（Server）、客户端（Client）

### 可选了解

- Markdown。我们将使用Markdown来编写后端文档。Ref: [Markdown-Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- 正则表达式(Regular Expression)
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
- 如果正在使用Windows，可以通过安装WSL（Windows Subsystem for Linux）的方式，以最小的代价运行起一个可用的Linux
- 使用VirtualBox或者VMware Player（Workstation），以虚拟机的形式运行起Linux。相比起WSL的方法，虚拟机有更好的io性能(如果微软还没有修好的的话)，并且在WSL2之前的WSL1并不能运行Docker
- 在电脑上安装双系统，在每年的春季的LUG Linux 101课程上有学长手把手教学

> 使用前两种方法的，可以在vscode中安装vscode-remote插件，或者设置PyCharm的Remote Python Interpreter来将环境运行在Linux上，代码界面运行在Windows上。

## Git

Git 是一个版本控制工具可以追踪、记录对⽂件的修改，并且⽅便多⼈协作。一般可以用 Git 管理代码和文档等。iGEM 官方会要求相关队伍将自己的项⽬转移⾄官⽅的 GitHub Organization 中，所以使⽤ Git 是必备的技能

使用Git，你需要知道:

- 各个名词的含义: Working directory, Staging Area, Git Repository, Remote Repository
- Commits, Branches
- 用`.gitignore`忽略指定文件
- 阅读`diff`的输出。通常现代的代码编辑器会自动高亮出修改的地方
- 使用`clone`, `add`, `rm`, `mv`, `commit`, `push`, `pull`, `status`, `diff`等git简单命令。
- 使用`merge`, `rebase`等命令，懂得如何处理在这些命令中发生冲突时的处理方法。 

在后端开发中，我们将使用GitHub进行代码托管，对于GitHub，你应该知道:

- `clone`, `push`, `pull`, `fetch`来进行与远程仓库的交互
- （可选）提交Pull Requests。（Fork并改动本仓库后，可以向本仓库发起Pull Requests的测试）
- （可选）发起一个issue

参考教程:

- [Pro Git](https://git-scm.com/book/zh/v2)
- 交互式Git教程[Learn Git Branching](https://learngitbranching.js.org)
- GitHub给出的官方教程[Git Handbook](https://guides.github.com/introduction/git-handbook/)

## Python

Python 是一门被广泛运用的语言。其对初学者友好，且含有大量的第三方库，覆盖了各个领域。

Python有2和3两个版本，有部分语法不兼容，可以了解二者语法的差异（可选）。

本次的后端开发计划使用Python 3作为主要的开发语言。具体的小版本待定。

你需要知道：

- Python的基础语法与自带的数据结构，了解库的文件系统，常见的自带库的使用。
- 使用`pip`安装第三方库
- `virtualenv`或`venv`。了解如何通过它们创建新的Python环境，如何激活这个环境。在开发时，我们将采用`virtualenv`等虚拟环境将开发环境与系统的Python环境隔离。
- WSGI，Web Server Gateway Inerface（可选）
- Django框架。我们计划使用此框架作为后端。

参考文档

- [Python Document](https://docs.python.org/)
- [廖雪峰的Python教程](https://www.liaoxuefeng.com/wiki/1016959663602400)
- 《Python核心编程》（Core Python Programming）

#### ~~Do you know Python（可选）~~

Hackergame 2019的一道Python题目，里面有20小问，参考着答案做会让你对Python的数据结构有更深入的了解。题目：[do_you_know_python.py](https://github.com/zeyugao/iGEM-2020-Backend-Learnning-Task/blob/master/do_you_know_python.py)。题解[Write-up](https://github.com/ustclug/hackergame2019-writeups/blob/master/official/%E4%B8%8D%E5%90%8C%E5%AF%BB%E5%B8%B8%E7%9A%84_Python_%E8%80%83%E8%AF%95/README.md)

## Django

本次的开发使用的后端框架即为Django。最后的Task可以帮助你掌握Django

对于Django，你需要知道：

- Django中添加页面（View）。Ref: [Requests and responses](https://docs.djangoproject.com/en/3.0/intro/tutorial01/)、[Views and templates](https://docs.djangoproject.com/en/3.0/intro/tutorial03/)和[Forms and generic views](https://docs.djangoproject.com/en/3.0/intro/tutorial04/)
- 通过ORM(Object-relational mapping)的方法与数据库进行交互。Ref: [Tutorial02](https://docs.djangoproject.com/en/3.0/intro/tutorial02/)
- 编写Django的单元测试。Ref: [Testing](https://docs.djangoproject.com/en/3.0/intro/tutorial05/)
- （可选）Django自带的认证系统。Ref: [User authentication in Django](https://docs.djangoproject.com/en/3.0/topics/auth/)
- （可选）在Django中实现[Restful](https://www.zhihu.com/question/28557115)。现成的框架：[django-rest-framework](https://www.django-rest-framework.org/)

参考：

- [Django documentation](https://docs.djangoproject.com/en/3.0/)
- [w3cschool](https://www.w3cschool.cn/django/)

## Docker（可选）

Docker是一个开源软件项目，让应用程序能够在隔离的容器中进行自动化工作。

关于Docker你需要知道：

- Docker的常用命令：`run`, `start`, `stop`, `restart`, `kill`, `exec`等
- `Dockerfile`和`.docker-compose`文件的阅读
- 管理本地镜像与镜像仓库

参考：

- [Docker document](https://docs.docker.com)
- [阮一峰的Docker教程](https://www.ruanyifeng.com/blog/2018/02/docker-tutorial.html)

## Database

熟悉以下内容：

- 关系型数据库（RDBMS）的相关概念。
- SQL 语⾔的基本使⽤。学会使用SQL语言进行创建/修改/删除数据库/表，查询数据、插入数据。
- 尝试安装MySQL，在上面进行简单的SQL操作。
- 认识其他类型的数据库，例如⽂档型数据库（如 MongoDB）、图数据库（如 Neo4j）、键值对存储数据库（如 Redis）

## Task

虽然不是必须的，但建议尝试完成以下任务。

### 微型博客系统（摘自2018年后端任务）

要求使⽤ Django 和 MySQL （SQLite亦可）构建简单的多⽤户博客站点，并⽤ Git 管理你的代码。⾄少要求实现⽤户注册、登录；博⽂展示、管理；简单权限控制等。

完成基础功能后可以思考：

- 如果⼀个⽤户有很多博⽂，在⼀⻚中显示出来是不合适的。有什么解决⽅案？（关键词: Pagination）
- 对于权限控制这⼀逻辑，也许你会直接在视图函数中写条件语句进⾏判断。这很直接，但如果将来逻辑复杂了起来（⽐如出现了积分等级系统），如此实现的权限系统会⾮常难管理。你有什么改进⽅案？
- 上⼀个问题中的假设场景其实可⻅于当今⽹上的各博客系统中。这说明权限控制已不是⼀个新鲜问题，⽽且很可能已经有了成熟的解决⽅案。你能找到相关的库并将其应⽤到⾃⼰的博客系统中吗？
- 也许你注意到了⽂档中的[提醒](https://docs.djangoproject.com/en/3.0/intro/tutorial01/#the-development-server)：不要在⽣产环境使⽤`runserver`命令。这⼀点很重要，因为 Django ⾃带的开发服务器没有任何优化。你能尝试将⾃⼰的博客站点部署在⽣产环境中吗？（关键词`apache`, `nginx`, `uwsgi`）

### 生物组件的管理

#### 前言

在生物代谢中，有这样几个名词：Model，Metabolite（代谢物），Reaction（反应）（化学与生物意义上），Gene（基因）。

可以这样子进行理解：
- 一个Model是一个代谢过程，这个代谢过程由许多个Reaction构成。
- 一个Reaction中有多个作为反应物以及生成物的Metabolite。
- 在宏观上来看，一个Model由许多个Gene进行调控

#### 正题

现在有许多个json文件，每个json包含了一个Model的信息。

你需要将这些json文件解析，导入到Django的数据库中。解析JSON的方法见：[JSON encoder and decoder](https://docs.python.org/3/library/json.html)

要求：

- 使用ORM的方法存储Model，Metabolite，Reaction和Gene的信息与联系（如果有，通过ForeignKey或ManyToManyField等方式实现）
- Model保存的信息：`id`，包含的Metabolite、Reaction和Gene
- Metabolite保存的信息：`id`，`name`，`formula`
- Reaction保存的信息：`id`，`name`，包含的Metabolite。**不**要求记录在这个反应中各个Metabolite的消耗量与生成量
- Gene保存的信息：`id`，`name`
- 提供一个网页，可以查询Model，Metabolite，Reaction，Gene的信息

JSON下载： [GitHub Hosted](https://raw.githubusercontent.com/zeyugao/iGEM-2020-Backend-Learnning-Task/master/models.zip) or [Atler Server Hosted](http://igem.elsagranger.tk/attachment/models.zip)

> 请不要学用GitHub来添加无法被追踪的二进制文件这个错误例子

#### 参考：

在`models.py`定义的Django Model参考：

```python
from django.db import models as _models

class Model(_models.Model):
    id_ = _models.CharField(unique=True, max_length=127, db_index=True)

class Reaction(_models.Model):
    id_ = _models.CharField(max_length=127, unique=True, db_index=True)
    name = _models.CharField(max_length=255, blank=True)
    models = _models.ManyToManyField(Model)

class Metabolite(_models.Model):
    id_ = _models.CharField(unique=True, max_length=127, db_index=True)
    name = _models.CharField(max_length=511)

    reactions = _models.ManyToManyField(Reaction)

class Gene(_models.Model):
    id_ = _models.CharField(unique=True, max_length=127, db_index=True)
    name = _models.CharField(max_length=127)

    models = _models.ManyToManyField(Model)
```
