# aliyun-change-eip
阿里云自动更换EIP脚本

# 说明
1.下载 change_eip.py、config.py、eip.py、instance.py 这4个文件到服务器中，不能下载到需要更换EIP的那台阿里云服务器上，因为解绑EIP后会导致这台服务器没有网络，后面的脚本就没办法继续执行下去了。

# 安装
1.安装Pythone 和 pip
//Debian/Ubuntu
apt-get update && apt-get install python python-dev python-pip
3.安装阿里云SDK
pip install aliyun-python-sdk-ecs

# 主要修改下面这4个参数：
access_id='你的阿里云AccessKey ID'
access_key_secret='你的阿里云AccessKey Secret'
ecs_vpc_id= 'ECS_ID 服务器ID'
ecs_regionid='ECS 服务器所在区域'
#服务器区域示例：香港写 cn-hongkong、新加坡写 ap-southeast-1 。
#更多区域：https://help.aliyun.com/document_detail/40654.html?spm=a2c1g.8271268.10000.5.1390df25tgiNPE

使用方式：python change_eip.py

