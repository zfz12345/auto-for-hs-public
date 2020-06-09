# auto-for-hs-public

> Latest Version: 0.2 / Date 20200609

auto for hs public.

> 图片详见 PDF版

---
### 相关附件
1.	战网即炉石程序. (官方下载)
2.	Win10以上系统. （否则hb会闪退）
3.	HB 炉石兄弟. (自行寻找)
4.	RunAsDate. (自行下载)
5.	AutoForHB程序.

---
### 相关文件
1.	autoforhbform.exe 应用文件.
2.	autoforhb.cfg 中控的相关设置文件(有部分冗余参数待删除).
3.	autoforhbform.exe.config / autoforhbform.pdb 系统生成文件.
4.	autoforhb-users.cfg 用户信息相关参数-需要手动设置.
5.	autohb.log 日志文件.
6.	autoforhb-userbattlestatic.db 用户赢取胜场/输场/投降 记录.
7.	autoforhb-userbattlestatic.db.bak 历史用户赢场/输场/投降 记录.

 
---------

### 相关设置
1.	autoforhbform.exe 界面设置.

* 从上到下分别为: 战网路径地址/RunAsDate地址/HearthBuddy地址. 
* 其次为 炉石战网启动延迟时间/炉石启动等待时间/兄弟启动等待时间.（以上3个参数根据自己的电脑响应速度决定.）
* 单用户模式/多用户模式
* 直接启动/RunAsDate启动

2.	autoforhbform.exe – 加密工具

 用于加密用户相关信息. 之后有用.

3.	autoforhb-users.cfg 用户信息配置.(暂无界面配置)

`0|hello3|hello3@163.com|EAAAAHd6DoBRyjl8pG4UfOsBm5gtoZcfmiz7gwjI9fRiZWpR|00:01-20:00|false`

从左到右依次为:
*	ID (第二个用户从1开始)
*	用户别名-打Log时, 便于识别.
*	账户
*	密码(使用上方加密工具加密)
*	运行时间 (多时间段 使用”;”分隔)(时间必须为00:00-23:59内数值) (特别注意 24:00 会造成转换错误, 请使用”00:00”进行替换)
*	是否赢得30胜结束.(注意 请使用兄弟原生插件 原理是读取Settings\Default\ Stats.json 内的数字进行判断胜场数目的. 如果不需要可以直接赋值为false.)

4.	RunAsDate相关设置

*	炉石兄弟运行地址.
*	时间.（有程序通过加壳导致 需要更改时间.）(0516可以设置时间0518解决)
*	--autostart --config:Default 兄弟开启后直接启动.
 
5.	战网设置(单用户/多用户模式)
 
* 单用户模式: 保证战网打开后, 可以直接启动即可.
* 多用户模式: 请不要勾选保持登录状态. 并且地址选择为中国地区. 且默认登录时, 光标处于第二行.（缓存一个用户）
* 不论单用户模式还是多用户模式. 都要配置`autoforhb-users.cfg`文件. 单用户时, 其账户信息可以随便修改.(因为不需要模拟登陆)


6.	炉石相关

炉石请不要选择全屏状态. 尽量选择窗口模式.

7.	炉石兄弟相关

炉石兄弟. 请提前选择好相对应的模式和卡组.

---------
### Q&A

1.	如果发生报错怎么办?

建议提交到Github的Issue.

2.	更换地址后报错.

建议检查autoforhub.cfg文件. 查看是否有多余的字符串. 已知BUG.

3.	我使用远程服务器模式. 无法自动登录账户怎么办.

建议使用脚本.` EnableCloseRDP.bat`

```
@%windir%\System32\tscon.exe 0 /dest:console
@%windir%\System32\tscon.exe 1 /dest:console
@%windir%\System32\tscon.exe 2 /dest:console

set /p input=请输入字符串:
```

4.	炉石兄弟的版本有什么要求么.
可以使用RunAsDate自动启动直接打开. 无额外弹窗.
