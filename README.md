# CentosScripts
There are about Centos scripts


#环境依赖
Linux localhost.localdomain 4.9.93-010.ali3000.alios7.x86_64 #1 SMP Fri Apr 20 00:18:51 CST 2018 x86_64 x86_64 x86_64 GNU/Linux

#使用问题
mode1模式下eth0 link down无法自动切换至eth1

#使用方法

1) 解压tar包
tar -xvf Change_network #放到任何位置即可

2) 初始化脚本
bash init.sh #执行完成之后会自动隐藏

3) 检查脚本运行状况
[root@localhost.localdomain /home/Change_network]
#ps -ef | grep -i change | grep -v grep
root      1111     1  0 11:33 ?        00:00:00 sh /home/NETWORK/Change_network.sh
root     12263 12259  0 11:45 ?        00:00:00 /bin/sh /home/NETWORK/check_change_network.sh

#systemctl status change_network

4) 启动服务
systemctl start change_network


#目录结构
#

[root@localhost.localdomain /home/Change_network]
#tree
#.
#├── change_network.service  / 添加systemd管控
#├── Change_network.sh	/ 切换网卡
#├── check_change_network.sh / 监控切换网卡服务脚本
#├── init.sh / 服务初始化
#├── nohup.out / 没用
#└── README / help you and help me. baby
#

