# 书籍屋电商网站

## 开发环境
    python3.7
## 依赖环境
    pip install Django==2.1.5
    pip install PyMySQL==0.9.3
    
```
# 安装 DjangoUeditor3（百度的富文本编辑器）
下载
    https://github.com/twz915/DjangoUeditor3
    (已经下载到项目根目录DjangoUeditor3-master.zip)
安装
    pip install DjangoUeditor3-master.zip

中途可能遇到的问题

  File "。。。。/book_shop/venv/lib/python3.7/site-packages/django/forms/boundfield.py", line 93, in as_widget
    renderer=self.form.renderer,
TypeError: render() got an unexpected keyword argument 'renderer'

注释掉报错的代码即可

```
## 配置数据库为Mysql

```
# settings.py

找到配置信息

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': '数据库名字',
        'USER': '数据库用户名',
        'PASSWORD': '数据库密码',
        'HOST': '127.0.0.1',
        'PORT': '3306',
    }
}

# app/__init__.py

增加以下两句代码：

import pymysql
pymysql.install_as_MySQLdb()

```
>- 迁移操作
    python manage.py makemigrations
    python manage.py migrate
    
## 运行
    python manage.py runserver

