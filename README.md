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