# Proxy
setup up a proxy ,share problems
一、主流使用软件：
3x-ui
https://github.com/MHSanaei/3x-ui 默认端口号：2053,登陆用户名和密码：admin/admin 支持平台linux与windows amd 与docker 项目:3x-ui
快速安装：bash <(curl -Ls https://raw.githubusercontent.com/mhsanaei/3x-ui/master/install.sh)
wg-easy
https://github.com/wg-easy/wg-easy 默认端口号：51821 首次要创建用户名和密码，无https证书，需要配置环境中使用- INSECURE=true，开放防火墙UDP:51820
安装：1.安装docker 环境curl -sSL https://get.docker.com | sh
      2.sudo mkdir -p /etc/docker/containers/wg-easy
      3.sudo curl -o /etc/docker/containers/wg-easy/docker-compose.yml https://raw.githubusercontent.com/wg-easy/wg-easy/master/docker-compose.yml
      4.编辑docker-compose.yaml文件，注意改网段和环境变量，要去除option这行
      5.cd /etc/docker/containers/wg-easy
      6.sudo docker compose up -d
使用：<img width="1384" height="870" alt="image" src="https://github.com/user-attachments/assets/aced425b-83c1-446c-93cf-5da52e742911" />
<img width="1471" height="776" alt="image" src="https://github.com/user-attachments/assets/090b7e93-1301-4baf-aa10-72172f89b118" />
Prometheus格式的访问格式为ip+port/metrics/prometheus
