说明：
     1. 请将demo_stream_decoding.c 和 MakeFile  文件放入安装目录/usr/local/SmarHTC_V6624/example/目录中，cd /usr/local/SmarHTC_V6624/example/，
     2. 执行make cleaan;make, cp demo_stream_decoding ../bin，注意可能需要安装 ZMQ 开发库
     3. 请将rtsp.txt 和 infer_sim_20240606.py 件放入安装目录/usr/local/SmarHTC_V6624/bin/ 目录中，另开 shell窗口，python infer_sim_20240606.py 12
     4. 修改rtsp.txt 文件中video stream，确保文件中视频流可读，文本中有多少路就是一次执行并发路数
     5. 开 shell窗口， mkdir -p /tmp/data/;mount -t ramfs -o size=10M ramfs /tmp/data/  /tmp/data/ 目录可以依据需求修改，
        demo_stream_decoding 中 -o 参数须与保持一致
     6. cd /usr/local/SmarHTC_V6624/bin/，
     ./demo_stream_decoding -i ./rtsp.txt -o /tmp/data/ -k
     7. 可开 shell窗口 cd /usr/local/SmarHTC_V6624/bin/，./dfu-smi 查看负载