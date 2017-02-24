# HTML5_Live

###推流APP
https://github.com/lvming6816077/LMVideoTest

###推流服务器
(nginx服务器->RTMP扩展->conf)

RTMP扩展：https://github.com/arut/nginx-rtmp-module

conf:
<pre>
rtmp {
    server{
        listen 1935: #监听的端口
        chunk_size 4000;
        application hls {#rtmp推流请求路径
            live on;
            hls on;
            hls_path /usr/local/var/www/hls;
            hls_fragment 5s;
        }
    }
}
</pre>

###HTML5播放页面
index.html