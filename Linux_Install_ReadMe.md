### 1. 系统环境：
	1.1 ubuntu16.04.2 X64
	1.2 更新显卡驱动（系统设置-软件和更新-附加驱动）
	    查看/usr/lib 及其子目录中是否已安装libX11.so 库，如
	1.3 安装qt 5.6.2 库 ，并设置 Qt5.6.2/5.6/gcc_64/lib 目录到LD_LIBRARY_PATH 变量下
	    拷贝： libfcitxplatforminputcontextplugin.so 到Qt5.6.2/5.6/gcc_64/plugins/platforminputcontexts/ 目录
	× 1.4 如需配置本地服务，安装nodejs(配置本地服务，建议源码包编译8.*及以上版本)
	1.5 拷贝 libcef.so 至/usr/lib 目录

### 2. 运行：

	2.1 保证work_dir目录和iexplorer目录为并列目录。
	2.2 在本机或网络上搭建服务（对应gvmldist文件夹资源目录），默认地址：http://127.0.0.1/newTest/index.html
		cd (gvmldist_dir) 
		npm start
	2.3 运行iexporer ,如提示缺少本地链接库，均可通过apt-get命令安装解决
	



#### 3. 联系人：研发中心 可视化平台部
	张国光 工作邮箱： zhanggg@geovis.com.cn
    池晓焱 工作邮箱：   chixy@geovis.com.cn
