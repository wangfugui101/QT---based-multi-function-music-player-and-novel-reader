# QT - based multi-function music player and novel reader
基于QT的多功能音乐播放与小说阅读器
2022年7月		基于爬虫的小说线上阅读器以及音乐播放器项目
技术栈：C++，C++STL，爬虫 ，网络编程，MYSQL，mplayer，linux，QT
项目简介：该项目致力于在阅读小说时播放背景音乐。
1.登录界面
1.1 登录按钮--当账号密码与数据库内所存放的账号密码不匹配的时候，会弹出警告“账号或密码错误”的弹窗，要重新输入账号与密码来进行登录；当账号密码与数据库内所存放的账号密码相匹配的时候，会弹出登录成功的弹窗，并跳转至主界面。
1.2 注册按钮--跳转至注册界面，并将登录界面的输入框内容清空。
1.3 事件过滤器--当点击账户或者密码输入框时，会触发事件，弹出自定义的软键盘，其中软键盘里面的按钮也是通过自定义控件来实现点击效果。
2.注册界面
功能上跟登录界面一样，拥有注册和取消功能。在注册账户时当数据库里面有相同的账户时，会弹出“存在相同账户”的弹窗。取消按钮就是返回至登录界面，并销毁注册界面
3.音乐播放界面
在界面的左上角显示了当前用户名，以及当前启动时间，并通过定时器事件，不停更新时间达到时间跳动效果。可以界面的背景、最小化、以及注销账号功能。
3.1音乐播放
只支持本地音乐播放，当点击添加按钮完成功能时，会创建一个进程来播放音乐，可在左边列表中显示当前音乐名。可支持音乐名查找，当未查询到音乐名时，会弹出“未找到”弹窗，当查询成功时，会自动选中该音乐名。当音乐播放时，在界面中会滚动显示音乐名，并且界面的下方会有进度条跟随音乐播放的进度。在进度条下方，会有音量调节，来达到自己控制音乐的声音。可以自由切换音乐，伴有上一首和下一首的功能按钮，也可以选中音乐名进行删除，也有清空音乐列表的功能。
3.2 小说搜索
小说是线上阅读，通过爬虫获取小说列表、小说目录以及小说内容。在播放界面下，可通过小说名或者小
说作者名，进行不完全匹配，当点击搜索小说按钮，会在下方显示与输入的关键字所对应的小说列表。基本支持所有的目前小说的爬取与阅读。当选择想要阅读的小说名后，点击目录按钮，跳转至小说阅读界面。
3.小说阅读界面
在此界面中，左边是该小说的目录列表，当选中想要阅读的章节后，双击，在右边可显示当前选择章节的小说内容。
技术难点：软键盘的信息的传递，mplayer的指令使用，正确获取想要的网页源码片段，爬取正确的链接和小说内容，正则表达式的正确书写以及贪心匹配和非贪心匹配。
自我评价：该项目是一个基于http协议的爬取，并未能实现https协议的爬取，很可惜。通过该项目，对网络爬取资源，程序编写框架，QT软件的使用都有了一定的进步。
