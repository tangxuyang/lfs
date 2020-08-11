Linux是我最希望能够涉猎的。

虽然也从很早就开始接触Linux了，那应该是08年的时候，第一次接触Ubuntu。从那时起我每次装机都会装双操作系统，一个是Windows一个时Ubuntu。虽然Ubuntu不是经常用但是我一定要有。还记得18年时候我下定决心从Windows转到Ubuntu，我坚持了很久，在公司一直用。不过很遗憾，最后因为换工作又重新回到了Windows！！

我有时候告诉自己，我要在Linus有生之年进入Linux的世界，虽然我这个目标有点大，但是确实是我真实的想法。

## LFS
Linux from scratch，就是从头开始构建自己的Linux。这样能够增加对Linux的了解。

## 我的host环境
- Ubuntu18.04.1
- git2.17.1
- LFS9.1
## check-expected
我把检查的脚本放到了check.sh了，这里列出期望的结果
- Bash-3.2 (/bin/sh should be a symbolic or hard link to bash)
- Binutils-2.25 (Versions greater than 2.34 are not recommended as they have not been tested)
- Bison-2.7 (/usr/bin/yacc should be a link to bison or small script that executes bison)
- Bzip2-1.0.4
- Coreutils-6.9
- Diffutils-2.8.1
- Findutils-4.2.31
- Gawk-4.0.1 (/usr/bin/awk should be a link to gawk)
- GCC-6.2 including the C++ compiler, g++ (Versions greater than 9.2.0 are not recommended as they have not
been tested)
- Glibc-2.11 (Versions greater than 2.31 are not recommended as they have not been tested)
- Grep-2.5.1a
- Gzip-1.3.12
- Linux Kernel-3.2
- M4-1.4.10
- Make-4.0
- Patch-2.5.4
- Perl-5.8.8
- Python-3.4
- Sed-4.1.5
- Tar-1.22
- Texinfo-4.7
- Xz-5.0.0

运行一下./check.sh，结果如下：
```
bash, version 4.4.19(1)-release
/bin/sh -> /bin/dash
ERROR: /bin/sh does not point to bash
Binutils: (GNU Binutils for Ubuntu) 2.30
./check.sh: line 10: bison: command not found
yacc not found
bzip2,  Version 1.0.6, 6-Sept-2010.
Coreutils:  8.28
diff (GNU diffutils) 3.6
find (GNU findutils) 4.7.0-git
./check.sh: line 22: gawk: command not found
/usr/bin/awk -> /usr/bin/mawk
gcc (Ubuntu 7.3.0-27ubuntu1~18.04) 7.3.0
g++ (Ubuntu 7.3.0-27ubuntu1~18.04) 7.3.0
(Ubuntu GLIBC 2.27-3ubuntu1) 2.27
grep (GNU grep) 3.1
gzip 1.6
Linux version 4.15.0-29-generic (buildd@lgw01-amd64-057) (gcc version 7.3.0 (Ubuntu 7.3.0-16ubuntu3)) #31-Ubuntu SMP Tue Jul 17 15:39:52 UTC 2018
./check.sh: line 36: m4: command not found
GNU Make 4.1
GNU patch 2.7.6
Perl version='5.26.1';
Python 3.6.5
sed (GNU sed) 4.4
tar (GNU tar) 1.29
./check.sh: line 43: makeinfo: command not found
xz (XZ Utils) 5.2.2

```
