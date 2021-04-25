**v2ray 的搭建脚本**

https://v2raytech.com/bitvise-connect-linux-server-tutorial/

https://v2raytech.com/v2ray-one-click-script-with-mask/


* 成本：一台境外服务器，一个解析到服务器 ip 的域名
* 服务器提前放行80.443端口

Bitvise连接Linux服务器教程 是上面的第一个链接，根据指示下载，然后连接服务器即可。

根据教程的指示，成功连接后执行脚本

```shell
yum install -y curl
bash <(curl -sL https://s.hijk.art/centos_install_v2ray2.sh)
```

然后一直回车就可以了，最后会得到一个 vmess.

然后下载 `v2rayN-core` 这个文件，运行里面的 exe 程序，复制刚才的 vmess，然后打开 exe 的剪切板导入，就会自动导入了。

列表会出现一个ip，就是 v2ray 了，右键设为活动服务器。然后右键桌面右下角的小图标 `系统代理` > `自动配置系统代理` ，点击即可，小图标变成红色说明运行成功。

可以打开 Google 试一下了。


## 其他

但是在用过一段时间后会偶尔失效，重新执行下面的脚本

```shell
bash <(curl -sL https://s.hijk.art/centos_install_v2ray2.sh)
```

重新获取 vmess 然后放到 v2rayN 即可
