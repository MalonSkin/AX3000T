# 小米路由器AX3000T解锁SSH，安装ShellCrash直接科学上网，ShellClash
小米路由器AX3000T解锁SSH，安装ShellCrash直接科学上网，不用刷机openwrt

## 一、Xiaomi 路由器 AX3000T 解锁SSH:
### 1、Windows搜索cmd，以管理员身份运行：

    curl -X POST http://192.168.31.1/cgi-bin/luci/;stok=XXXXXX/api/misystem/arn_switch -d "open=1&model=1&level=%0Anvram%20set%20ssh_en%3D1%0A"
    curl -X POST http://192.168.31.1/cgi-bin/luci/;stok=XXXXXX/api/misystem/arn_switch -d "open=1&model=1&level=%0Anvram%20commit%0A"
    curl -X POST http://192.168.31.1/cgi-bin/luci/;stok=XXXXXX/api/misystem/arn_switch -d "open=1&model=1&level=%0Ased%20-i%20's%2Fchannel%3D.*%2Fchannel%3D%22debug%22%2Fg'%20%2Fetc%2Finit.d%2Fdropbear%0A"
    curl -X POST http://192.168.31.1/cgi-bin/luci/;stok=XXXXXX/api/misystem/arn_switch -d "open=1&model=1&level=%0A%2Fetc%2Finit.d%2Fdropbear%20start%0A"

## 2、计算SSH密码
https://miwifi.dev/ssh 输入路由器的SN码，在路由器后台可以查询SN码。

用putty软件登录路由器

用户名是：root，密码是上一步计算出来的，提示 Are U OK 表示已经登录成功。
