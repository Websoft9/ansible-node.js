# 更多...

下面每一个方案，都经过实践证明行之有效，希望能够对你有帮助

## 域名绑定

当服务器上只有一个网站时，不做域名绑定也可以访问网站。但从安全和维护考量，**域名绑定**不可省却。

以示例网站为例，域名绑定操作步骤如下：

1. 确保域名解析已经生效  
2. 使用 SFTP 工具登录云服务器
2. 修改 [Nginx虚拟机主机配置文件](/zh/stack-components.md#nginx)，将其中的 **server_name** 项的值修改为你的域名
   ```text
   server
   {
   listen 80;
   server_name www.example.com;  # 此处修改为你的域名
   ...
   }
   ```
3. 保存配置文件，重启 [Nginx 服务](/zh/admin-services.md#nginx)


## 使用 Nginx 伪静态

LNMP 环境默认已经安装 伪静态模块，通过下面两个方式配置网站的伪静态规格：

1.  在服务器目录 */etc/nginx/conf.d/rewrite* 下新建你网站的伪静态规则文件（例如：wordpress.conf）
2.  在网站的[虚拟主机配置段](/zh/stack-components.md#nginx) **server{ }** 中将伪静态规则文件 include 进来
   ```text
   server
   {
   listen 80;
   server_name mysite2.yourdomain.com;  # 此处修改为你的域名
   index index.html index.htm index.php;
   root  /data/wwwroot/mysite2;
   ...

   ## Includes one of your Rewrite rules if you need, examples
   include conf.d/rewrite/wordpress.conf;  # 引入你的伪静态规则
   }
   ```
3. 保存配置文件，重启 [Nginx 服务](/zh/admin-services.md#nginx)


## 重置 MySQL 密码

1. 远程连接到服务器，
2. 运行一下命令，按提示输入新密码即可
   ```
   sudo git clone https://github.com/Websoft9/ansible-linux.git; cd ansile-linux/Mysql_ResetPasswd_Script;sudo sh reset_mysql_password.sh
   ```