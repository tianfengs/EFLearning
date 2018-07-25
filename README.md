# EFlearning
学习entity framework心得和遇到的问题

## Entity Framework使用MySql遇到的问题，下面是测试通过的方案

1. MySql版本选择：64位版 mysql-5.6.25-winx64.zip   
	
	1.1 ，由于MySql的最新版8.11.0暂时还无法和EF兼容。  
	1.2 下载地址 https://downloads.mysql.com/archives/community/ 此地址为Archived Versions下载地址
2. 在VS 2013中使用 Entity Framework Power Tools Beta5（在vs2017中没有成功使用）
	1. 1 此插件可以把MySql数据库转成Code First架构。而不像使用Add/ADO.Net Entity DataModel功能，产生edm文件
3. MySQL for Visual Studio 要用最新的1.2.8否则，只能在VS 2013中加载MySql库，在VS 2017中加载不了
4. Connector/NET 使用6.8.3版本测试通过，最新的8.11.0版本暂时无法和EF兼容
	1.1 下载地址 https://downloads.mysql.com/archives/c-net/  此地址为Archived Versions下载地址
	1.2 下载文件名为mysql-connector-net-6.8.3 
5. 如果出现以下错误“未为提供程序“MySql.Data.MySqlClient”找到任何 MigrationSqlGenerato”时，要手动引用相应版本的“MySql.Data.Entity.EF6”，此处引用6.8.3.0,并在配置文件（App.config）中的provider中设置正确版本号。
6. App.config范例请看文件：“App配置范例.txt”[App配置范例.txt]
