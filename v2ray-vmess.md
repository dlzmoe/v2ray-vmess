**v2ray 的搭建脚本**

* 成本：一台境外服务器，一个解析到服务器 ip 的域名
* 服务器提前放行80.443端口(厂商一般默认就放开了，在防火墙查看)


## 开始

1. 在服务器厂商那里重置系统为 CentOS 7.6 最佳，然后重置密码，用户名root，密码自己记好，后面要用。

2. 下载一个可以链接 ssh 的工具，推荐 [finalshell](https://www.hostbuf.com/t/988.html)，其他也行，比如 xshell。

3. 填入服务器的ip、端口号(默认是22)、用户名(默认是root) ，在下面输入框输入密码（上面重置的密码） 。确认无误后，点击登录按钮，开始连接服务器。

根据教程的指示，连接ssh服务器。成功连接后执行脚本。

执行安装脚本
```shell
yum install -y curl
# bash <(curl -sL https://raw.githubusercontent.com/hijkpw/scripts/master/v2ray.sh)
# bash <(curl -sL https://s.hijk.art/centos_install_v2ray2.sh)
# 脚本已失效

# 不可用
# bash <(curl -s -L https://git.io/v2ray.sh)

# 可用 https://github.com/wulabing/V2Ray_ws-tls_bash_onekey
wget -N --no-check-certificate -q -O install.sh "https://raw.githubusercontent.com/wulabing/V2Ray_ws-tls_bash_onekey/master/install.sh" && chmod +x install.sh && bash install.sh
```

4. 选择1 安装v2ray，接下来都是默认回车。

5. 输入域名的时候要保证域名解析到本服务器ip地址。

6. 后面都是默认回车。  

最后会得到一个 vmess.

然后下载 `v2rayN-core` 这个文件，运行里面的 exe 程序，复制刚才的 vmess，然后打开 exe 的剪切板导入，就会自动导入了。

会出现一个列表，右键设为活动服务器。然后右键桌面右下角的小图标 `系统代理` > `自动配置系统代理` ，点击即可，小图标变成红色说明运行成功。

可以打开 Google 试一下了。

7. 可在客户端选择检查更新 v2rayN。

