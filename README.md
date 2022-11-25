# IPTV
**肥羊的IPTV直播源搜集仓库**  
**肥羊影音数码综合Telegram交流群：[点击加入](https://t.me/feiyangdigital)**  
**肥羊影音数码综合Telegram频道：[点击加入](https://t.me/feiyangofficalchannel)**  
## 抖音世界杯直播源PHP代理
- 使用Docker一键部署  
   amd64架构：  
   ```shell
   docker run -d --restart unless-stopped --privileged=true -p 9527:80 --name douyin-php youshandefeiyang/douyin-php:amd64
   ```  
   arm64架构：  
   ```shell
   docker run -d --restart unless-stopped --privileged=true -p 9527:80 --name douyin-php youshandefeiyang/douyin-php:arm64
   ```
- 使用Docker自己构建镜像并部署
    ```shell
    # 克隆项目并进入指定的路径
    git clone https://github.com/youshandefeiyang/IPTV.git && cd IPTV/douyin
    # 构建Docker镜像
    docker build -t zb-app .
    # 启动镜像
    docker run -d -p 9527:80 --name my-zb-app zb-app
    ```
- 访问地址:http://你的IP:/zb.php?id=douyin&quality=xxx  
**quality后面可以加画质参数：ld、sd、hd、uhd，什么都不加默认为uhd**
