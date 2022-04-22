# gocc

go 交叉编译器

使用方法 拉到项目之后进入 执行
``` shell
go install 
```

进入 docker/base 目录 执行
```shell
docker build -f Dockerfile -t yyt/gocc-base .
```
然后进入 docker/go-1.16.5 目录执行
```shell
docker build -f Dockerfile -t yyt/gocc-1.16.5 .
```
然后进入 docker/go-latest 目录执行
```shell
docker build -f Dockerfile -t yyt/gocc-latest .
```

# 能编译的参考平台
--targets=windows/*,darwin/*
Platforms: android, darwin, ios, linux, windows
Achitectures: 386, amd64, arm-5, arm-6, arm-7, arm64, mips, mipsle, mips64, mips64le

编译到 windows 7 386 命令
```shell
gocc --targets=windows-7/386 .
```

编译到 windows 7 amd64 命令
```shell
gocc  --targets=windows-7/amd64 .
```

注意 要想在 windows下运行不出现 dos窗口 需加上参数 -ldflags "-H windowsgui"

# 编译
```shell
gocc -ldflags "-H windowsgui" --targets=windows-7/386 .
gocc -ldflags "-H windowsgui" --targets=windows-7/amd64 .
```