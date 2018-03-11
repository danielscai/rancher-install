# rancher-install

### 安装Docker

在节点上运行如下命令 
```
yum install -y docker  docker-compose 

cat > /etc/docker/daemon.json  <<EOF
{
    "registry-mirrors": ["https://ar69mv7u.mirror.aliyuncs.com"]
}
EOF


systemctl enable docker.service
systemctl restart docker
```


### 安装Rancher 服务器

运行如下命令
`sudo docker run -d --restart=unless-stopped -v /root/mysql:/var/lib/mysql -p 80:8080 rancher/server:stable`

### 将新节点加入到 Rancher集群中

到 Rancher 界面中, 选择 "基础架构" -> "主机" , 点击"添加主机" 
