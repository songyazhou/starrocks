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

<<<<<<< HEAD
> 编译后的文件放在starrocks/output目录中
=======
StarRocks can provide satisfying performance in various data analytics scenarios, including multi-dimensional screening and analysis, real-time data analytics, ad hoc analysis. StarRocks also supports thousands of concurrent users. As a result, StarRocks is widely used by companies in business intelligence, real-time data warehouse, user profiling, dashboards, order analysis, operation, and monitoring analysis, anti-fraud, and risk control. At present, over 100 medium-sized and large enterprises in various industries have used StarRocks in their online production environment, including Airbnb, JD.com, Tencent, Trip.com and other well-known companies. There are thousands of StarRocks servers running stably in the production environment.

## Fork

StarRocks forked from Apache Doris(incubating) 0.13 in early 2020. We recreated many important parts of the database from then, including a full vectorized execution engine, a brand new CBO optimizer, a novel real-time update engine, and query federation for data lakes.

Today, there are only about 30% of the code in StarRocks is identical to Apache Doris(incubating).

## Build

Because of the thirdparty dependencies, we recommend building StarRocks with the development docker image we provide.

For detailed instructions, please refer to [build](https://github.com/StarRocks/docs/blob/main/administration/Build_in_docker.md).

## Install

Download the current release [here](https://www.starrocks.io/download/community).  
For detailed instructions, please refer to [deploy](https://github.com/StarRocks/docs/blob/master/quick_start/Deploy.md).

## Links

* [StarRocks official website](https://www.starrocks.com)
* [StarRocks documentation](https://docs.starrocks.com)
* [Introduction to StarRocks](https://starrocks.medium.com/introduction-to-starrocks-7bda3474e0e7?source=friends_link&sk=1288c0abc7cde1ac3a38f8e4d865b178)

## Community
* [StarRocks slack channel](https://join.slack.com/t/starrocks/shared_invite/zt-z5zxqr0k-U5lrTVlgypRIV8RbnCIAzg)
* [StarRocks telegram group](https://t.me/joinchat/73R83y0JOnJkMTll)

## LICENSE

Code in this repository is provided under the [Elastic License 2.0](https://www.elastic.co/cn/licensing/elastic-license). Some portions are available under [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0). Please see our [FAQ](https://www.starrocks.com/en-US/product/license-FAQ).

## Contributing to StarRocks

A big thanks for your attention to StarRocks! 
In order to accept your pull request, please follow the [CONTRIBUTING.md](CONTRIBUTING.md).
>>>>>>> branch-2.3
