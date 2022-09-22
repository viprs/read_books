《Selenium 2自动化测试实战》
======================
[中]虫师 电子工业出版社 2016


第1章 自动化测试基础
------------------
分层的自动化测试

自动化工具介绍


第2章 测试环境搭建
------------------
Windows下环境搭建

Ubuntu下环境搭建

第3章 Python基础
------------------
略

第4章 WebDriver API
-------------------
	4.1 从定位元素开始
		4.1.1 id定位
		4.1.2 name定位
		4.1.3 class定位
		4.1.4 tag定位
		4.1.5 link定位
		4.1.6 partial link定位
		4.1.7 XPath定位
		4.1.8 CSS定位
		4.1.9 用By定位元素

	4.2 控制浏览器
		控制浏览器窗口大小
			driver.maximize_window()
		控制浏览器后退、前进
			driver.
		模拟浏览器刷新

	4.3 简单元素操作
		4.3.1 126邮箱登录
		小作品：163邮箱登录
		代码：
		4.3.2 WebElement接口常用方法

	4.4 鼠标事件
	4.5 键盘事件


第5章 自动化测试模型
---------------------
	5.1 自动化测试模型介绍
	5.2 模块化驱动测试实例
	5.3 数据驱动测试实例
		5.3.1 参数化邮箱登录
		5.3.2 参数化搜索关键字
		5.3.3 读取txt文件
		5.3.4 读取csv文件
		5.3.5 读取xml文件

第6章 Selenium IDE 
------------------
	6.1 IDE安装
	6.2 界面介绍
	6.3 创建测试用例
	6.4 Selenium IDE命令
	6.5 断言与验证
		断言：失败则停止，强校验。如assertTitle assertText assertAlert
		验证：失败则继续，弱校验。如verityTitle verifyText verifyAlert
	6.6 等待与变量
		等待：
			等待固定时间：pause(seconds)
			在一定时间内等待某一元素：waitForTitle waitForText，如果没有设置时间，默认为60秒
		变量：
			存储变量：storeTitle storeText storeForElementPresent 分别定义成为title、text和element变量中。
			使用变量：type id=kw ${value}

第7章 unittest单元测试框架
-------------------
	7.1 认识unittest
	7.2 更多关于unittest
		用例执行的顺序
		执行多级目录的用例
		跳过测试和预期失败
	7.3 带unittest的脚本分析
	7.4 编写web测试用例

第8章 自动化测试高级应用
-------------------
	8.1 HTML测试报告
		用HTMLTestRunner生成HTML测试报告
			例子：
			    fp = open('./test_result_%s.html' % time.strftime("%Y-%m-%d %H-%M-%S"), 'wb')
			    runner = HTMLTestRunner(stream=fp,
			                            title=u'百度搜索测试报告',
			                            description=u"测试用例执行情况：")
			    runner.run(suite)
			    fp.close()
	8.2 自动发送邮件功能
		小作品：用163邮箱发送自动化邮件
		*遇到的问题*：163邮箱不能直接用用户名和密码登录，需要：
		* 先开通SMTP协议，这时需要设置授权码（不能与密码相同）
		* 用SMTP协议登录时，密码应该用授权码
	8.3 Page Object设计模式
		8.3.1 认识Page Object
		8.3.2 Page Object 实例