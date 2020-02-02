# ssr-ss-tutorial

默认centos7 

1.先更换服务器内核：

yum -y install wget

wget --no-check-certificate -O rskernel.sh https://raw.githubusercontent.com/hombo125/doubi/master/rskernel.sh && bash rskernel.sh


完成后会重启，重新连接服务器，连上后开始第二步的操作。

2.一键安装锐速：（BBR太垃圾了）

wget -N --no-check-certificate https://raw.githubusercontent.com/91yun/serverspeeder/master/serverspeeder-all.sh && bash serverspeeder-all.sh

3. 安装ssr

脚本一

yum -y install wget

wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/ssr.sh && chmod +x ssr.sh && bash ssr.sh

记得协议 origin
混淆 plain

备用脚本二

./shadowsocksR.sh uninstall

yum -y install wget

wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocksR.sh

chmod +x shadowsocksR.sh

./shadowsocksR.sh 2>&1 | tee shadowsocksR.log



出现类似的就表示成功：
[Running Status]
ServerSpeeder is running!
version              3.10.61.12

[License Information]
License              6291BDBE113A6E9E (valid on current device)
MaxSession           unlimited
MaxTcpAccSession     unlimited
MaxBandwidth(kbps)   unlimited
ExpireDate           2034-12-31

[Connection Information]
TotalFlow            14
NumOfTcpFlows        14
TotalAccTcpFlow      9
TotalActiveTcpFlow   2

[Running Configuration]
accif                eth0       
acc                  1
advacc               1
advinacc             1
wankbps              10000000
waninkbps            10000000
csvmode              0
subnetAcc            0
maxmode              1
pcapEnable           0

其他的一些命令：
service serverSpeeder start #启动
service serverSpeeder stop #停止
service serverSpeeder reload #重新加载配置
service serverSpeeder restart #重启
service serverSpeeder status #状态
service serverSpeeder stats #统计
service serverSpeeder renewLic #更新许可文件
service serverSpeeder update #更新
chattr -i /serverspeeder/etc/apx* && /serverspeeder/bin/serverSpeeder.sh uninstall -f #卸载




