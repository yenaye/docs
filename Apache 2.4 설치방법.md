

1. expat-devel 설치
```
 yum install gcc gcc-c++ expat-devel zlib-devel (root권한)
```


2. pcre 설치
```
 cd /home/apps/
 tar xvfz pcre-8.43.tar.gz
 cd /home/apps/pcre-8.43
 ./configure --prefix=/home/apps/pcre
 make
 make install
```


3. apr 설치 
(** APR이란 : 어플리케이션 실행을 위해 사용 될 수 있는 공용 라이브러리를 묶어 놓은 것)
```
cd  /home/apps/
tar xvfz apr-1.7.0.tar.gz
cd apr-1.7.0
./configure --prefix=/home/apps/apr
cp -arp libtool libtoolT (중요)
make
make install
```


4. apr-util 설치
```
cd /home/apps/
tar xvfz apr-util-1.6.1.tar.gz
cd apr-util-1.6.1
./configure --prefix=/home/apps/apr-util --with-apr=/home/apps/apr
make
make install
```


5. openssl 설치 (root권한)
```
cd  /home/apps/
tar xvfz openssl-1.1.0d.tar.gz
cd openssl-1.1.0d
./config shared --openssldir=/home/apps/openssl
make
make install
```


6. apache 설치
```
cd  /home/apps/
tar xvfz httpd-2.4.41.tar.gz
cd httpd-2.4.41
./configure --prefix=/home/apps/apache --enable-module=so --enable-so  --enable-mods-shared=ssl --with-ssl=/home/apps/openssl --enable-ssl=shared --with-pcre=/home/apps/pcre  --with-apr=/home/apps/apr --with-apr-util=/home/apps/apr-util
make
make install
```


apache 설치 중 make할 때 OPENSSL_sk_num 에러 발생시
```
cd /usr/lib64/
ll -l | grep libssl.so (libssl.so -> libssl.so.1.0.1e soft 링크 확인)
rm libssl.so (soft 링크가 걸려있을 경우 제거)
ll -l | grep libcrypto.so (libcrypto.so -> libcrypto.so.1.0.1e soft 링크 확인)
rm libcrypto.so (soft 링크가 걸려있을 경우 제거)
```
