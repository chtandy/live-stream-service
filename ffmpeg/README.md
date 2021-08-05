### command
```
ffmpeg -i "rtmp://172.31.0.11:1935/source/111.stream"  -max_muxing_queue_size 1024 -filter:v "realtime" -tune zerolatency -s 1280x720 -r 30 -vcodec libx264  -b:v 2560k -bf 0  -ar 44100 -ac 1 -b:a 128k -colorspace:v "bt709" -color_primaries:v "bt709" -color_trc:v "bt709" -color_range:v "tv" -pix_fmt yuv420p -f flv rtmp://input.xtj99.com/live/ffmtest1 &
```


- wowza 不需重新編碼  `-c:a copy -c:v copy`
```
ffmpeg -re -i rtmp://out.xtj99.com/live/720 -c:a copy -c:v copy -f flv rtmp://adfd4b1db7c624d418b12568336687fb-172053035.ap-northeast-1.elb.amazonaws.com/live/720
```
- srs 要重新編碼才能推 `-c:a aac -c:v h264`
```
ffmpeg -re -i rtmp://out.xtj99.com/live/720 -c:a aac -c:v h264 -f flv rtmp://a1bf9a304267c463c937cb42211b323e-1994924086.ap-northeast-1.elb.amazonaws.com/live/720
```
