环境: ubuntu20.04.1



安装 nasm 2.15.05

```
wget https://www.nasm.us/pub/nasm/releasebuilds/2.15.05/nasm-2.15.05.tar.bz2
tar -xvf nasm-2.15.05.tar.bz2
cd nasm-2.15.05
./configure
make
sudo make install
```



编译

```bash
sudo apt-get install build-essential uuid-dev iasl -y
sudo apt-get install python-is-python3
sudo apt-get install gcc python3-distutils -y

git clone https://github.com/tianocore/edk2.git
cd edk2
git submodule update --init
make -C BaseTools 


export EDK_TOOLS_PATH=$HOME/edk2/BaseTools
. edksetup.sh BaseTools
```



## 修改Conf/target.txt

```
TARGET_ARCH = X64
TOOL_CHAIN_TAG        = GCC
```











