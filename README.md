# Mid
Mid ——移动端优化解决方案

## Git更换用户要比Github难很多

### git config
基本命令，查询git语句。从列表中选择我们需要操作的命令。

###git config user.email  或者  cat ~/.gitconfig | head -3 
查看用户邮件信息，我们发现，这个邮件和我们所接入的项目账户名不符合，那么我们就需要更改邮箱以及密码的设置。

###git config --global user.email "email"
修改用户名邮件信息。修改名称同上一致。cat ~/.gitconfig | head -3 

###难点
又到了修改密码的难点了，记得上次是修改一个文件，蛮不容易的，语句是什么的，忘记了，看来只能重新查询了。

### 现在的问题是git无法同步
user.password
试着用下这个语句提示修改成功。  

### 找到这个文件了，输入vi .git/config
终于成功了，在这里大致说一下解决方案。
更换git用了我大约一个小时的时间去解决这个问题。
首先就是更改用户名和用户邮箱，这个用语句直接更改就好了。
然后用vi编辑配置文件，因为这个文件地址前面没有加入用户名，我们加入用户名。url = https://xxx(你的用户名)@github.com/**/xxx.git 基本是这个形式的，进行保存，这样就可以了。
用esc退出输入：wq保存即可

### 现在新建立一个项目进行第二次测试
就是当打开新的项目时候，这个是否还可以使用。


