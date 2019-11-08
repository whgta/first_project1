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

## 项目结构分析：
- 1.'nanage.py':
    - 以后和项目交互基本上都是基于这个文件，一般都是在终端输入 python manage.py [子命令]。可以输入python manage.py
    - help：看下能做什么事情，除非你知道自己在做什么，一般情况下不应该编辑这个文件
- 2.'settings.py'：保存项目所有的配置信息
- 3.'urls.py':
    - 用来做url与视图函数映射的，以后来了一个请求，就会从这个文件中找到匹配的视图函数
- 4.'wsig.py':专门用来做部署的 不需要修改

## django推荐的项目规范：
- 按照功能或者模块进行分层，分成一个个app，所有和某个模块相关的视图都写在对应的app的views.py中，并且模型和其他的也是类似
- 然后django已经提供了一个比较方便创建app的命令叫做'python manage.py startapp [app名称]'。那所有的代码卸载各自的app中。


## DEBUG模式：
- 1.如果开启了DEBUG模式，那么以后我们修改了Django项目的代码，然后按下ctrl+s，那么Django就会自动的给我们启动项目，不需要手动重启。
- 2.以后Django项目中的代码出现bug，那么在浏览器中和控制台会打印出错误信息。
- 3.在生产环境中，精致开启DEBUG模式，不然由很大的安全隐患
- 4.当DEBUG模式设置程false，ALLOWED_HOSTS必须设置


## ALLOWED_HOSTS:
- 这个变量是用来设置以后别人只能通过这个变量中的ip地址或者域名来访问


