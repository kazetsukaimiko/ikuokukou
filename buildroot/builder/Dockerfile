FROM alpine
RUN apk add --no-cache make bash perl rsync findutils python3 ncurses ncurses-libs ncurses-dev xz file xz gcc libc-dev

# alpine-sdk libc-dev binutils-cross binutils-cross-embedded


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



# TODO : Import buildroot script for platform (Orange Pi / Drivers) - DONE
# TODO : Import buildroot script for userspace (Python/Java) - DONE
# TODO : Build Maven projects + copy
# TODO : Explore docker (performance)
