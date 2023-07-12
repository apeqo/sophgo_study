Leds :  /sys/class/leds 直接修改文件数据即可调整亮度方式等信息
NFS配置：网线不够，暂时跳过

Makefile
•“=”：延时赋值，该变量只有在调用的时候，才会被赋值 •“:=”：直接赋值，与延时赋值相反，使用直接赋值的话，变量的值定义时就已经确定了。 论坛：https://www.firebbs.cn/ 355 天猫：https://yehuosm.tmall.com 野火 Linux 基础与应用开发实战指南 基于 i.MX6ULL 系列 •“?=”：若变量的值为空，则进行赋值，通常用于设置默认值。 •“+=”：追加赋值，可以往变量后面增加新的内容。

$(wildcard  \**.c\)

$@ target
$< first prerequisites
$? newer prerequisites
$^ all prerequisites

- Compiling a C program: `n.o` is made automatically from `n.c` with a command of the form `$(CC) -c $(CPPFLAGS) $(CFLAGS) $^ -o $@`
- Compiling a C++ program: `n.o` is made automatically from `n.cc` or `n.cpp` with a command of the form `$(CXX) -c $(CPPFLAGS) $(CXXFLAGS) $^ -o $@`
- Linking a single object file: `n` is made automatically from `n.o` by running the command `$(CC) $(LDFLAGS) $^ $(LOADLIBES) $(LDLIBS) -o $@`

makefile里的shell变量用"/$/$"

procfs 是“process filesystem”的缩写，所以它也被称为进程文件系统，procfs 通常会自动挂载在根 目录下的/proc 文件夹。procfs 为用户提供内核状态和进程信息的接口，功能相当于 Windows 的任 务管理器


locate sys/stat.h 查找安装的编译器

常见头文件：
头文件 stdio.h：C 标准输入与输出（standard input & output）头文件，我们经常使用的打印 函数 printf 函数就位于该头文件中。 • 头文件 stdlib.h：C 标准库（standard library）头文件，该文件包含了常用的 malloc 函数、free 函数。 • 头文件 sys/stat.h：包含了关于文件权限定义，如 S_IRWXU、S_IWUSR，以及函数 fstat 用于 查询文件状态。涉及系统调用文件相关的操作，通常都需要用到 sys/stat.h 文件。 • 头文件 unistd.h：UNIX C 标准库头文件，unix，linux 系列的操作系统相关的 C 库，定义了 unix 类系统 POSIX 标准的符号常量头文件，比如 Linux 标准的输入文件描述符（STDIN）， 标准输出文件描述符（STDOUT），还有 read、write 等系统调用的声明。 • 头文件 fcntl.h：unix 标准中通用的头文件，其中包含的相关函数有 open，fcntl，close 等操 作。 • 头文件 sys/types.h：包含了 Unix/Linux 系统的数据类型的头文件，常用的有 size_t，time_t， pid_t 等类型。

系统调用 C函数库有缓冲区 linux系统调用更加确定化 需要合理选择

I2C：
SDA SCL 
前文中提到的起始 (S) 和停止 (P) 信号是两种特殊的状态，起始和停止信号一般由主机产生。如 下图。 • 当 SCL 线是高电平时 SDA 线从高电平向低电平切换，这个情况表示通讯的起始。 • 当 SCL 是高电平时 SDA 线由低电平向高电平切换，表示通讯的停止。