# alpine-vnc-arm32v7

$ uname -m
x86_64

$ docker run --rm -t arm64v8/ubuntu uname -m
standard_init_linux.go:211: exec user process caused "exec format error"

$ docker run --rm --privileged multiarch/qemu-user-static --reset -p yes

$ docker run --rm -t arm64v8/ubuntu uname -m
aarch64

$ docker run --rm --privileged multiarch/qemu-user-static --reset -p yes
standard_init_linux.go:211: exec user process caused "exec format error"

docker run --rm --privileged multiarch/qemu-user-static:register
