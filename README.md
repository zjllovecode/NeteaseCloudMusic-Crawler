# NeteaseCloudMusic Crawler
概述：
---------
  一个使用Java实现的爬虫程序，用于爬取网易云音乐上的音乐信息。

## 使用方法：
  
1.访问localhost:8080/init?auth=888888 初始化歌曲分类。

2.访问localhost:8080/crawl?auth=888888。

3.点击歌曲评论数排行榜，可查看网易云音乐上评论量最多的歌曲(根据评论数降序排序)。

4.点击歌单播放量/收藏量排行榜可分别查看播放量与收藏量较高的歌单。

5.点击根据url获取歌曲信息，输入要查询的歌曲页面对应的url，可从页面上看到歌曲的基本信息及其热门评论，评论信息会存入数据库中。

6.点击根据url获取歌单信息，输入要查询的歌单页面对应的url，可从页面上看到歌单的相关信息。

7.点击热门评论排行榜可查询之前查找过的热门评论(按评论点赞数降序排序)。

程序会在凌晨一点自动更新评论数。

## 注意：

数据库使用mysql，运行爬虫前需要创建名为crawl的数据库.
由于网易云音乐内容评论采用utf8mb4。utf8mb4是utf8的扩展，所以数据库字符集也要相应的设置为utf8mb4，排序规则选择第一个非空的就行。
（utf8与utf8mb4的区别https://my.oschina.net/zjllovecode/blog/1509900）
