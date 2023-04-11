个人测试 个人测试 个人测试

## Memo

TvBox相关的memo

可能是利益相关的原因，网上资讯太多实在是看不懂，所以自己整理一下

XXTV或者XXBox大概的原理是，有大神做了安卓空客程序，所谓空客就是app里没有资源本身或者没有资源的信息。
app本身应该是以在安卓TV或者谷歌TV上能看各种各样流视频的功能的一个汇总。

其基本逻辑应该是用尽一切办法收集和整合网上的视频，然后播放，所以支持很多种不同的input。

好像是（不是很确定，因为我只安装过一个app）不同的app他们大概的功能相同，但是使用的配置文件的文法不同。

jar包是爬虫本体，[类似这样](https://github.com/vpei/TvJar), 应该是不同的网站有不同的爬法[bilibili](https://github.com/vpei/TvJar/blob/master/app/src/main/java/com/github/catvod/spider/Bili.java)，[欧乐](https://github.com/vpei/TvJar/blob/master/app/src/main/java/com/github/catvod/spider/Olevod.java)。

但不可能完全靠手工去写，所以可能类似能用[xpath的](https://github.com/vpei/TvJar/blob/master/app/src/main/java/com/github/catvod/spider/XPath.java)就靠这个共通的类来弄。

CatVod/TVBox/MaoTv/Pluto Player 这些不同的名字其内容应该都是相似的。
[FongMi/Tv](https://github.com/FongMi/TV)是貌似开源的还存活的项目

配置文件应该也是近似的，所以这个配置编辑器理论上是可以通用？[配置编辑器](https://kvymin.github.io/CatVodTVJsonEditor/)

我猜测是这个大佬做的两个和TvBox类似的空壳app，貌似过去叫MaoTV后来叫BiuBiu吧
[围观大佬](https://github.com/xlc520/MaoTV)

## 围观配置文件

以这个为例子（因为感觉好像一直在更新），研究一下配置文件

https://github.com/vpei/tvurl/blob/main/out/tvbox.txt

感觉是骚操作，应该是把jar包格式换成png了，程序本身好像还支持checksum，所以应该是可以防止被修改的。

这URL甚至是ipfs的。。。

```
"spider":"http://121.36.203.35:8080/ipfs/QmaoybUpK9dEC7XJqt7hy3CWFeuxCDECPoh1iUA85K6MoR?filename=custom.PNG;md5;112dd3396623b4bebbad3ebd67fb2929",
```

感觉水很深，这些jar都是加密过的。。。
网上甚至还有[解密方法](https://github.com/dlgt7/TVbox-interface)


## memo

[xbiubiu规则](https://www.bilibili.com/read/cv17962662?from=search)
[jar](https://notabug.org/cxr1314/y)
[cloudreve](https://github.com/cloudreve/Cloudreve)
[合并数据源](https://github.com/vpei/tvurl)
[Alist样式](https://blog.ciberviler.top/script/Alist%E5%B8%B8%E7%94%A8%E6%A0%B7%E5%BC%8F%E4%BB%A3%E7%A0%81.html)
[Alist](https://alist-doc.nn.ci/docs/intro)
[TVHelper](https://github.com/sec-an/TVHelper)
[简单配置](https://github.com/smxl/assets)
[freed](https://github.com/YuanHsing/freed)