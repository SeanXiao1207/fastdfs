# Docker for fastdfs-nginx

-将dockerfile文件上传到docker环境服务器(image也可以用https://github.com/happyfish100/fastdfs的)
-执行构建镜像：docker build -t bbjreg.svicloud.com/tools/fastdfs:V3.0 .
-上传镜像：docker push bbjreg.svicloud.com/tools/fastdfs:V3.0

# docker-compose.yml

-支持单机和双机（多机配置类同）部署，具体可以选择对应目录的docker-compose.yml文件即可

# Config

- 多store路径配置：
    -修改storage.conf和mod_fastdfs.conf的store_path_count=目录数，store_path数字下标=路径（store_path0=/var/fdfs0）
    -storage配置对应映射目录
- 多tracker配置：参考双机docker-compose.yml：
    -配置多个tracker服务
    -storage的TRACKER_SERVER指定对应的tracker地址

## Simplest docker run example

使用docker-compose的方式运行即可：
例如：docker-compose up -d

