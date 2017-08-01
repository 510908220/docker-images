# docker-images

> 整理一些常用的镜像,在需要的时候可以快速使用.



## 镜像

| 文件                            | 说明                                       | 使用                                       |
| ----------------------------- | ---------------------------------------- | ---------------------------------------- |
| Dockerfile_ubuntu16.04_nodejs | 基于ubuntu14.04构建,包含nodejs、python3.  cnpm、pip、apt-get都是使用的阿里云源,国内速度很快. | `sudo docker pull registry.cn-hangzhou.aliyuncs.com/510908220/develop:ubuntu16.04_nodejs` |
|                               |                                          |                                          |
|                               |                                          |                                          |



## 构建

```bash
docker build -t ubuntu16.04_nodejs -f Dockerfile_xxx .
```

