# cloudpanel

azure 面板安装教程
安装docker
bash <(curl https://get.docker.com)

部署容器
docker run --name cloudpanel -d -it -p 8111:80 --restart=always cdntip/cloudpanel /bin/bash
其中8111端口 可以自行修改。

创建账号
docker exec -it cloudpanel /bin/bash  # 进入容器
python3 manage.py createsuperuser    # 创建管理员命令， 根据提示创建即可

部署完成， 浏览器打开 ip+端口即可。

后台地址 http://ip:8111/api/admin/
