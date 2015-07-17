# responsive-page
v1.0.0 2015-7-16 by Sun

让你的页面轻松适配各种移动设备和PC端浏览器

* 非常适合专题landing页
* 页面内容一般为几张图片拼接
* 同时要适配移动端和PC端
* 要自适应宽度
* (绝对)定位元素仅需使用px单位即可适配
* 切图时仅需切640宽(可以配置)的图片
* 即使内容很长, 换行也需要正确

## 基础原理
计算出页面内容与页面宽度的比率, 通过 transform: scale 缩放页面内容来达到适配任何屏幕(占满屏幕宽度)的目的.

## 兼容性
特性: querySelectorAll, CSS3 transform, matchMedia
*   PC端: IE9+, 其他现代浏览器(chrome, firefox等等)
* 移动端: iOS4+, Android 2.3+

## 示例
* [jd.html](http://ufologist.github.io/responsive-page/demo/jd.html) 页面中包含多个需要适配的模块
* [70c.html](http://ufologist.github.io/responsive-page/demo/70c.html) 页面仅包含一个需要适配的模块和绝对定位的可点击区域, 并开启 center 模式来适配PC端

## 使用手册
最好的使用手册就是示例

## API文档
```javascript
responsivePage(options);
```

| 参数    |            | 作用                                                                            |
|---------|------------|---------------------------------------------------------------------------------|
| options | {          |                                                                                 |
|         | selector   | string, 内容区域的父级元素, 接受任何合法的CSS选择器, 默认为: .mod-responsive    |
|         | sliceWidth | number, 切片宽度(单位是px), 默认为: 640                                         |
|         | center     | boolean, 页面宽度超过切片宽度后, 是否不再适配宽度居中显示在页面中, 默认为: true |
|         | }          |                                                                                 |

## 版本更新历史
[CHANGLOG](CHANGLOG.md)

## 感谢他们给我的灵感
* [pageResponse](https://github.com/peunzhang/pageResponse)
* [JD的页面](http://sale.jd.com/m/act/LZkDEwunm53ilyrR.html)