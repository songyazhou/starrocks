# starrocks_source

StarRocks 源代码

# 通过源码编译StarRocks

## 前提条件
在编译StarRocks之前,请确保您已安装Docker

## 下载镜像
```
docker pull starrocks/dev-env:branch-2.3
```

## 编译StarRocks
``` bash
# 创建编译目录
mkdir /data/sr_build
cd /data/sr_build

# 下载项目代码
git clone https://git.zorelworld.com/BigData/Platform/starrocks_source.git starrocks
cd starrocks

# 运行docker编译环境
docker run -it -v /data/sr_build/.m2:/root/.m2 -v /data/sr_build/starrocks:/root/starrocks --name sr_build -d starrocks/dev-env:branch-2.3

# 运行编译脚本
docker exec -it sr_build /root/starrocks/build.sh
```

> 编译后的文件放在starrocks/output目录中