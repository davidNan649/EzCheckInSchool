# EzCheckInSchool
最简单的完美校园自动健康打卡，基于Github Actions免服务器运行。

- 仅需学号姓名🎫
- 随机校内经纬度🗺️
- 打卡结果微信推送💬
- 随机温度(36.2℃-36.4℃)🌡
- 校内打卡三次:06:00,12:30,21:00🕑

**Github Actions定时任务可能出现几分钟的误差，
可以迁移到腾讯云云函数（现在免费），修改`input()`为对应字符串后设置定时触发器即可**

**首次开启若不在打卡时间将会重打早间卡作为测试**

## 更新日志
2020.9.13 20:45 更新最简单免抓包使用方法及代码

2020.9.12 7:00 修复时间判断代码，现在将正常打卡三次

## 使用方法
首先，点击右上角Star并Fork

接下来你需要把学号和姓名设为Secert

你Fork的项目->Settings->Secert->New Secert

Name:STUNO Value:你的学号 如`201812340101`

Name:USERNAME Value:你的姓名 如`张三`

Name:SCKEY Value:Server酱调用URL 使用前请绑定[Server酱](http://sc.ftqq.com/)，如` http://sc.ftqq.com/abcdefghigklmnopqrstuvwxyz.send`

以上步骤完成后

Settings->Action->I understand... 开启Actions

回到项目主页，修改README.md 随便加几个空格即可

设置完成打卡后打卡时间内会每天自动打卡三次，第一次使用请观察效果。

**注意：本项目默认学校为河南工业大学，其他学校请自行抓打卡提交的包（POST `https://reportedh5.17wanxiao.com/sass/api/epmpics` JSON）修改main.py代码。**

## 友情链接

https://github.com/YooKing/HAUT_autoCheck - 初版Python代码参考

https://github.com/LovelyWhite/Haut-AutoCheckin - iPhone捷径版

