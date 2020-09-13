# -🎄简介
河南工业大学校园网下使用路由器实现多终端同时上网
# -🛒设备
Newifi d2
# -🎨路由器配置
路由器刷入breed
# -🛠编译openwrt固件
这里采用lean源码编译https://github.com/coolsnowwolf/lede
型号相应选择，记得在Language选项下选择python3
# -⚡刷写固件
breed下刷入编译的bin固件
# -设置登录脚本
脚本用的是这位学长的https://github.com/ehaut/autologin-srun3k
利用winscp将登陆脚本上传至\root目录，更改学号密码
# -启动脚本
`python autologin.py`
# -👾enjoy！！

