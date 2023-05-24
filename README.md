# SteamCmd
注意！！防火墙必须全部同意！！ 【本编译软件需要30G左右空间哦，下载需要一段时间】
--
使用步骤教程
--
//第一步
把steamcmd.exe放进一个新建文件夹【文件夹随便取名，这里假设命名cs-server】再点击steamcmd.exe

//第二步
等steamcmd.exe自动下载及加载完一切后最下列出现【steam>】的时候就可以开始我们的操作了！

//第三步
在该文件夹【cs-server】内创建名称Server的空文件夹

//第四步
回到cmd内输入 force_install_dir 【dir后面打个空格填入文件Server位置，例如 force_install_dir D:\cs-server\Server】

//第五步
cmd内接着输入 login anonymous 【等待全ok】

//第六步
最后cmd内输入 app_update 740 validate 
【下载全部服务器前置，30G左右哦需要一段时间！】


验证修复教程 
--
需要重新走第四步骤定位Server文件【force_install_dir D:\cs-server\Server】再-第五步骤
重新登陆【login anonymous】后输入【app_update 740 validate】即可。
【一般插件就包含addon，cfg文件，这两个文件直接删了再安装别的插件用的时候会出现错误。

这时候用这个指令验证文件他就会给你补全属于他自己的文件，直接修复不用重新下载30G文件！】


因国服改动需要把登录服务器改成国际服
--
在steam库-csgo属性启动项添加【-worldwide】或者点击国际服登录即可在社区服务-局域网栏找到自己的服务器


启动服务器bat编辑 
--
创建txt文件【server.txt】
编辑内容【srcds -game csgo -console -usercon +game_type 0+game_mode 1 +mapgroup mg_active +map de_dust2 -tickrate 128】
后缀【server.txt】改成【server.bat】就ok！

服务器启动顺序
--
需先打开游戏，再打开bat文件。
如果先打开bat文件steam会显示你已开始游戏，你上不去游戏的！！

必备插件解压位置
--
Addons跟cfg文件放到 D:\cs-server\Server\csgo 内即可

需给予自己steam管理员权限 【拥有权限了才能用全部插件】 附加指令：聊天框输入!admin
--
进入\addons\sourcemod\configs\admins_simple.ini文件txt格式打开

在最下面空区添加 "STEAM_0:0:xxxxxxxx"	"99:z"  注：需要双键号概括你的id跟权限码！

【"STEAM_0:0:xxxxxxxx"】为你的steamID 

查询链接推荐：https://steamid.io/lookup/

复制自己的steam主页URL查询，最上面显示的就是你steamid 

让服务器允许全部插件
--
进入\addons\sourcemod\configs\core.cfg中的内容
"FollowCSGOServerGuidelines" "Yes" 修改成 "No"
可以无视，我帮你们已经改掉了 :D
