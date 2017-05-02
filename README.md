# Cms
**Bash用的是linux命令**

**git = bash + GUI**

**仓库放在哪个目录就在哪个目录下右键点Git Bash Here**

###基本命令：

#change directory
cd

#make directory
mkdir

#print working directory
pwd

#move
mv

#copy
cp

#remove
rm


###基本命令练习：

Administrator@PC-201701141928 MINGW32 /c
$ pwd
/c

Administrator@PC-201701141928 MINGW32 /c
$ cd aaa

Administrator@PC-201701141928 MINGW32 /c/aaa
$ mkdir hello

Administrator@PC-201701141928 MINGW32 /c/aaa
$ cd hello

Administrator@PC-201701141928 MINGW32 /c/aaa/hello
$ cd ..

Administrator@PC-201701141928 MINGW32 /c/aaa
$ echo 'hello'
hello

Administrator@PC-201701141928 MINGW32 /c/aaa
$ echo 'hello'
hello

Administrator@PC-201701141928 MINGW32 /c/aaa
$ echo 'hello' > a.txt                             //输出内容到a.txt

Administrator@PC-201701141928 MINGW32 /c/aaa
$ cat a.txt
hello                                              //将a.txt中的内容输出

Administrator@PC-201701141928 MINGW32 /c/aaa
$ cp a.txt b.txt                                   //复制文件

Administrator@PC-201701141928 MINGW32 /c/aaa
$ ls ..
'$360Section'/   'Documents and Settings'@   soft/
'$Recycle.Bin'/   MSOCache/                  swapfile.sys
 360SANDBOX/      pagefile.sys              'System Volume Information'/
 aaa/             PerfLogs/                  Users/
 Boot/           'Program Files'/            WiFi_Log.txt
 bootmgr         'Program Files (x86)'/      Windows/
 BOOTNXT          ProgramData/
 discard/         retain/

Administrator@PC-201701141928 MINGW32 /c/aaa
$ cd

Administrator@PC-201701141928 MINGW32 ~
$ cd c aaa
bash: cd: too many arguments                                 //失误了

Administrator@PC-201701141928 MINGW32 ~                      //改变目录
$ cd /c/aaa

Administrator@PC-201701141928 MINGW32 /c/aaa
$ cd ..

Administrator@PC-201701141928 MINGW32 /c
$ mkdir hello

Administrator@PC-201701141928 MINGW32 /c
$ cd hello

Administrator@PC-201701141928 MINGW32 /c/hello
$ cd ..

Administrator@PC-201701141928 MINGW32 /c
$ cd aaa

Administrator@PC-201701141928 MINGW32 /c/aaa
$ mv b.txt ../hello                                  //移动文件

Administrator@PC-201701141928 MINGW32 /c/aaa
$ mv a.txt c.txt                                     //文件重命名

Administrator@PC-201701141928 MINGW32 /c/aaa
$ rm c.txt                                           //删除文件

Administrator@PC-201701141928 MINGW32 /c/aaa
$ clear








###设置Git参数

#显示当前Git的配置
git config --list


#设置提交仓库时的用户名信息
git config --global user.name "杨健"


#设置提交仓库是的邮箱信息
git config --global user.email "291906254@qq.com"

#list -a








Administrator@PC-201701141928 MINGW32 ~
$ echo \
> change \
> your \
> mind
change your mind




关于如何使用git bash进行push与pull

1、进入你项目的目录，进行git初始化，创建.git文件夹

git init

2、将bash引到你要添加文件的目录中使用：

git add *.*

命令添加需要提交的文件

3、添加好要添加的文件后，使用命令：

git status

查看你已经添加的文件

4、确定一次要添加这么多文件后，提交你的文件至git版本管理器

git commit -m 'first commit'

使用git show命令可以查看到你的提交记录


5、到github网站上创建一个仓库，然后将https或ssh码弄下来

1）Https方式　　

git remote add origin https://github.com/用户名/仓库名.git

2）SSH方式

git remote add origin git@github.com:用户名/仓库名.git

6、push本地git至github远程仓库

git push origin master    //origin 为仓库别名

注意：
（1）master指的是分支（branch）名字。一个仓库中默认的分支名字就是master，以后，你可以有别的branch；
（2）如果上一步使用的是SSH方式，那么命令就直接执行，如果使用Https方式，则每次push都需要输入密码

pull与push相反，是将代码从远程仓库同步至本地仓库并merge的命令

git pull origin master
