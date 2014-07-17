
# Doogga Data Sync Project
 
将企业内部服务器上的数据传送到doogga的服务器上。
传送过程对帐号/权限/产品有针那性的控制，避免数据泄漏，混乱,因此勿泄漏配置文件信息。

Tips
=============
外网同步到Doogga Hub服务器
-------------
1. 必须安装rsync
2. 需要有passwd.rsync文件
3. passwd.rsync文件的权限需是700
4. 当前用户需要是passwd.rysnc的拥有者，或者是root用户
公司内网机器同步到内网Hub服务器
-------------
1. 必须安装sshpass

Introduce
=============
1. 确保transfer.conf文件中${local_data_path}变量被设置，且设置的路径已存在
2. 正式运行用start_daemon.sh启动程序, 这样程序就会在后台运行
    ./start_daemon.sh

3. 平时调试时启动start.sh进行调试
    ./start.sh

4. 停止运行请到启动脚本的目录下（例如现在就是在当前目录下启动），执行
    ./stop.sh
   停止程序的运行
