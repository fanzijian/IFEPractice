## [定位和居中](http://ife.baidu.com/course/detail/id/95)
## 思路

### 父元素的居中

* 父元素需要设置为absolute,设置为relative会出错，除非声明body的高度
* [relative设置为百分比](http://acgtofe.com/posts/2014/06/percentage-in-css)：当一个元素的高度使用百分比值，如果其包含块没有明确的高度定义（也就是说，取决于内容高度），且这个元素不是绝对定位，则该百分比值等同于auto

```css
position: absolute;
left: 50%;
top: 50%;
transform: translate(-50%,-50%);
```
### 子元素的定位

因为知道子元素的高度与宽度，所以直接通过绝对定位，将圆心定位到左上角与右下角。

值得注意的是，子元素需要显示为一个四分之一圆，可以通过`border-radius: 50%;`来设置。然后通过将父元素设置为`overflow:hidden`来控制只显示四分之。

### 参考资料
1. [大漠老师](http://www.w3cplus.com/css/advanced-html-css-lesson2-detailed-css-positioning.html)
2. 非常完善的讨论的各种情况的资料：[Centering in CSS](https://css-tricks.com/centering-css-complete-guide/)
3. [居中代码的生成工具](https://css-tricks.com/float-center/)