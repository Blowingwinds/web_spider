## 1.msf_scnner 应用尝试

kali: 192.168.0.103 

​	网络连接状态为物理连接 

win10 1:192.168.0.105

win10 2:192.168.0.107

启动msf，找寻可用的scnner模块

![image-20220217184351690](C:\Users\tel15\AppData\Roaming\Typora\typora-user-images\image-20220217184351690.png)

往下有关于http、smb、vnc、sap等等相关搜索途径的模块

## 2.主机存活测试

#### 利用arp和udp两种方式

```
use auxiliary/discovery/arp_sweep
```

![image-20220217185013221](C:\Users\tel15\AppData\Roaming\Typora\typora-user-images\image-20220217185013221.png)

执行指令run   --》192.168.0.0/24范围查找

![image-20220217185150721](C:\Users\tel15\AppData\Roaming\Typora\typora-user-images\image-20220217185150721.png)

```
use auxiliary/discovery/udp_sweep
```

​	过程类似，直接放结果，速度上udp更快一点

![image-20220217185914429](C:\Users\tel15\AppData\Roaming\Typora\typora-user-images\image-20220217185914429.png)

## 3.http服务搜索

​	该方法较慢

```
use auxiliary/scanner/http/http_version
```

![image-20220217191115543](C:\Users\tel15\AppData\Roaming\Typora\typora-user-images\image-20220217191115543.png)