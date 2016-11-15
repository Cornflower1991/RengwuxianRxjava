## RxJava
扔物线[给Android开发者的RxJava详解](http://gank.io/post/560e15be2dca930e00da1083)文章中的例子




### 项目依赖

项目名称 | 项目信息
学习下RxJava操作符.

一、Obervable的创建
>1.create 2.from 3.just
常见操作
>1.repeat重复
>2.range 从一个指定的数字x开发发射n个数字 range()函数用两个数字作为参数：第一个是起始点，第二个是我们想发射数字的个数。
>interval轮询 第一个参数延时,第二个参数间隔,第三个参数单位
>timer 延迟执行  (官方已废弃轮训方法,推荐用interval) 第一个参数为延迟执行的时间,第二个为时间单位
二、过滤
>1、filter
>2、take   take()函数用整数N来作为一个参数，从原始的序列中发射前N个元素，然后完成.takeLast相反取后面的对应N个元素
>3、Distinct 去除重复
>4、DistinctUntilsChanged //它能轻易的忽略掉所有的重复并且只发射出新的值。
>5、First and last 只发射第一个元素或者最后一个元素。
>6、skip和skipLast 跳过前面和后面N个元素 与take 对应
三、变形
>map 1对1 的变形
>flatMap 1->Observable 的变形
>ConcatMap 与flatMap对应 维持元素顺序  flatMap是合并多次操作的结果 ConcatMap是顺序依次连接每次操作的结果.
>SwitchMap 和flatMap()很像，当源Observable发射一个新的数据项时，如果旧数据项订阅还未完成，就取消旧订阅数据和停止监视那个数据项产生的Observable,开始监视新的数据项.
>Scan 类似于递归

>lift compose


### 参考的文章
作者 | 文章| 参考的地方
------- | -------| -------
[扔物线](https://github.com/rengwuxian) | [给Android开发者的RxJava详解](http://gank.io/post/560e15be2dca930e00da1083) | 示例代码
[胡凯](https://github.com/kesenhoo) | [ 高效加载大图](http://hukai.me/android-training-course-in-chinese/graphics/displaying-bitmaps/load-bitmap.html) | Bitmap压缩算法
[intbird](http://blog.csdn.net/intbird) | [Android OOM ,回收布局文件中ImageView占用的内存.Bitmap OOM回收解决.](http://blog.csdn.net/intbird/article/details/19905549) | Bitmap回收
[任玉刚](https://github.com/singwhatiwanna)|[Android开发艺术探索](https://item.jd.com/11760209.html) | BitmapFactory解析的配置
[徐宜生](https://github.com/xuyisheng)|[Android群英传](https://item.jd.com/11758334.html)| Canvas的使用
[shwenzhang](https://github.com/shwenzhang)|[Android内存优化杂谈](http://mp.weixin.qq.com/s?__biz=MzAwNDY1ODY2OQ==&mid=400656149&idx=1&sn=122b4f4965fafebf78ec0b4fce2ef62a&3rd=MzA3MDU4NTYzMw==&scene=6#rd)| 内存优化




