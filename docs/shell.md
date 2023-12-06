## 常用命令

### 过滤配置文件前面的“#”

```shell
grep -v  "^#" /etc/apt/sources.list
```

### 备份的后缀名以当前时间

```
.$(date "+%Y_%m_%d_%H.%M.%S") 
```

### 替换

```
sed -i 's/http:\/\/ports\.ubuntu\.com\/ubuntu-ports\//http:\/\/mirrors\.aliyun\.com\/ubuntu-ports\//g' /etc/apt/sources.list
```

### 去掉注释行

```shell
awk '/^[^#]/' squid.conf
```

使用grep -v "^#" 来去掉注释行 | 其中-v是取相反 | ^# 表示注解行 | ^$ 表示空行
cat smb.conf |grep -v "^#"|grep -v "^;"|grep -v "^$"

### 定时任务
```shell
* * * * * /usr/sbin/ntpdate 210.72.145.44 > /dev/null 2>&1
```