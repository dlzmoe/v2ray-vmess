**v2ray 的搭建脚本**

https://v2raytech.com/bitvise-connect-linux-server-tutorial/

https://v2raytech.com/v2ray-one-click-script-with-mask/


* 成本：一台境外服务器，一个解析到服务器 ip 的域名
* 服务器提前放行80.443端口

Bitvise连接Linux服务器教程 是上面的第一个链接，根据指示下载，然后连接服务器即可。

## 开始

官网：[https://www.bitvise.com/ssh-client-download](https://www.bitvise.com/ssh-client-download)

正常情况官网打不开，因为需要tz.

直接下载脚本软件：[https://netfiles.pw/download.php?filename=/BvSshClient-Inst.exe](https://netfiles.pw/download.php?filename=/BvSshClient-Inst.exe)

填入服务器的ip、端口号(默认是22，搬瓦工默认不是22，请从后台查看)、用户名(默认是root)，`intial method` 选 `password` ，在下面输入框输入密码（服务器密码在管理页面查看），同时勾选 `sotre encrypted password in profile` 。填好后建议点击左侧的 `save profile as` 按钮保存配置，下次使用时无需再填写。确认无误后，点击左下角的登录按钮，开始连接服务器。

根据教程的指示，连接ssh服务器。成功连接后执行脚本。

执行安装脚本
```shell
yum install -y curl
# bash <(curl -sL https://raw.githubusercontent.com/hijkpw/scripts/master/v2ray.sh)
# bash <(curl -sL https://s.hijk.art/centos_install_v2ray2.sh)
# 脚本已失效

bash <(curl -s -L https://git.io/v2ray.sh)
```



然后一直回车就可以了，最后会得到一个 vmess.

然后下载 `v2rayN-core` 这个文件，运行里面的 exe 程序，复制刚才的 vmess，然后打开 exe 的剪切板导入，就会自动导入了。

列表会出现一个ip，就是 v2ray 了，右键设为活动服务器。然后右键桌面右下角的小图标 `系统代理` > `自动配置系统代理` ，点击即可，小图标变成红色说明运行成功。

可以打开 Google 试一下了。


## 其他

但是在用过一段时间后会偶尔失效，重新执行下面的脚本。

```shell
bash <(curl -sL https://s.hijk.art/centos_install_v2ray2.sh)
```

重新获取 vmess 然后放到 v2rayN 即可。
