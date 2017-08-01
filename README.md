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



## 推送

这里使用的是阿里云提供的[镜像服务](https://cr.console.aliyun.com/#/imageList).

STEP1:创建一个镜像仓库

我这里是`registry.cn-hangzhou.aliyuncs.com/510908220/develop`

STEP2: 登陆阿里云docker registry:

`sudo docker login --username=528194763@qq.com registry.cn-hangzhou.aliyuncs.com`

STEP3:推送

```bash
$ sudo docker tag [ImageId] registry.cn-hangzhou.aliyuncs.com/510908220/develop:[镜像版本号]
$ sudo docker push registry.cn-hangzhou.aliyuncs.com/510908220/develop:[镜像版本号]
```



相当于是在阿里云web上已经创建了仓库,然后本地就创建不同的镜像版本推送即可. 和往`docker hub`推送还是有点区别的.

```bash
docker push [OPTIONS] NAME[:TAG]
```

比如`docker push westdoorblowcola/django:1.8.2`，相当于`westdoorblowcola/django`是仓库