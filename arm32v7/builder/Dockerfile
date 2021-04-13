FROM alpine:3.13

ENV GCC_ARCH=x86_64
ENV GCC_CC_ARCH=arm-linux-gnueabihf
ENV GCC_LINARO_MAIN_VERSION=6.5-2018.12
ENV GCC_LINARO_VERSION=6.5.0-2018.12

ENV GCC_PATH=/opt/gcc
ENV CC=${GCC_PATH}/gcc-linaro-${GCC_LINARO_VERSION}-${GCC_ARCH}_${GCC_CC_ARCH}/bin/${GCC_CC_ARCH}-

RUN mkdir -p $GCC_PATH; \
    cd $GCC_PATH; \
    wget -c https://releases.linaro.org/components/toolchain/binaries/${GCC_LINARO_MAIN_VERSION}/${GCC_CC_ARCH}/gcc-linaro-${GCC_LINARO_VERSION}-${GCC_ARCH}_${GCC_CC_ARCH}.tar.xz; \
    tar xf gcc-linaro-${GCC_LINARO_VERSION}-${GCC_ARCH}_${GCC_CC_ARCH}.tar.xz; \
    rm -rf gcc-linaro-${GCC_LINARO_VERSION}-${GCC_ARCH}_${GCC_CC_ARCH}.tar.xz;

RUN ${CC}gcc --version