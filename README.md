# HoshinoAuthorizeSystem
用于HoshinoV2的授权系统

当前授权系统仅能管理用咖啡佬的服务层的功能，不能管理通过MiraiNative加载的插件

下载后覆盖原来的hoshino文件夹，然后安装requirements.txt中的依赖就行了

>pip install -r ./requirements.txt

支持yobot缝合板管理,将nonebot_plugin.py替换yobot/src/client下的文件即可

网页端使用方法

1.从<https://github.com/wdvxdr1123/pcr-auth-vue/releases>下载编译好的前端

2.将前端放入auth/vue文件夹中

3.按照注释，修改__init__.py和web_server.py

4.打开机器人公网访问

### 使用方法
**<>内参数为必填 []内参数为选填，不填的话会自动获取当前群号**

**SU指令**
- 生成卡密 <时长>*<数量>
- 授权 <群号>±<时长>
- 转移授权 <旧群号>*<新群号>
- 退群 <群号>
- 卡密列表
- 授权列表
- 授权状态

**一般通过群员指令**
- 充值 <卡密>*[群号]
- 检验卡密 <卡密>

### 火龙的话
- 触发器用的都是on_command，支持群聊&私聊使用，但是不能像on_prefix那样愉快的去掉空格了
- Mirai暂时无法真实退群，但是Bot会完全忽略已经执行退群的群，差不多也等于退群了，想要充值的话还得手动踢了重新拉进群才行。
- 到期提醒部分没碰，先歇逼了。

### 功能列表(含网页端)
- [x] 查询卡密列表分页
- [x] 批量修改时长
- [x] 批量添加卡密
- [x] 批量删除卡密
- [x] 导出卡密
- [x] 加群自动接受(拒绝)
- [x] 网页群组管理
- [x] 精简封装代码
- [x] 到期提醒
- [x] 手动到期提醒
- [ ] 退群提醒

特别感谢:[xhl6666](https://github.com/xhl6666)
