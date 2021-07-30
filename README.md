export PATH="$HOME/kernel dir/proton-clang/bin:$PATH"

export ARCH=arm64
export SUBARCH=arm64

export CROSS_COMPILE=aarch64-linux-gnu- CROSS_COMPILE_ARM32=arm-linux-gnueabi-

make "defconfig"

make menuconfig

cp .config arch/arm64/configs/blabla_defconfig


make -j$(nproc --all) CC=clang CROSS_COMPILE=aarch64-linux-gnu- CROSS_COMPILE_ARM32=arm-linux-gnueabi-
