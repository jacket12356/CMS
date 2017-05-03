# Cms
**Bash用的是linux命令**

**git = bash + GUI**

**仓库放在哪个目录就在哪个目录下右键点Git Bash Here**
<hr/>

<h3>基本命令：</h3>

#change directory<br/>
*cd*

#make directory<br/>
*mkdir*

#print working directory<br/>
*pwd*

#move<br/>
*mv*

#copy<br/>
*cp*

#remove<br/>
*rm*


<h3>基本命令练习：</h3>

Administrator@PC-201701141928 MINGW32 /c<br/>
$ pwd<br/>
/c

Administrator@PC-201701141928 MINGW32 /c<br/>
$ cd aaa

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ mkdir hello

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ cd hello

Administrator@PC-201701141928 MINGW32 /c/aaa/hello<br/>
$ cd ..

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ echo 'hello'<br/>
hello

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ echo 'hello'<br/>
hello

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ echo 'hello' > a.txt                             //输出内容到a.txt

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ cat a.txt<br/>
hello                                              //将a.txt中的内容输出

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ cp a.txt b.txt                                   //复制文件

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ ls ..<br/>
'$360Section'/   'Documents and Settings'@   soft/<br/>
'$Recycle.Bin'/   MSOCache/                  swapfile.sys<br/>
 360SANDBOX/      pagefile.sys              'System Volume Information'/<br/>
 aaa/             PerfLogs/                  Users/<br/>
 Boot/           'Program Files'/            WiFi_Log.txt<br/>
 bootmgr         'Program Files (x86)'/      Windows/<br/>
 BOOTNXT          ProgramData/<br/>
 discard/         retain/<br/>

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ cd

Administrator@PC-201701141928 MINGW32 ~<br/>
$ cd c aaa<br/>
bash: cd: too many arguments                                 //失误了

Administrator@PC-201701141928 MINGW32 ~                      //改变目录<br/>
$ cd /c/aaa

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ cd ..

Administrator@PC-201701141928 MINGW32 /c<br/>
$ mkdir hello

Administrator@PC-201701141928 MINGW32 /c<br/>
$ cd hello

Administrator@PC-201701141928 MINGW32 /c/hello<br/>
$ cd ..

Administrator@PC-201701141928 MINGW32 /c<br/>
$ cd aaa

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ mv b.txt ../hello                                  //移动文件

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ mv a.txt c.txt                                     //文件重命名

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ rm c.txt                                           //删除文件

Administrator@PC-201701141928 MINGW32 /c/aaa<br/>
$ clear








<h3>设置Git参数</h3>

#显示当前Git的配置<br/>
*git config --list*


#设置提交仓库时的用户名信息<br/>
*git config --global user.name "杨健"*


#设置提交仓库是的邮箱信息<br/>
*git config --global user.email "291906254@qq.com"<br/>
<br/>
#list -a*








Administrator@PC-201701141928 MINGW32 ~<br/>
$ echo \ <br/>
> change \ <br/>
> your \ <br/>
> mind <br/>
change your mind




关于如何使用git bash进行push与pull<br/>

1、进入你项目的目录，进行git初始化，创建.git文件夹<br/>

*git init<br/>*

2、将bash引到你要添加文件的目录中使用：<br/>

*git add '*.*'<br/>*

命令添加需要提交的文件<br/>

3、添加好要添加的文件后，使用命令：<br/>

*git status<br/>*

查看你已经添加的文件<br/>

4、确定一次要添加这么多文件后，提交你的文件至git版本管理器<br/>

*git commit -m 'first commit'<br/>*

使用git show命令可以查看到你的提交记录<br/>


5、到github网站上创建一个仓库，然后将https或ssh码弄下来<br/>

1）Https方式　　<br/>

*'git remote add origin https://github.com/用户名/仓库名.git<br/>'*

2）SSH方式<br/>

*git remote add origin git@github.com:用户名/仓库名.git<br/>*

6、push本地git至github远程仓库<br/>

*git push origin master    //origin 为仓库别名<br/>*

注意：<br/>
（1）master指的是分支（branch）名字。一个仓库中默认的分支名字就是master，以后，你可以有别的branch；<br/>
（2）如果上一步使用的是SSH方式，那么命令就直接执行，如果使用Https方式，则每次push都需要输入密码<br/>

pull与push相反，是将代码从远程仓库同步至本地仓库并merge的命令<br/>
<br/>
*git pull origin master*
