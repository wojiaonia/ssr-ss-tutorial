# ssr-ss-tutorial

## 默认centos7 

### 1. 安装ssr

脚本一

yum -y install wget

wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/ssr.sh && chmod +x ssr.sh && bash ssr.sh

记得协议 auth_sha1_v4

混淆 plain  (!!!!!!!!!!!!!!!!!)

备用脚本二

./shadowsocksR.sh uninstall

yum -y install wget

wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocksR.sh

chmod +x shadowsocksR.sh

./shadowsocksR.sh 2>&1 | tee shadowsocksR.log

### 2. bbr plus
不要在生产环境使用一键脚本，建议手动安装，进不了系统用vnc切内核

wget "https://github.com/cx9208/bbrplus/raw/master/ok_bbrplus_centos.sh" && chmod +x ok_bbrplus_centos.sh && ./ok_bbrplus_centos.sh
安装后，执行uname -r，显示4.14.129-bbrplus则切换内核成功
执行lsmod | grep bbr，显示有bbrplus则开启成功



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




