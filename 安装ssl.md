# 官网
https://www.openssl.org/source/

# 安装依赖库
```
# yum -y install gcc
```

# 编译 & 安装
```
# cd /usr/local/ssl

# tar -zxvf openssl-1.1.0g.tar.gz

# cd openssl-1.1.0g

# ./config --prefix=/usr/local/ssl --openssldir=/usr/local/ssl

# make &&  make install
```

# 配置环境变量
```
# cd /usr/local

# ln -s ssl ssl

# vim /etc/ld.so.conf
/usr/local/ssl/lib

# ldconfig

# vim /etc/profile
export SSL_HOME=/usr/local/ssl
export PATH=$PATH:{SSL_HOME}/bin

# source /etc/profile

# mv /usr/bin/openssl /root/

# ln -s /usr/local/ssl/bin/openssl /usr/bin/openssl
```

# 查看openssl版本
```
# openssl version
OpenSSL 1.1.0g  2 Nov 2017
```
