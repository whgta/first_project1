# 第一个项目笔记：
## 创建项目：
- 1.通过命令行方式：
    '''
    django-admin startproject [项目名称]
    '''
- 2.通过pycharm的方式：文件->新建项目->选择django。然后指定项目所在位置以及python解释器，再点击creat创建即可


## 项目运行：
- 1.终端：进入项目文件夹中，然后执行下面的语句：
    '''
    python manage.py runserver
    '''
    
## 改变端口号：
- 1.在终端：运行是加上端口号就可以，命令为：python manage.py runserver 9000
- 2.在pycharm中，右上角->项目配置->port.改变你想要的端口号

## 让同局域网中的其他电脑可以访问本机项目：
- 1.让项目运行的时候，host为0.0.0.0
    - 在终端，使用命令python manage.py runserver 0.0.0.0:8000
    - 在pycharm， 右上角->项目配置->host，改为0.0.0.0
- 2.在'settings.py'文件中，配置'ALLOWED_HOSTS',将本机地址添加进去
    - 注意关闭防火墙
    
