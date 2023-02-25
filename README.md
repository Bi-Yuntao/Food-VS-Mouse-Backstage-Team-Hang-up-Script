# 美食大战老鼠后台组队挂机脚本
通过按键精灵实现双人组队后台挂机脚本，设置合理的参数可以挂机三岛。

## Version1.00-----------------------------------------
组好双人房间后再开启脚本  
枫叶登录请使用内置flash模式  
## Version2.00-----------------------------------------
### 更新：
局内自动放置卡片，仅支持预设5种卡

### 注意：
预设卡片的位置内容务必遵循格式，否则脚本无法正常执行，格式如下：  
用英文分号";"分隔每个位置，用英文逗号","分隔x和y坐标。  
例如预设海星放置在第2行(从上往下)第7列(从左往右)，第6行第7列  
则输入框内填入：2,7;6,7
## Version3.00-----------------------------------------
### 更新：
1. 2p可以作为1p的辅助，放置卡片；  
2. 优化卡片放置策略的调度，具体调度如下：  
    1. 角色放置后立即开始放置2p卡一。可放小火炉等作为生产火苗的辅助
    2. 0.5s后开始放置2p卡二。可放木盘子、苏打气泡等0耗辅助卡
    3. 15s后开始放置1p卡一，同时开始放置2p卡三。可选择放置瓜皮、扑克牌罩等卡，
在初始火苗或初始生产卡充足的情况下可选择直接放置输出卡
    4. 31s后开始放置1p卡二，同时开始放置2p卡四。可选择放置输出卡
    5. 4s后开始放置1p卡三，同时开始放置2p卡五。可选择放置输出卡
    6. 0.5s后开始放置1p卡四。可选择放置输出卡
    7. 0.5s后开始放置1p卡五。可选择放置输出卡
3. 丰富卡片CD选项：
    7s(普通卡:海星等;上取整有技能木盘子等)  
    3s(7技能棉花糖;8技能木盘子)  
    4s(7技能木盘子)  
    15s(7技能瓜皮)  
    25s(扑克牌罩等)  
    30s(0技能瓜皮,6技能章鱼烧;上取整扑克牌罩等)  
    40s(狮子座等)  
    50s(0技能章鱼烧)  
### 注意：
自定义的卡片放置策略务必顺应该脚本的卡片放置调度；  
同时填写时注意区分先后顺序，避免木盘子还未放置，而1p已经开始放置输出卡，导致无法正常放置卡片
## Version4.00-----------------------------------------
### 更新：
1. 新增单人挂机功能，单人挂机可自定义不同卡片间延时，且最大支持8种卡的配置；  
2. 增加脚本结束提醒  
### 问题修复：
自动收集火苗时，火苗飘过鼠标点击位置会导致本次点击失效。可能会使点击“继续挑战”操作失效，最终造成脚本无法正常工作
### 注意：
单人挂机请保证两张卡片的放置间隔延时合理。如果达到同步，会同时从卡槽取卡A和卡B，使得取出的卡A又被放回卡槽，导致两个卡的放卡操作都失效    
## Version4.01-----------------------------------------
### 更新：
1. 优化窗口句柄获取方式：点击"获取"按钮后，再次点击目标窗口即可。突破登录方式限制
2. 增加系统缩放倍率的填写，无需修改自己的Windows设置。查看当前win系统缩放比例：Windows设置->系统->屏幕->缩放与布局
## Version5.00-----------------------------------------
### 更新：
增加卡片放置策略配置的保存，现在可以更快切换战术了
### 注意：
配置方案描述中不要使用换行，否则第一行后所有描述将会丢失(懂ini文件格式的可以自己通过编辑文件来修复)
## Version6.00-----------------------------------------
### 更新：
1. 增加新功能——悬赏三连。仅支持组队双开；
2. 增加新功能——遗迹；
3. 增加新功能——跨服；
4. 增加新功能——一键日常。点击开始后自动执行所有勾选的功能，请先在对应功能页面内设置好相关参数再开始；
5. 更新uservar.ini文件，通过直接修改该文件，使得每次运行exe程序时，已经配置好符合自己情况的参数；
6. 优化默认翻牌，现在可以翻多张牌，翻牌编号用英文分号分隔；
7. 优化卡片放置策略填写，可通过占位符"-"表示本次不放卡，以解决两种卡冲突放置的问题。    填写示例：2,7;6,7;4,7;-;5,7;-;3,7
### 注意：
1. 使用悬赏三连、遗迹和跨服之前，确保当前界面能够点击到世界地图；
2. 悬赏三连和遗迹的“2P昵称路径”指在组队房间内邀请界面中的昵称截图图片路径，必须用抓抓截图，同时在截图包含完整昵称的前提下尽量小，否则无法识别；
3. 跨服的“1P昵称路径”指在跨服房间列表中的昵称截图图片路径，必须用抓抓截图，同时在截图包含完整昵称的前提下尽量小，否则无法识别；
4. uservar.ini文件必须与exe程序放在同一文件夹中
## Version6.01-----------------------------------------
### 更新：
1. 为组队模式增加自定义卡片前置延时，1P和2P独立设置；
2. 优化循环检测进入游戏，现在能自动一直点击"开始"(房主)或"准备"(房客)；
3. 增加检测游戏进度的异常事件提示，若超过十分钟仍未检测到继续挑战或结算翻牌，则会弹出对话框提示
## Version6.02-----------------------------------------
### 更新：
1. 增加新功能——会长任务。任务3仅支持双开；
2. 增加新功能——情侣任务；仅支持组队双开；
3. 增加新功能——魔塔；
4. 更新新功能对应的uservar.ini文件。
### 注意事项：
会长任务和情侣任务的文件夹结构必须严格保持不变，且任务截图命名方式也必须遵循格式：    
会长任务    
&emsp;┣ 任务1    
&emsp;&emsp;┣ 美味岛-神殿-继续挑战.bmp    
&emsp;&emsp;┕ 火山岛-芥末小屋日-领取奖励.bmp    
&emsp;┣ 任务2    
&emsp;&emsp;┣ 美味岛-咖喱岛夜-领取奖励.bmp    
&emsp;&emsp;┕ 火山岛-芥末小屋夜-继续挑战.bmp    
&emsp;┕ 任务3    
&emsp;&emsp;┣ 美味岛-可可岛夜-领取奖励.bmp    
&emsp;&emsp;┕ 火山遗迹-果仁瀑布-无二阶段.bmp    
截止目前并未收集完所有任务，须自行截图新任务
## Version6.03-----------------------------------------
### 更新：
增加卡片位置填写占位符："1"、"10"，分别表示本次放卡操作推迟1s、10s
### 问题修复：
1. 修复卡片前置延时超过某五位数时无效的BUG(Int溢出)；
2. 解决1P、2P悬赏图标位置不一的特殊情况(两个号悬赏图标位置一致的请忽略此条内容)：请新建且确保2P界面的悬赏活动图标截图文件名符合以下格式——若1P的图标截图命名为<悬赏活动图标.bpm>，则2P应为<悬赏活动图标_2p.bpm>，且二者存储于同一路径
