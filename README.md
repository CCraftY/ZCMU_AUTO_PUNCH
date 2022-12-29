 # ZCMU自动健康打卡脚本 ![](https://img.shields.io/badge/%E6%89%93%E5%8D%A1-ZCMU-brightgreen) [![ZCMU Auto Punch](https://github.com/CCraftY/ZCMU_AUTO_PUNCH/actions/workflows/main.yml/badge.svg)](https://github.com/CCraftY/ZCMU_AUTO_PUNCH/actions/workflows/main.yml)
~~低调使用，建议私有库运行~~
 > 浙江中医药大学自动健康打卡
## 2022/12/26 表格内容变化，跟进更新，尚未测试
## 2022/12/27 新增secret，待测试
## 2022/12/28 
 + 新增 `PHONE` `ADDR` `ADDRDE` `PARNAME` `PARPHONE` 环境变量
 + 完善所有填报项，解决国外IP自动填充无效
 + 理论上可用


 ## ❗❗❗请遵守学校防疫政策，出现异常请关闭脚本手动进行打卡❗❗❗
 ## ⚠⚠⚠   仅供学习交流使用，请于下载后24小时内删除   ⚠⚠⚠

 ## 使用方法

 ### 配置

 1. fork 该仓库

 2. 点击仓库中的 `Setting` 标签，选中 `Secrets`

 3. 选中 `New repository secret` 新建环境变量

 | Name          | Value            | Desc                                                       |
 | ------------- | ---------------- | ---------------------------------------------------------- |
 | USERNAME     | 学号             |   支持多用户登录，以','分隔 |
 | PASSWORD      | 统一身份认证密码 |   https://ias.zcmu.edu.cn/cas/login |
 | DD_BOT_TOKEN（选填） | 推送服务     | 钉钉推送(DD_BOT_TOKEN和DD_BOT_SECRET两者必需)官方文档 ,只需https://oapi.dingtalk.com/robot/send?access_token=XXX 等于=符号后面的XXX即可 |
 | DD_BOT_SECRET(选填)  |推送服务      | (DD_BOT_TOKEN和DD_BOT_SECRET两者必需) ,密钥，机器人安全设置页面，加签一栏下面显示的SEC开头的SECXXXXXXXXXX等字符 , 注:钉钉机器人安全设置只需勾选加签即可，其他选项不要勾选|
 |TOKEN(选填) |pushplustoken|需填写主用户pushplustoken(任意字符，首位)以','分隔。例现有2位用户:TOKEN=任意字符,第二位用户plusplustoken|
 |LOCATION      |定位              | 须按规范填写，后果自负|
 |ACCOMMODATION|开学后居住地||

 
### 推送说明
 > 若单用户使用，可根据notify.py内的推送配置自行选择推送渠道。请确保在workflow中添加相应代码。

 > 自用 ✔ dingdingbot，可以自行修改代码
 > 主用户使用DingDingBot，其余用户使用[pushplus](http://www.pushplus.plus)
 
 > 主用户监测所有用户打卡情况，其余用户各自分别推送各自的情况
  
 > 配置方法演示

 ![](./assets/create_secret.png)

 ![](./assets/new.png)

 ### 使用

 **程序将在每天 5:30(UTC 21:30) 自动运行，也可以在 `Aciton` 中手动触发运行。**

 **三个月左右 GitHub Action 会暂停自动运行，需要手动重新启动！**

 ![](./assets/run.png)

 ### 运行成功示例
 ![](./assets/success.png)

 ## 鸣谢
 [浙江理工大学自动健康申报（新版）](https://github.com/typenoob/zstu_report)(大部分代码，打卡系统为杭州某多)
  
 [HDU-AutoPunch 杭州电子科技大学自动健康打卡脚本](https://github.com/YeQiuO/HDU_AUTO_PUNCH)(Github Action环境)

 [浙大城市学院健康打卡脚本](https://github.com/chansyawn/zucc-auto-check)

 [杭州电子科技大学自动健康打卡脚本](https://github.com/Eanya-Tonic/HDU-Health_checkin)

 [zkeq 自用API](https://github.com/zkeq/icodeq-api)
 


# TO DO
> 继续借鉴各位大佬的经验，用仅有的能力更新

* Docker环境补齐
* 简化代码，使用循环选择元素
* ✅多用户登录 
* ✅多用户推送


# Coding with ❤
