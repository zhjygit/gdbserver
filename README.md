# gdbserver-arm
静态gdbserver-arm
## 前置
```
sudo apt-get install gcc-arm-linux-gnueabi
sudo apt-get install g++-arm-linux-gnueabi
sudo apt-get install texinfo
```
## 源码
http://ftp.gnu.org/gnu/gdb/
## 动态编译
```
mkdir build
cd build
../configure --target=arm-linux --prefix=/opt/arm-linux-gdb
make -j4
make
```
## 静态编译
gdb源码的 /gdb/server目录下
将Makefile的139行加上 -static
执行
```
./configure --target=arm-linux --host=arm-linux-gnueabi CFLAGS=-static
make -j4
```
