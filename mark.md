#### 总体

```
a{text-decoration: none;color: black;}
*{margin: 0;padding: 0;}/*清除所有元素自带的margin和padding属性以便调整*/
.content{width:55.625rem;margin: 0 auto;}/*margin:0 auto 用于居中一整个块元素*
```



清除a自带样式，清除所有元素自带内外边距

margin: 0;padding: 0;居中整个大块元素

开发技巧设置

 *设置border{0.001rem solid}可以观察每个模块的大小边

**包围标签：双击div标签开头选中标签内容2、按Ctrl+]包围3、输入div即可在首尾添加包围标签**

反包围：双击标签开头选中标签内容2、按Ctrl+shift+]反包围3、可去掉最外层的p标签并自动处理子节点的缩进

撤销多选光标的最后一个光标：双击选中class2、按下Ctrl+e选中相同词3、按Ctrl+shift+z不再选中最后一个词

ctr+/ 注释或反注释

**转到定义：Alt+d**

**折叠其他选区：Alt+Shift+o。**

**左边的大纲是长文档导航的利器。alt+w激活它(mac是ctrl+w)**

**ctr+/可以注释所选区域**

行内样式表会使hover无法使用

#### 顶部（top)

```
<div id="top" style="width=100%">
```

一定要设置成百分比模式 否则放缩时候无法铺满

** line—height=height时 可以使文字居中对齐**

不要设定高度 要靠内容撑开

#### 第一部分（one）



```
#content_one li{display: table-cell;text-align: center;vertical-align: middle;}/*display li ul父子元素配合 转化为表格模式使其可以横向显示并均匀分配空间*/
#content_one ul{width: 34.375rem;float: right;height: 4.1875rem; display:table;list-style: none;font-size: smaller;font-weight: 800;}
```

ul横向排布+均匀对齐

ul内添加display：table 每个li内添加display：table-cell 使其拥有表格均匀分割的性质

![](/one_1.png)



#### 第二部分（two）

![](/two_1.png)

input type=button无法实现搜索图片与文字并齐，使用button标签即可

右侧文本框没有实现文本输入限制从缩进后才开始

放缩时背景不会断开

![](/two_2.png)

书上的小技巧 对于列表 中间有格线

```
li+li{border-top:0.3125rem solid gray;}
```

使相邻元素才会有边界

#### 第三部分

![](/three_1.png)

点击这四个框会改变右边内容（内容全是自己找的呜呜）

```
var li=document.querySelectorAll("#three li");
				var text=document.querySelectorAll(".three_text")
				var mark=0;
				li[0].onclick=function()
				{
					text[1].style.display="none";
					text[2].style.display="none";
					text[3].style.display="none";
					text[0].style.display="block";
					li[mark].style.backgroundColor="#1d9f9f";
					li[mark].style.color="white";
					li[0].style.backgroundColor="white";
					li[0].style.color="black";
					mark=0;
```

点击 0标的事件 其他均隐藏 显示0的内容 改变导航的颜色 并改变上次点击导航的颜色

记录此次事件发生的下标 以便下次事件发生改变导航的颜色

其他三个事件也是类似此

#### 第四部分

![](/four_1.png)

这个图片的带背景颜色的 通过ps的取色器 调整到与图片颜色一模一样的效果

#### 其他

某个大bug 浏览器会有右边的空白 最后通过显示边框看出问题部分 寻找很久发现是定义了一个marginleft导致超出边界。。。

