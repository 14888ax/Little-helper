# ！！！注意该项目为复制二改操作跟繁琐但可以自定义更加安全如要懒人操作请跳转https://github.com/Tigaisgzy/Little-helper ！！！


**配置一次，就可以每天自动打卡了！**
> 
> **[贴吧签到](#贴吧签到)**
> 
> **[微博超话签到](#微博超话签到)**

# 提示
**如果某个自动打卡不需要，只需要在仓库的workflows文件夹下，将不需要的yaml文件删除即可**

# 贴吧签到

1. 先fork仓库
2. 在仓库的Settings --> Secrets中配置变量
> BDUSS_BFESS 这两个去网页版登录后在cookie里找
> STOKEN      好像能用挺久的一次
3. 配置定时任务
4. 配置成功后，在仓库的Actions中查看运行情况

# 微博超话签到  
   自动获取超话列表，自动签到
   使用方法与贴吧签到相同，只需要再添加SUB_TOKEN即可
> SUB_TOKEN 只需要这个cookie，有效期一年


# 一共设置的变量有
1. SUB_TOKEN （从微博cookies获取）
2. STOKEN （从贴吧cookies获取）
3. BDUSS_BFESS （从贴吧cookies获取）
4. EMAIL_ADDRESS （用于完成后邮件通知的目标）
5. HOST_EMAIL_ADDRESS （设置发送签到完成的邮箱地址）
6. HOST_EMAIL_PASSWORD （设置发送签到完成的邮箱的密码）


# 关于设置HOST EMAIL
>以qq邮箱为例
1. 登录qq邮箱网页版找到右上角设置
2. 在安全一栏中找到安全设置
3. 找到POP3/IMAP/SMTP/Exchange/CardDAV 服务开启服务
4. 复制授权码在环境变量里面设置HOST_EMAIL_PASSWORD

# 关于安全方面
1. 众所周知，复制了仓库原仓库的主人是可以看到你的更改，但是无法发现你的环境机密变量。只要将你的变量设置在机密变量里面就不会被原主人发现
2. 关于位置问题。由于github上自动设置的服务器在美国所以你签到的地址就是在美国。请注意异地登录等问题

# 我无法正确签到如何排除错误
1. 在action中找到你无法签到的对应任务
2. 点开work中的build查找第五行及其以下是否有什么报错必要时可以自行重新手动执行任务
