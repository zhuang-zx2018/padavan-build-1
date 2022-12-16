## 说明

- 直接Fork到自己的仓库，修改好 .github/workflows/build-padavan.yml 文件之后，点击右上角的 Star 星星按钮即可开始自动编译
- 可更改需要编译的源码，hanwckf 或者 chongshengB 两种源码
- 可更改需要编译的型号，注意名称要与源码configs/templates/目录下的名字相同
- 重新编译点击 Unstar 星星按钮后再点击 Star 星星按钮即可重新编译

## 依赖说明

```shell
# Debian/Ubuntu
sudo apt update
sudo apt install unzip libtool-bin curl cmake gperf gawk flex bison nano xxd \
	fakeroot kmod cpio git python3-docutils gettext automake autopoint \
	texinfo build-essential help2man pkg-config zlib1g-dev libgmp3-dev \
	libmpc-dev libmpfr-dev libncurses5-dev libltdl-dev wget libc-dev-bin

# Archlinux/Manjaro
sudo pacman -Syu --needed git base-devel cmake gperf ncurses libmpc \
        gmp python-docutils vim rpcsvc-proto fakeroot cpio help2man

# Alpine
sudo apk add make gcc g++ cpio curl wget nano xxd kmod \
	pkgconfig rpcgen fakeroot ncurses bash patch \
	bsd-compat-headers python2 python3 zlib-dev \
	automake gettext gettext-dev autoconf bison \
	flex coreutils cmake git libtool gawk sudo

# CentOS 7
sudo yum update
sudo yum groupinstall "Development Tools"
sudo yum install ncurses-* flex byacc bison zlib-* texinfo gmp-* mpfr-* gettext \
	libtool* libmpc-* gettext-* python-docutils nano help2man fakeroot

# CentOS 8
sudo yum update
sudo yum groupinstall "Development Tools"
sudo yum install ncurses-* flex byacc bison zlib-* gmp-* mpfr-* gettext \
	libtool* libmpc-* gettext-* nano fakeroot

# CentOS 8不能直接通过yum安装texinfo，help2man，python-docutils。请去官网下载发行的安装包编译安装
# 以texinfo为例
# cd /usr/local/src
# sudo wget http://ftp.gnu.org/gnu/texinfo/texinfo-6.7.tar.gz
# sudo tar zxvf texinfo-6.7.tar.gz
# cd texinfo-6.7
# sudo ./configure
# sudo make
# sudo make install

```

## 感谢

- [hanwckf](https://github.com/hanwckf/rt-n56u)
- [LetMeDecay](https://github.com/LetMeDecay/Padavan-build)
- [chongshengB](https://github.com/chongshengB/rt-n56u)
