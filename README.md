# haley教你如何实现页面跨媒体布局，及应该注意哪些细节处理
常用媒体查询的写法
## 基本套路：
1. 先写不带媒体查询的设计图样式，
2. 然后依次从小到大挨个写，
3. 这样的好处是，比如我没有写1366px的屏，那么他会继承1280px的，这样就不会导致样式错乱
4. 如果从大到小反着写，如果用户使用1366px屏幕，那么样式会继承1440px的，会导致页面错乱。
## 跨媒体系统需要的一些基本样式表及其顺序
### base级基础样式，可以写一些基本的缩写等，比如 fz12 表示font-size:12px;ovh表示overflow:hidden;fl表示float:left;等等 也可以直接引入我的另外一个库文件 [base级样式库](https://github.com/haley168/style-base)
### 初始化 诸如 p h系列等的margin
### 插件类 引入的第三方插件 诸如 bootstrap swiper等
### pc端基础搭建 先将pc端页面搭建完毕
### pc端媒体查询 不同显示尺寸下的效果 这个仅在pc端引入
### pc与phone的控制显示 有些特殊元素可能需为pc和wap各写一套样式，同时在pc端仅显示pc端，wap端仅显示wap的，xs-hide表示wap隐藏；sm-hide表示pc端隐藏
### 手机端专属样式 这个仅在wap端引入


# [查看demo](https://haley168.github.io/media/)
