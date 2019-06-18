## python ORM之peewee 学习一

### 一、原因

#### 使用ORM映射框架的原因之一是防止SQL注入

### 二、简单使用示例

#### 1.连接数据库

##### 先 from peewee import *，引入包。

#### 值得注意的是再使用peewee之前，应率先安装pymql， pip install pymysql。

##### 创建数据库连接，使用peewee的MySQLDatabase进行mysql数据的连接。

![1560849713525](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1560849713525.png)

其中这些参数分别是：test指的数据库名称、user用户名、password密码，host MySQL主机地址，port指MySQL端口。

#### 2. 创建模型

##### 使用peewee的模型的写法，我感觉和Django自带的ORM框架model的写法一致，可能现在还刚刚开始探索，区别可能深入之后会有所体现。

![1560849917642](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1560849917642.png)

##### 使用了peewee的Model，其中值得注意的是Field()的类型写法吧，CharField()在MySQL里是varchar类型，DateField()是date类型，BooleanField()是tinyint类型，默认生成id(在未有任何操作的情况下)。下面附上mysql的截图：

![1560850141130](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1560850141130.png)

##### 使用 Person.create_table()语句便可创建表。

#### 3. 增删改查

![](D:\study_collections\图片集合\Snipaste_2019-06-18_18-22-59.png)

