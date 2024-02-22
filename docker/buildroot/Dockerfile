FROM alpine
RUN apk add --no-cache alpine-sdk make bash perl rsync findutils python3 ncurses binutils binutils-cross binutils-cross-embedded binutils-aarch64 xz

# Where we are putting buildroot
ENV BUILDROOT=/opt/buildroot

# Version of buildroot to download
ENV VERSION=buildroot-2023.11

# Working directory
RUN mkdir -p $BUILDROOT

WORKDIR $BUILDROOT

RUN wget https://buildroot.org/downloads/${VERSION}.tar.xz -O buildroot.tar.xz

RUN tar -xvf buildroot.tar.xz

WORKDIR $BUILDROOT/$VERSION

# TODO : Import buildroot script for platform (Orange Pi / Drivers)
# TODO : Import buildroot script for userspace (Python/Java)
# TODO : Build Maven projects + copy
# TODO : Explore docker (performance)
