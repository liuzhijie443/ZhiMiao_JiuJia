# ZhiMiao_JiuJia
** 推荐：https://github.com/SunshineList/jiujia
** 这个老哥的成品软件可以自动获取PID
### 2022年8月6日
**pid已由原来的纯数字固定id变成了随机字母id，并且未开放预约的疫苗无法获取PID。**
**原py程序无法直接使用，大家根据需要自行修改吧**
![48_9HP(@}QEPPPMO @S22_V](https://user-images.githubusercontent.com/25584923/183229846-d0eb0de2-8250-41c1-9e58-473fac066065.png)
### 目标
[2022-04-17编写]

[2022-06-20可用]

一个简单的九价抢购python脚本，用于抢购知苗易约疫苗，请勿用于盈利，免费提供，仅供学习。

***
### 使用方法

**参数配置：**
jiujia.ini
```
[jiujia]
cookie=
wait_speed=1000
buy_speed=1000
p_id=54
id=492
# cookie 小程序抓包cookie
# wait_speed 等待开始刷新时间，单位毫秒
# buy_speed 抢购间隔，单位毫秒
# p_id 1是九价（九价人乳头瘤病毒疫苗），2是四价（四价人乳头瘤病毒疫苗），3是二价（二价人乳头瘤病毒疫苗-进口），54是二价（二价人乳头瘤病毒疫苗(大肠杆菌)），其他疫苗请抓包获取。不同医院小程序内置的ID可能不一样，具体请抓包查看。
# id 门诊医院id
```
***
**cookie配置方法：**</br>

使用fiddler抓包知苗易约小程序：https://blog.csdn.net/A_Liucky_Girl/article/details/124534772

fiddler抓不到PC端微信小程序的包：https://www.csdn.net/tags/NtzaggxsNTA1MjgtYmxvZwO0O0OO0O0O.html

点击门诊进入疫苗预约

cloud.cn2030.com 开头的就是知苗易约的包

```
ASP.NET_SessionId=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpYXQiOjE2NTU3MDE2NjAuMDg2ODAyNywiZXhwIjoxNjU1NzA1MjYwLjA4NjgwMjcsInN1YiI6IllOVy5WSVAiLCJqdGkiOiIyMDIyMDYyMDEzMDc0MCIsInZhbCI6InJ2RmZBUUlBQUFBUU1EUXdZVFptWXpnek4yRm1OR0V5Tnh4dmNYSTFielZNY0VsRWRFMXFZMnR6UzA1ckxXTkdNelpOTldKekFCeHZcclxuVlRJMldIUTJVRlZNTVU5TlNFMTVlV1JOVDFOcGRtSnNTalJSRFRFeE15NHhOaTQwT0M0eU5Ea0FBQUFBQUFBQSJ9.mcqQXSdBADjCbXrmRgvWN7bj55tCNPXomPwf7rwsFRU
```
抓包后等号后面ey到结尾这一段就是cookie
***
**门诊id配置方法：**</br>

点击门诊进入疫苗预约

包列表中的：https://cloud.cn2030.com/sc/wx/HandlerSubscribe.ashx?act=CustomerProduct&id=492&lat=22.83393&lng=108.31343

id=492就是门诊id
![image](https://user-images.githubusercontent.com/25584923/174531087-545f7d7c-8a15-4ead-9088-748d4cf193d4.png)
***
**疫苗产品p_id配置方法：**</br>

1是九价（九价人乳头瘤病毒疫苗），2是四价（四价人乳头瘤病毒疫苗），3是二价（二价人乳头瘤病毒疫苗-进口），54是二价（二价人乳头瘤病毒疫苗(大肠杆菌)），其他疫苗请抓包获取。
不同医院小程序内置的ID可能不一样，具体请抓包查看。

上面抓包信息组合起来配置文件内容就是下面这样子：
```
[jiujia]
cookie=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpYXQiOjE2NTU3MDE2NjAuMDg2ODAyNywiZXhwIjoxNjU1NzA1MjYwLjA4NjgwMjcsInN1YiI6IllOVy5WSVAiLCJqdGkiOiIyMDIyMDYyMDEzMDc0MCIsInZhbCI6InJ2RmZBUUlBQUFBUU1EUXdZVFptWXpnek4yRm1OR0V5Tnh4dmNYSTFielZNY0VsRWRFMXFZMnR6UzA1ckxXTkdNelpOTldKekFCeHZcclxuVlRJMldIUTJVRlZNTVU5TlNFMTVlV1JOVDFOcGRtSnNTalJSRFRFeE15NHhOaTQwT0M0eU5Ea0FBQUFBQUFBQSJ9.mcqQXSdBADjCbXrmRgvWN7bj55tCNPXomPwf7rwsFRU
wait_speed=1000
buy_speed=1000
p_id=1
id=492
```
祝大家抢购成功
***
### 注意事项
准点前两分钟打开</br>
测试预约成功后及时取消预约，不然没办法预约第二次。</br>
抢购前先试一下抢2价，需要提前在我的-个人信息-填写好姓名性别身份证号</br>
每个ip有自己的cookie，不可共享Cookie。</br>
没有多线程，也不要多开</br>
cookie有效期一个小时</br>
如果需要提高成功率请选择多开电脑和多开账号，且一台电脑对应一个账号</br>
感谢刘欣大神：[https://www.liuxincode.cn/](https://www.liuxincode.cn/)

![image](https://user-images.githubusercontent.com/25584923/174532767-b7c11363-a01c-4a06-a371-eeb6496ddd4f.png)


![image](https://user-images.githubusercontent.com/25584923/174532654-95c33b79-c28b-4589-8876-35c7fbdaa53a.png)
