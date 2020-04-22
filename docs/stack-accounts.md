# Username and Password

These accounts are required for Node.js image installation and configuration

## MongoDB

* Administrator username: *`root`*
* Administrator password: stored in the file of your server instance: */credentials/password.txt*. You can use **SSH** and run the command to get the database password  
  ```
  cat /credentials/password.txt
  ```

## MySQL

* Administrator username: *`root`*
* Administrator password: stored in the file of your server instance: */credentials/password.txt*. You can use **SSH** and run the command to get the database password  
  ```
  cat /credentials/password.txt
  ```
   ![Run the cat command](https://libs.websoft9.com/Websoft9/DocsPicture/zh/common/catdbpassword-websoft9.png)

> If you want to log in MySQL, refer to [MySQL Web interface Management](/admin-mysql.md) 

## Linux

* Host Name: Internet IP or Public IP of your Instance
* Connect by: Online SSH on Cloud Console or SFTP/SSH tools on your local computer
* Password: It was set by yourself when created instance
* Username: Different Cloud Platform has differences
   |  Cloud Platform   |  Administrator Username   | Other |
   | --- | --- | --- |
   |  Azure   |  It was set by yourself when created instance   | [How to enable root access?](https://support.websoft9.com/docs/azure/server-login.html#sample2-enable-the-root-username) |
   |  AWS CentOS   |  centos   | [How to enable root access?](https://support.websoft9.com/docs/aws/server-login.html#sample2-enable-the-root-username) |
   |  AWS Ubuntu   |  ubuntu   | [How to enable root access?](https://support.websoft9.com/docs/aws/server-login.html#sample2-enable-the-root-username) |
   |  Alibaba Cloud, HUAWEI CLOUD, Tencent Cloud |  root   |

If don't remember the password of Linux, you should reset password on Cloud Console