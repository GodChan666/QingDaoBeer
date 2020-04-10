# QingDaoBeer
青岛啤酒撸流量，领取青岛啤酒流量和趣味天天摇（抽奖挂机）
## 推广
VPS： [RackNerd](https://my.racknerd.com/aff.php?aff=376)
## 视频演示
哔哩哔哩：
1. [效果演示](https://www.bilibili.com/video/BV1JZ4y1x7SV)
2. [百度ai获取](https://www.bilibili.com/video/BV18K4y1r7WR)
3.[搭建实战](https://www.bilibili.com/video/BV1NZ4y1x7pC)
4. [设置域名访问](https://www.bilibili.com/video/BV14t4y1U7op)
	
	
	

### 青岛啤酒撸流量，领取青岛啤酒流量和趣味天天摇（抽奖挂机）
本文中的源代码取自[kukume](https://github.com/kukume/unicom).
## 操作
- 下载代码文件，修改application.yml，使用filezilla上传（/root/godchan666）
- 使用Xshell 6链接上你自己的VPS,输入以下代码，搭建环境
- 访问网站--成功
>你不一定必须要照着我的来

## 环境
	JDK1.8(可以装tomcat替代，因为会自带)
	MySQL（如使用mysql）
		新建名为：QingDaoBeer 
		账号	：admin
		密码	：123456
	nginx/apache（如需域名访问）
>>		MySQL数据库所给文件默认为此，你也可以自行更改
## 宝塔面板

	#centos
			yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh
		美国节点：
			yum install -y wget && wget -O install.sh http://128.1.164.196:5880/install/install_6.0.sh && sh install.sh
	#ubuntu
		wget -O install.sh http://download.bt.cn/install/install-ubuntu_6.0.sh && sudo bash install.sh
	#debian
		wget -O install.sh http://download.bt.cn/install/install-ubuntu_6.0.sh && bash install.sh
## api安装
需要安装tesseract-ocr      https://digi.bib.uni-mannheim.de/tesseract/

		#如是debian
				apt-get install tesseract-ocr
		#如是centos
				yum install tesseract
下载py，https://u.iheit.com/index.py
			或者
							
			wget https://u.iheit.com/index.py
安装python

		#如是debian
				apt-get install python3
				apt-get install python3-pip
		#如是centos
			yum install python3
			yum install python3-pip
				检查Python3及pip3是否正常可用：
					# python3 -V
					# pip3 -V
安装依赖

	pip3 install requests
	pip3 install pytesseract
	pip3 install flask
	pip3 install Pillow
后台执行
>安装screen

	>CentOS/RedHat/Fedora
						yum -y install screen 
	Ubuntu/Debian
						apt-get -y install screen
#
	python3 index.py
		#或者使用screen			
	screen -dmS qdocr python3 index.py
默认地址为http://localhost:5000/getCode 然后更改配置文件中的api地址（稍后更新）
api源码大部分来自https://github.com/teenyda/qingdao


## 百度AI
		直接访问：https://ai.baidu.com/tech/ocr/general
## 安装
编译包下载： https://github.com/GodChan666/QingDaoBeer/releases/
百度云：链接:https://pan.baidu.com/s/1uCpncBZn_T0zC9kX-VoGVQ 提取码:cveb 

	wget https://github.com/GodChan666/QingDaoBeer/releases/download/5.0/unicom.jar
		
 更改application.yml中的配置
>可以在本地完成，然后通过filezilla上传，并且推荐没基础的人使用这种方法

	然后把unicom.jar放到文件夹下，比如/root/godchan666文件下
运行

	cd /root/godchan666
	java -jar unicom.jar
	如需后台运行，可以使用screen

	cd /root/godchan666
	screen -dmS unicom java -jar unicom.jar
运行之后打开http://IP地址:8099即可

如果需要域名访问，在宝塔中添加反向代理，代理地址设置为http://localhost:8099即可

##特别注意
>是不是照着搭建结果还是运行不了啊？
>>如果是像centos7这样的还需要关闭防火墙
#
查看防火墙状态

	firewall-cmd --state


停止firewall

	systemctl stop firewalld.service

禁止firewall开机启动

	systemctl disable firewalld.service 

