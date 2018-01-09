# Git的上传步骤
1.进入GitHub官网：https://guides.github.com
2.注册账号
3.新建数据库（New repository）
点击右上角的+号，选择New repository
 
在Repository下的输入框输入数据库名（例如：hello-world），选择public，点击绿色的create repository
 
3.下载Windows版本的Git，并安装
4.打开cmd，输入ssh-keygen –t rsa –C “your email ”
双引号中输入之前注册GitHub用的邮箱
5.一直敲回车，最后提示成功
6.打开Git bash，进入到
Cd ~/.ssh
Cat id_rsa.pub（可用Tab键补全）
7.进入GitHub的界面
点击头像，选择Settings
 
1）选择SSH and GPG keys，点击右边的New SSH Key，如果第一次操作，下面的文本框 为空，应为
 
2）进入Git bash界面，将之前的Cat id_rsa.pub的内容复制下来（ 左击红色标记的位置，鼠标移到编辑，点击标记，选择以下截图中的内容，再左击以上红色标记的位置，鼠标移到编辑，点击复制）
 

3）输入你想要输入的标题（title），将2）中复制的内容粘贴到key下面的文本框中，点击 Add SSH Key
 
完成以上步骤后，就会出现以下界面
 
4）验证是否成功：在Git bash界面输入：git –T git@github.com ，如果是第一次的会提示是否continue，输入yes就会看到：You've successfully authenticated, but GitHub does not provide shell access 。这就表示已成功连上github。
8.设置username和email
在Git bash 中输入：（global前是两个”-”）,your name指的是你的用户名，your email 指的是之前注册用的邮箱
Git config –global user.name “your name”
 
Git config –global user.email “your email”
 
9.开始上传文件：
1）打开Git bash界面，cd到需要上传的目录下（eg.cd G:/wc）或者新建文件夹（mkdir wc），新建完之后仍需cd到对应的文件夹下。
 
2）在命令行中输入：
Git init
 
初始化需要上传的文件
3）在命令行中输入：
Git add .
Add后加“.”是添加当前文件夹中的所有文件，也可跟指定的文件名，添加指定的文件
4）打开GitHub界面，选择以下地址栏中的内容进行复制
 
如果在主页（http://github.com），可以通过点击红圈圈出来的位置（也就是点击指定的repository）找到以上地址栏
 
5）将本地仓库关联到GitHub上：
Git remote add origin https://github.com/tuotuoshou/helloworld
 
6）pull对应的分支（例如：master）
Git pull origin master 
如果出现以下问题：
 
可输入：
Git pull origin master –allow-unrelated-histories
7)上传代码到GitHub中：
Git push –u origin master
中间可能会弹出输入账号、密码的对话框，输入你的邮箱和密码即可。
8）完成以上步骤，如果GitHub中出现上传的文件，即为成功
 
