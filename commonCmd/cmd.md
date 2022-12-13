
## 常用命令

### linux
#### 当前文件夹磁盘大小
du -lh --max-depth=1

### ssk-key
ssh-keygen.exe -t rsa -C "邮箱"

### git配置
git config --global user.name "xxx"
git config --global user.email "xx@xx.com"

### windwows查看端口占用
netstat -aon | findstr "端口号"

### 更新unityPackage
python -m upmscripts.auto_publish
### 创建unityPackage
python -m upmscripts.new_package

### git tag
1.创建tag
git tag -a v1.0.9 -m "some comment"
2.推送单个tag
git push origin [tagname]

### 安卓打包release
gradle clean assembleOriginalCNrelease

### docker操作
// build
docker build -f [DockerFilePath] -t [name:tag]
https://www.runoob.com/docker/docker-build-command.html

// push images
docker push [imageUrl]
imageUrl=docker.xxxGroup.com:5000/xxxservice/app/building:vX.X.X-X-xxxxx

// 看日志
docker logs -f [containerID]

// 删镜像
docker rmi [imageID]
子命令
-f: 强制删除, 即便有容器引用该镜像
-no-prune: 不要删除未带标签的父镜像

// 清理镜像
docker image prune
子命令
-a, --all: 删除所有没有用的镜像, 而不仅仅是临时文件
-f, --force: 强制删除镜像文件, 无需弹出提示确认

// 查找过滤
docker ps -f name=xxx --format "{{.Names}}, {{.ID}}"

// 一些测试
docker run -itd -p 9299:9299 -p 9295:9295 -p 17010:17010 -p 18010:18010/udp -p 19010:19010/udp docker.xxx.com:5000/xxxservice/xxx:2.0

### k8s操作
// 打印环境变量
kubectl exec [资源名] -- printenv

