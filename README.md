## 自动抢票回家

#### 运行环境： Python3 + Window7

### 准备工作

1、准备一个12306账号，将乘客信息录入进去

2、下载对应本地Chrome浏览器的chromedriver驱动，下载地址：[https://npm.taobao.org/mirrors/chromedriver/]
    |chromedriver版本|支持的Chrome版本|
    | - | - | 
    |v2.33	|v60-62
    |v2.32	|v59-61
    |v2.31	|v58-60
    |v2.30	|v58-60
    |v2.29	|v56-58
    |v2.28	|v55-57
    |v2.27	|v54-56
    |v2.26	|v53-55
    |v2.25	|v53-55
    |v2.24	|v52-54
    |v2.23	|v51-53
    |v2.22	|v49-52
    |v2.21	|v46-50
    |v2.20	v43-48
    v2.19	v43-47
    v2.18	v43-46
    v2.17	v42-43
    v2.13	v42-45
    v2.15	v40-43
    v2.14	v39-42
    v2.13	v38-41
    v2.12	v36-40
    v2.11	v36-40
    v2.10	v33-36
    v2.9	v31-34
    v2.8	v30-33
    v2.7	v30-33
    v2.6	v29-32
    v2.5	v29-32
    v2.4	v29-32
    找不到对应的，就都下载最新的或最近更新的试试，我的就是这样成的！
    
  3、目的地的cookies
    进入12306查询你需要的出发地=》目的地的车票，按F12进入调试模式，点击查询->Network(如下图)，_jc_save_formStation,_jc_save_toStation即分别为所需出发地、目的地的Cookies
    ![show_place_cookies](https://github.com/sanplit/public/blob/master/images/12306_tickets/show_place_cookies.png)
    
### 使用说明
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
    
