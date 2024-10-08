### 项目描述

mockdata 是一个 Python 库，用于生成模拟数据。
它包含各个行业各种字段，包含地址，个人信息（姓名，性别，职位等），
电话，银行相关信息（信用卡，银行信息），货币（汇率、币种等），
汽车（车牌号，汽车识别码）相关信息，公司（公司名称，联系方式）信息，
信用卡，经纬度，互联网相关信息，文件，密码，代理信息等等 可以用于测试、演示和开发。

### 更新日志
```
1.0.0
    - 首次提交
1.0.1
    - 演示
1.0.2
    - 修复mock_time()方法
    - 优化MockCreditCard()类中mock_credit_card_provider()方法
    - 新增mockdata方法使用示例.doc文件，包含mockdata方法使用示例
1.0.3
    - 优化common
    - 增加语言参数，默认为中文，如需生成英文数据，请使用MockAddress('en_US').mock_address()
    
```


### 安装步骤
* 从pypi安装
```
pip install mockdata
```
* 从源码安装
```
https://github.com/Joyamon/mockdata.git
cd mockdata
python setup.py
```
### 项目目录说明
```
mockdata
    ├── __init__.py
    ├── fields
       │   ├── __init__.py
       │   ├── mock_address.py
       │   ├    ......
       └── setup.py
       └── README.md
       └── requirements.txt
    ├── mockdata方法使用示例.doc
      
    ├── utils
      └── __init__.py
       └── convert.py    # base64转图片
   

```
### 语言
```
数据默认生成为中文，如需生成英文数据，
请使用MockAddress('en_US').mock_address()
```


### 使用方法

```

C:\Users\YAFEX>pip show mockdata
Name: mockdata
Version: 1.0.0
Summary: mockdata生产数据
Home-page: https://github.com/Joyamon/mockdata
Author: 半只程序员
Author-email:
License:
Location: C:\Python312\Lib\site-packages
Requires: Faker, Pillow
Required-by:

C:\Users\YAFEX>python
Python 3.12.4 (tags/v3.12.4:8e8a4ba, Jun  6 2024, 19:30:16) [MSC v.1940 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
# 地址相关信息
>>> from mockdata.fields.mock_address import MockAddress
>>> MockAddress().mock_address()  
'吉林省阜新县永川谭路L座 836975'
>>> MockAddress().mock_city()
'成都县'
>>> MockAddress().mock_country()
'科特迪瓦'
>>> MockAddress().mock_street_name()
'蔡街'
# 表情emoji
>>> from mockdata.fields.mock_emoji import MockEmoji
>>> MockEmoji().mock_emoji()
'🛠️'
# 电话
>>> from mockdata.fields.mock_phone import MockPhone
>>> MockPhone().mock_phone_number()
'15927727902'
# 个人信息
>>> from mockdata.fields.mock_profile import MockProfile
>>> MockProfile().mock_profile()
{'job': '餐饮服务', 'company': '昂歌信息传媒有限公司', 'ssn': '440802194111247513', 
'residence': '河南省上海市高明沈阳路Z座 596771', 
'current_location': (Decimal('24.971868'), Decimal('84.577041')), 
'blood_group': 'O-', 
'website': ['https://www.shaoxue.cn/', 'https://gj.cn/', 'https://yinmo.cn/'], 
'username': 'laili', 'name': '徐志强', 'sex': 'F', 'address': '辽宁省佳县清河田街S座 185675', 
'mail': 'tzeng@gmail.com', 'birthdate': datetime.date(1920, 2, 25)}

```


### License

MIT

