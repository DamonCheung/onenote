Ubuntu Linux系统包含两类环境变量：系统环境变量和用户环境变量。系统环境变量对所有系统用户都有效，用户环境变量仅仅对当前的用户有效。

文章转载自http://leonhongchina.blog.163.com/blog/static/180294117201132611320112/

修改用户环境变量
用户环境变量通常被存储在下面的文件中：

~/.profile
~/.bash_profile 或者 ~./bash_login
~/.bashrc
上述文件在Ubuntu 10.0以前版本不推荐使用。

系统环境变量
系统环境变量一般保存在下面的文件中：

/etc/environment
/etc/profile
/etc/bash.bashrc
/etc/profile和 /etc/bash.bashrc在Ubuntu 10.0版本中不推荐使用。

加入环境变量
如想将一个路径加入到$PATH中，可以像下面这样做（修改/etc/profile）：

$ sudo nano /etc/profile
在里面加入:

export PATH="$PATH:/my_new_path"
你可以自己加上指定的多个路径，中间用冒号隔开。环境变量更改后，在用户下次登陆时生效，如果想立刻生效，则可执行下面的语句：

$source /etc/profile
