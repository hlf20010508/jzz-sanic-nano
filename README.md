本程序为jzz-sanic精简版
完整版项目https://github.com/hlf20010508/jzz-sanic.git

<br/>

连接数据库后的效果

<img src='https://github.com/hlf20010508/jzz-sanic-nano/raw/master/readme_photos/1.png'/>
<img src='https://github.com/hlf20010508/jzz-sanic-nano/raw/master/readme_photos/2.png'/>
<img src='https://github.com/hlf20010508/jzz-sanic-nano/raw/master/readme_photos/3.png'/>
<img src='https://github.com/hlf20010508/jzz-sanic-nano/raw/master/readme_photos/4.png'/>


本程序需要mysql服务器

在mysql服务器中创建一个数据库，然后将jzz-nano.sql导入该数据库即可得到数据示例

<br/>

运行config.py设置数据库配置

```
python config.py
```

<br/>

运行程序
```
sanic run.app -H 127.0.0.1 -p 5000
```

<br/>

若需要部署到服务器上，需要将host设置为0.0.0.0

需要开机运行，则将jzz-nano@.service复制到系统目录/etc/systemd/system文件夹下

在jzz-nano@.service中编辑host和port，并更改工作目录

<br/>

开机运行
```
sudo systemctl enable jzz-nano@username
```

此处username为系统当前用户名

立即运行
```
sudo systemctl start jzz-nano@username
```

取消开机运行和当前运行分别使用disable和stop，查看状态使用status

<br/>

本程序使用的前端来自jzz-vue-nano项目https://github.com/hlf20010508/jzz-vue-nano.git
