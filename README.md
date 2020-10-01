# -🎄简介
河南工业大学校园网下使用路由器实现多终端同时上网
# -🛒设备
Newifi d2
# -🎨路由器配置
路由器刷入breed
# -🛠编译openwrt固件
这里采用lean源码编译https://github.com/coolsnowwolf/lede
型号相应选择，记得在`Language`选项下选择`python3`
# -⚡刷写固件
breed下刷入编译的bin固件
# -设置登录脚本
脚本用的是这位学长的https://github.com/ehaut/autologin-srun3k
利用winscp将登陆脚本上传至`/root`目录，更改学号密码
# -启动脚本
`nohup python3 autologin.py >/dev/null 2>&1 &`
# -完善
我用这个脚本每天早上起来会断，需要手动ssh在连接，因此加入`crontab`定时任务,~顺便开机启动~

添加每小时运行一次脚本`0 * * * * sleep 60 && nohup python3 autologin.py >/dev/null 2>&1 &`

~开机启动`@reboot sleep 60 && nohup python3 autologin.py >/dev/null 2>&1 &`~  @reboot在openwrt内无法使用此段作废
# -👾Enjoy！！

