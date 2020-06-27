
# [HousePricing](https://github.com/PENGZhaoqing/HousePricing)

**TODO list:**
1. > __地图找房__ 
~~初始位置  首页地图每平米价格~~

2. > **房源列表**
~~基本信息 -> 图片~~

3. > **房价分析**
~~热力图 -> 初始位置~~
~~Tableau (api)~~

4. > **抓取房屋及周边**
~~无法获取(或极少)商场(shop)信息~~


<br/>

**项目扩展:**
> 1. 更换为高德api
> 3. 构建房价预测模型(添加router)
> 4. 标签词云
> 2. 选择城市 -> 爬取房价信息 -> 抓取房屋及周边

<br/>

**项目使用:**
1. 安装 rails on ruby 框架

2. 安装 mysql 数据库
    + 第一次使用 mysql 请 `gem install mysql2`
    + 更改 mysql 数据库字符编码为 `utf8mb4`(请参阅网络教程/博客)
    + 在数据库中建立housepricing_develop数据库
    `CREATE DATABASE housepricing_develop`    

3. 在项目文件夹目录下
    `bundle install`

4. 编辑 */config/database.yml* 文件 *(暂未知是否root用户存在权限问题，可进行测试，如无法连接，请创建新用户并授权)*

    ```
    default: &default
        username: [your username]
        password: [your password]
    ```

5.  `rake db:migrate`&nbsp;*// 构建数据库表单*
    `rake db:seed`&nbsp;&nbsp;&nbsp;&nbsp;*// 写入housetdata.json到数据库*

6. 启动
    `rails server`
到浏览器输入`localhost:3000`即可进入
