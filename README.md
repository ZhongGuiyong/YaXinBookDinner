#此为亚信MVNO部门的订餐系统。

##一、技术架构：
    1.UI技术：html,css
    2.前端技术：js，php,ajax
    3.数据库技术：mysql

##二、系统入口：index.html

##三、部署流程：
    １.将book__dinner文件夹部署到linux服务器上。
    2.将book_dinner_info.sql通过phpMyadmin导入到数据库中，这个文件为数据库表文件的结构和数据的双重备份，如要测试可使用里面的数据。
    3.进入index.html即可使用

##四、使用介绍：
    初步可供测试的人名是：钟贵勇，刘侠，刘侠萍，地址是：http://zgydwz.duapp.com/
    系统实现逻辑：
    1、在浏览器中打开index.html（注，并不是本地打开，需要部署到服务器并且已经配置好php和mysql的运行环境）
    2、用户输入姓名后，系统自动查询登录并且会有启发一个状态清除器，自动清除用户前一天或者前几天的订餐状态（如果当天已订餐不会清除当天的状态）。
    3、用户输入姓名并且输入想吃的菜，点击“订餐”，数据库自动添加用户订餐数据。
    4、如果用户当天已经订餐并且输入订菜的名称，输入姓名后系统自动弹出订餐状态并且告知用户已经预定的菜式
    5、如果用户当天已经订餐并且输入订菜的名称，输入姓名后可修改想吃的菜，点击“修改想吃的菜”，数据库会保存新的菜名。
    6、如果用户当天已经订餐并且输入订菜的名称，输入姓名后去取消订餐，点击“取消订餐”，数据库自动清除订餐状态。
    7、点击后台管理，可查看用户订餐状态，后期将完善后台管理的功能。

##五、bug说明：
    1、输入人名后由于是动态弹出菜式选择框，导致css布局有所变化。
    2、由于个人不是很懂html和css，页面显示仅在chrome浏览器显示正常，在其他浏览器均显示不正常。
    3、按钮的变化不是特别明显，这也是bug的一个地方。

##六、引用文件说明：
    1.css文件夹中使用的css样式表示从网上下载的。
    2.PHPExcel_1.8.0_doc这个文件夹使用的PHPExcel这个框架，用以在网页中读取或者生成标准格式的excel文档，详情请看excuteXls.php这个负责生成excel文档的文件。



>Writen by zhonggy
>Date：2016.8.2