## 自动抢票回家

#### 测试环境： Python3 + Window7

### 准备工作

1、准备一个12306账号，将乘客信息录入进去

2、下载对应本地Chrome浏览器的chromedriver驱动，下载地址：[https://npm.taobao.org/mirrors/chromedriver/]
   对应的自行百度吧，找不到对应的，就都下载最新的或最近更新的试试，我的就是这样成的！
    
  3、目的地的cookies
    进入12306查询你需要的出发地=》目的地的车票，按F12进入调试模式，点击查询->Network->点击跳转的链接即可查看到Cookies，_jc_save_formStation,_jc_save_toStation即分别为所需出发地、目的地的Cookies
    
### 仅需修改如下内容
```
#用户名，密码，如1
username = u"username"
passwd = u"passwd"
# cookies值得自己去找, 下面两个分别是深圳, 武昌,如3
starts = u"%u6DF1%u5733%2CSZQ"
ends = u"%u6B66%u660C%2CWCN"
# 时间格式2018-02-11，自由选择
dtime = u"2018-02-11"
# 车次，选择第几趟，0则从上之下依次点击
order = 0
###乘客名，可多人，如[u"user1",u"user2"]
users = [u"user1"]
##席位
xb = u"二等座"
pz=u"成人票"
```
    
浏览器提示不安全，需要开发模式等等，都是因为浏览器与驱动不对应，赶快换一个试试吧~

突然觉得...这些都是多余的

### 运行操作
  方式一：window下双击tickets.py
  方式二：进入当前目录下，命令 >python tickets.py
  
