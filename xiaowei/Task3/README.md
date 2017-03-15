# [三栏式布局](http://ife.baidu.com/course/detail/id/94)
## 采用双飞燕布局
### 思路1
> * 1. 通过将左边的float: left;右边的部分float:right;中间的通过margin来控制从而自适应。
> * 2. 通过利用负的margin-left:100%实现后续block与main块同行显示(margin设置为负值同时float:left会有此效果)

### 碰到问题
1. 页面的最外框container始终比显示器的宽度大？
将container的width:100%属性去掉，则恢复正常。

2. 未使用如下初始化
```js
* {
	padding: 20px;
	margin: 0px;
}
```

3. 很多使用不标准，应该注重html的语义化

## 参考博客
[IFE-Task-03：三栏式布局](http://www.edwardesire.com/2016/05/29/ife-task-03-three-column-layout/)

