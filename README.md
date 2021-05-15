# ws_flask

today i want to use mac to run the uwsgi + python3.6 + django1.11
使用了pipenv shell来作为虚拟环境
我使用了uwsgi来实现websocket, 但是报了错误
you need to build uWSGI with SSL support to use the websocket handshake api function !!!
我已经使用brew install openssl 安装了 openssl,

找到了网上的方法

CFLAGS="-I/usr/local/opt/openssl/include" LDFLAGS="-L/usr/local/opt/openssl/lib" UWSGI_PROFILE_OVERRIDE=ssl=true pip install uwsgi -I --no-cache-dir
