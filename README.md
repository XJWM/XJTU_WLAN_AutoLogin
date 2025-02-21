## 深澜认证协议,python模拟登录XJTU校园网（仅限兴庆教学区XJTU_STU Wifi 对应认证页面IP为10.6.18.2）

- 根据大佬博客修改，原文在：https://blog.csdn.net/qq_41797946/article/details/89417722
- 1.对原来的jxnu_wifi.py进行了适应性修改，将认证地址改为10.6.18.2及其子域名；将username和password行的账号密码信息删除
- 2.在KIMI的帮助下修改了encryption系列文件的一个数组索引越界的一个错误
- 3.新增了检查网络是否正常连接的检查程序，添加了提示信息

---

## 如何使用

### 1.打开xjtu_wifi.py,安装必须的软件包，然后添加username和password行的账号密码参数,srun_md5.py,srun_xencode.py中都有需要填写账号密码参数的部分，请注意：xjtu_wifi.py在L97,L98分别填写用户名和密码,srun_md5.py在L6填写密码,srun_xencode.py在L72，填写账号和密码

### 2.若调试完成，可用pyintsaller -F -w xjtu_wifi.py的命令进行打包，生成exe文件也可使用

### 3.非教学区的XJTU_STU对应的认证页面是10.6.21.2，不能简单地修改代码中的认证网址就能实现在10.6.21.2环境下的认证，其他版本可能会解决

---

## Contribute Together

### 1.欢迎PR，感谢！

### 2.求star!!! QAQ

---

## Other

###1.程序自动化尝试：尝试在添加用户名和密码后打包为exe文件，发现可以运行；将此程序添加为任务计划程序（以日志记录到设备无线连接到XJTU_STU为触发器），
发现不能自动化运行。

###2.浏览器油猴脚本：这种方法的编程部分更简单，但是要完成认证必须手动打开浏览器并输入认证网址，网页会有执行认证脚本的过程。脚本文件非常简单，补充在项目文件夹TemperMonkey_Scripts中，感谢另一位同学的贡献！
