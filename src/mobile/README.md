

说到前端页面的布局方案，可以从远古时代的Table布局说起，然后来到 DIV+CSS布局，之后有了Float布局，Flex布局，Column布局，Grid布局等等。

而另一方面，还有一些 布局概念：

1. 静态布局

直接使用px作为单位

2. 流式布局

宽度使用%百分比，高度使用px作为单位

3. 自适应布局

创建多个静态布局，每个静态布局对应一个屏幕分辨率范围。使用 @media媒体查询来切换多个布局

4. 响应式布局

通常是糅合了流式布局+弹性布局，再搭配媒体查询技术使用

5. 弹性布局

通常指的是rem或em布局。rem是相对于html元素的font-size大小而言的，而em是相对于其父元素（非font-size的是相对于自身的font-size）


rem布局 设计稿750px
```
var _winWidth = document.documentElement.clientWidth || window.innerWidth,
    _style = document.getElementsByTagName("html")[0].style;
_winWidth >= 750 ? _style.fontSize = "100px" : _style.fontSize = _winWidth / 7.5 + "px";

```
