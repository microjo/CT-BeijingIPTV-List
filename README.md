# 中国电信北京 IPTV 播放列表

## 来源
参照 [北京电信 IPTV 播放列表][OpenGG-bj-telecom-iptv]中的地址，使用 [sdhzdmzzl@github](https://github.com/sdhzdmzzl) 的[扫描工具][iptv_channel_scanner_windows]生成，有2个不同地址段扫描成功，结果分别是[`IPTV-Raw1.m3u`](IPTV-Raw1.m3u)和[`IPTV-Raw2.m3u`](IPTV-Raw2.m3u)。

## 剔除重复的频道数
**合计** | **181**
-----|-----
高清 | 70
4K | 2
标清 | 109

## 组播播放列表
参照[北京联通 IPTV 播放列表][wuwentao-bj-unicom-iptv]的修改方式，按以下规则，生成清晰的包含组播地址的播放列表[`iptv-multicast.m3u`](iptv-multicast.m3u)。

* 在扫描的地址顺序基础上，根据***先高清后标清 + 央视、北京等分类***排序
* 逐个打开节目源，标记频道名称
* 频道名称增加关键字区分节目源清晰度
	1. 标识***高清***为1080p
	2. 标识***4K***为4K
	3. 无标识则为***标清***

## 参考资料
* [北京电信 IPTV 播放列表@OpenGG][OpenGG-bj-telecom-iptv]
* [北京联通 iptv 列表@sdhzdmzzl](https://gist.github.com/sdhzdmzzl/93cf74947770066743fff7c7f4fc5820)
* [北京联通 IPTV 播放列表@wuwentao][wuwentao-bj-unicom-iptv]
* [北京联通 IPTV 频道列表@islercn](https://github.com/islercn/BeiJing-Unicom-IPTV-List/)
* [北京联通的 IPTV 节目列表](https://bjiptv.tk/)
* [PDCN Padavan 老毛子固件静态路由设置教程（第一步）](http://www.nihaodd.com/jiaocheng/242.php)
* [浙江电信 IPTV+上网 Padavan 老毛子固件单线复用](https://blog.csdn.net/xiangsanliu/article/details/104269601)
* [IPTV 直播源抓包教程，新手小白向](https://www.znds.com/tv-1137126-1-1.html)
* [IPTV 中继原理](https://github.com/wuwentao/bj-unicom-iptv/blob/master/iptv.md)
* [组播 IP 地址到底是谁的 IP？](https://www.zhihu.com/question/27233903)


[OpenGG-bj-telecom-iptv]: https://github.com/OpenGG/bj-telecom-iptv
[wuwentao-bj-unicom-iptv]: https://github.com/wuwentao/bj-unicom-iptv
[iptv_channel_scanner_windows]: https://github.com/sdhzdmzzl/iptv_channel_scanner_windows