## ��������

### ���������ļ�ǰ��ġ�#��

```shell
grep -v  "^#" /etc/apt/sources.list
```

### ���ݵĺ�׺���Ե�ǰʱ��

```
.$(date "+%Y_%m_%d_%H.%M.%S") 
```

### �滻

```
sed -i 's/http:\/\/ports\.ubuntu\.com\/ubuntu-ports\//http:\/\/mirrors\.aliyun\.com\/ubuntu-ports\//g' /etc/apt/sources.list
```

### ȥ��ע����

```shell
awk '/^[^#]/' squid.conf
```

ʹ��grep -v "^#" ��ȥ��ע���� | ����-v��ȡ�෴ | ^# ��ʾע���� | ^$ ��ʾ����
cat smb.conf |grep -v "^#"|grep -v "^;"|grep -v "^$"

### ��ʱ����
```shell
* * * * * /usr/sbin/ntpdate 210.72.145.44 > /dev/null 2>&1
```