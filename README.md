# Using-the-LAN-to-share-a-web-proxy-for-other-devices

Note for using the LAN to share a web proxy for other devices


# 整体思路

为局域网其他设备提供代理服务的思路很简洁清晰就是

1. 各设备在同一局域网下后
2. 主动共享代理网络的设备允许来自局域网的连接，任意设备都可以共享代理
3. 被共享网络的设备设置对应连接的代理，任意设备都可以连接代理

# 开启共享代理网络

## windows

环境 win 11 ，工具 clash

1. windows 开启移动热点

   ![image-20231203133735138](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203133735138.png)
2. windows 开启 allow LAN 选项

   ![image-20231203133333240](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203133333240.png)
3. 记录 windows 的局域网 IP，这里是 192.168.0.114

   ![image-20231203133457371](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203133457371.png)

![image-20231203133543915](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203133543915.png)

4. 记录 windows 的代理端口，这里是使用默认的 7890

![image-20231203133909861](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203133909861.png)

## Android

1. 开启移动热点
2. 开启 allow LAN 选项并设置端口

   2.1. 打开 clash 软件点击设置

   ![image-20231203135706937](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203135706937.png)

2.2. 点击覆写

![image-20231203135721527](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203135721527.png)

2.3. 设置相应端口并开启允许来自局域网的连接，这里设置的端口号后面用于其他设备连接代理

![image-20231203135745845](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203135745845.png)

3. 记录 android 设备的 IP，各 android 设备异曲同工

   3.1. 设置中点击关于手机

   ![image-20231203140241156](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203140241156.png)

   3.2. 点击状态信息

   ![image-20231203140322716](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203140322716.png)

   3.3. 记录局域网 IP

   ![image-20231203140404717](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203140404717.png)

# 其他设备连接代理

1. 连接局域网，就是连接共享网咯的热点 WIFI，这里不多加赘述
2. 按之前记录的主动共享网络的局域网 IP 和代理端口号，手动设置代理

## Android

1. 点击WiFi详情页

   ![image-20231203134657865](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203134657865.png)
2. 点击代理，点击手动代理

![image-20231203134746236](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203134746236.png)

![image-20231203134807718](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203134807718.png)

3. 代理填写之前记录的 IP 和 port

   ![image-20231203134855130](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203134855130.png)

## Windows

1. 设置 -> 网络和 Internet -> 代理

![image-20231203135044598](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203135044598.png)

2. 编辑手动设置代理

![image-20231203135112224](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203135112224.png)

3. 代理填写之前记录的 IP 和 port，并开启代理，记得保存

   ![image-20231203135246759](image/Using%20the%20LAN%20to%20share%20a%20web%20proxy%20for%20other%20devices/image-20231203135246759.png)

然后就可以共享代理网络了。
