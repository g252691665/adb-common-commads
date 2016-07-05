#### 常用adb命令详解
***
1. 显示系统中所有的Android平台

	android list targets
2. 显示系统中全部	AVD(已经创建的模拟器)
	
	android list avd
3. 创建AVD(模拟器)
	
	android create avd --name(或者-n) 名称 --traget(或者-t) 平台的编号
4. 启动模拟器
	
	emulator -avd 名称 -sdcard sd卡的image(默认为<system>/sdcard.img) -skin 名称
5. 删除模拟器

	android delete avd --name 名称
6. 创建SDCard
	
	mksdcard 1024M(大小) sd卡的image(默认为<system>/sdcard.img)
7. 启动ddms

	ddms
8. 显示当前运行的全部模拟器

	adb devices
9. 多某一模拟器执行命令

	adb -s 模拟器编号 命令
10. 强制安装应用程序

	adb install -r 应用程序.apk
11. 获取模拟器中的文件
	
	adb pull <remote> <local>
12. 向模拟器中写文件
	
	adb push <local> <remote>
13. 进入模拟器的shell模式
	
	adb shell
14. 启动sdk manager

	android
15. 卸载应用程序
	
	adb uninstall apk的包名
16. 查看adb命令帮助信息

	adb help
17. 在命令行中查看LOG信息

	adb logcat
18. 删除系统应用
	
	adb remount(重新挂载系统分区，使得系统分区重新读写)
	adb shell
	cd system/app
	rm *.apk
19. 获取管理员权限
	
	adb shell am start -n 包名/包名+类名
20. 端口映射

	adb foorward tcp:主机端口号 tcp:模拟器端口号
21. 访问数据库sqlite3
	
	adb shell
	sqlite3 数据库名
