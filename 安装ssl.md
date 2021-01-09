# 安装 ssl
## linux 下安装 ssl
[openssl](https://www.openssl.org/source/ 'openssl')

### 1. 安装依赖库
```bash
# yum -y install gcc
```

### 2. 编译 & 安装
```bash
# mkdir -p /usr/local/openssl

# cd /usr/local

# tar -xzvf openssl-1.1.1i.tar.gz

# cd openssl-1.1.1i

# ./config --prefix=/usr/local/openssl --openssldir=/usr/local/openssl

# make &&  make install

# ln -sf /usr/local/openssl/bin/openssl /usr/bin/openssl

# echo "/usr/local/openssl/lib" >> /etc/ld.so.conf

# ldconfig -v
```

### 3. 查看 ssl 版本
```bash
# openssl version
OpenSSL 1.1.1i  8 Dec 2020
```

## windows 下安装 ssl
[openssl](http://slproweb.com/products/Win32OpenSSL.html 'openssl')

### 1. 安装

### 2. 配置环境变量
1. 新建环境变量 "OPEN_SSL_HOME"，值是 "D:\Program Files\OpenSSL-Win64"
2. 在 path 里添加 "%OPEN_SSL_HOME%\bin;"
