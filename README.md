# 谷歌云 Google Cloud Platform 免费300美金注册方法
## 前言
1. 注册一个Google账号。
2. 一张双币信用卡（如：建行VISA卡）。
3. 科学上网网络。
---
## 步骤一：注册谷歌云
* 打开Google进入「[Google云端平台](https://console.cloud.google.com/home/dashboard?project=resolute-vault-248504&hl=zh-CN)」。
![01](https://github.com/masonvip/GCP/blob/master/readme.md/01.png?raw=true)

* 弹出Google Cloud Platform欢迎您的界面。
* 勾选同意条款。
* 所在国家/地区选择「香港」。⚠️中国选项已被谷歌云移除。
* 同意并继续。
* 会让你填写实名信用卡信息，地址填写香港地址。⚠️信用卡会扣除约10港币，注册完成自动返还到原账户。
![02](https://github.com/masonvip/GCP/blob/master/readme.md/02.png?raw=true)

* 完成后会显示赠金和天数。
![03](https://github.com/masonvip/GCP/blob/master/readme.md/03.png?raw=true)

---
## 步骤二：防火墙规则设置
* 点选左上角三横线「导航菜单」。
* 下拉到「网络」，点选「VPC网络」，点选「防火墙规则」。
![04](https://github.com/masonvip/GCP/blob/master/readme.md/04.png?raw=true)

* 点选创建防火墙规则
![05](https://github.com/masonvip/GCP/blob/master/readme.md/05.png?raw=true)
* 名称：all
* 目标：网络中所有实例
* 来源IP地址范围：0.0.0.0/0
* 协议和端口：全部允许
* 点选创建。
![06](https://github.com/masonvip/GCP/blob/master/readme.md/06.png?raw=true)
---
## 步骤三：创建实例
* 点选左上角三横线「导航菜单」。
* 下拉到「计算」，点选「Compute Engine」，点选「VM实例」。
![07](https://github.com/masonvip/GCP/blob/master/readme.md/07.png?raw=true)
* 点选「创建实例」。
![08](https://github.com/masonvip/GCP/blob/master/readme.md/08.png?raw=true)
* 名称：默认，可以自定义。
* 区域：选择香港或台湾。
* 地区：a、b、c三条路线，任选一个。
![09](https://github.com/masonvip/GCP/blob/master/readme.md/09.png?raw=true)
* 机器类型：选择共享核心最小的一个即可。⚠️越小越便宜。
![10](https://github.com/masonvip/GCP/blob/master/readme.md/10.png?raw=true)
* 启动磁盘：默认选择Debian GNU/Linux 9 (stretch)。
* 防火墙：允许 HTTP 流量，允许 HTTPS 流量两项都勾选。
* 点选创建。
![11](https://github.com/masonvip/GCP/blob/master/readme.md/11.png?raw=true)
* 创建好VM实例里会显示IP，复制该实例的「外部IP地址」。
![12](https://github.com/masonvip/GCP/blob/master/readme.md/12.png?raw=true)
* Mac电脑打开「网络实用工具」，将IP粘贴到选框内，点选「Ping」，即可看到数值。一般低于80ms，速度都不错。⚠️如果数值过高建议重新创建实例，直到筛选出Ping值较低的。
* 也可以打开[Ping检测网址](http://ping.chinaz.com/)进行查看数值。
![13](https://github.com/masonvip/GCP/blob/master/readme.md/13.png?raw=true)
---
## 步骤三：搭建路线
* 返回到VM实例。
* 点选SSH或SSH右边三角形，选择「在浏览器窗口中打开」。
![14](https://github.com/masonvip/GCP/blob/master/readme.md/14.png?raw=true)
* 在终端里输入sudo -i
* 回车键
![15](https://github.com/masonvip/GCP/blob/master/readme.md/15.png?raw=true)
* 输入下面代码
>`wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log`
* 会自动加载如下图显示，按回车键。
![16](https://github.com/masonvip/GCP/blob/master/readme.md/16.png?raw=true)
* 选择2，按回车键。
![17](https://github.com/masonvip/GCP/blob/master/readme.md/17.png?raw=true)
* 自定义输入一个密码，按回车键。
![18](https://github.com/masonvip/GCP/blob/master/readme.md/18.png?raw=true)
* 在1-65535之间任意输入数字作为端口号，按回车键。
![19](https://github.com/masonvip/GCP/blob/master/readme.md/19.png?raw=true)
* 按回车键，你也可以选择自己喜欢的加密方式。
![20](https://github.com/masonvip/GCP/blob/master/readme.md/20.png?raw=true)
* 协议按回车键。
![21](https://github.com/masonvip/GCP/blob/master/readme.md/21.png?raw=true)
* 按回车键。
![22](https://github.com/masonvip/GCP/blob/master/readme.md/22.png?raw=true)
* 按任意键，开始搭建。
![23](https://github.com/masonvip/GCP/blob/master/readme.md/23.png?raw=true)
* 耐心等待代码运行，约9分钟。
![24](https://github.com/masonvip/GCP/blob/master/readme.md/24.png?raw=true)
* 完成后终端会显示黑屏，请滚动下鼠标即可看到下图信息。
![25](https://github.com/masonvip/GCP/blob/master/readme.md/25.png?raw=true)
⚠️请复制保存信息，然后关闭终端即可。
