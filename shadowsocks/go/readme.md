
使用方法：

使用root用户登录，运行以下命令：
wget –no-check-certificate -O shadowsocks-go.sh https://raw.githubusercontent.com/leassy/LinuxScript/master/shadowsocks/go/shadowsocks-go.sh
chmod +x shadowsocks-go.sh
./shadowsocks-go.sh 2>&1 | tee shadowsocks-go.log

安装完成后，脚本提示如下：
Congratulations, Shadowsocks-go install completed!
Your Server IP:your_server_ip
Your Server Port:your_server_port
Your Password:your_password
Your Local Port:1080
Your Encryption Method:rc4-md5
Welcome to visit:http://xos.me/shadowsocks-go.html
Enjoy it!

卸载方法：
使用 root 用户登录，运行以下命令：
./shadowsocks-go.sh uninstall

安装完成后即已后台启动 Shadowsocks-go ，运行：
/etc/init.d/shadowsocks status

 

可以查看 Shadowsocks-go 进程是否已经启动。
本脚本安装完成后，已将 shadowsocks-go 加入开机自启动。

使用命令：
启动：/etc/init.d/shadowsocks start
停止：/etc/init.d/shadowsocks stop
重启：/etc/init.d/shadowsocks restart
状态：/etc/init.d/shadowsocks status

多用户多端口配置文件示例：
配置文件路径：/etc/shadowsocks/config.json
{
“port_password”:{
“8989”:”password0″,
“9001”:”password1″,
“9002”:”password2″,
“9003”:”password3″,
“9004”:”password4″
},
“method”:”rc4-md5″,
“timeout”:600
}
