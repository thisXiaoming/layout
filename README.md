# layout

###CSStask02布局任务三列布局
两边列固定，中间列变化.使用margin实现。

###CSS布局的几种方式
+ 使用max-width来替代width使窗口和盒模型宽度自适应。
+ 使用box-sizing使padding和border不增加视觉宽度
+ 使用overflow：auto来清除浮动：
  避免浮动的时候，浮动比父元素还高就溢出到容器外面的情况
+ 应用媒体查询进行响应式布局：
  响应式设计是一种针对不同的浏览器或者设备“响应”显示不同效果的策略。
  用百分比宽度来布局，响应式布局中，当浏览器窗口变窄无法容纳侧边栏的菜单时，布局显示为一列
+ inline-block布局：
   可以使用 inline-block 来布局。有一些事情需要你牢记： vertical-align 属性会影响到 inline-block 元素，可能会把它的值设置为 top 。 需要设置每一列的宽度 如果HTML源代码中元素之间有空格，那么列与列之间会产生空隙
+ CSS多列布局column
+ 使用flex进行布局：
  新的 flexbox 布局模式被用来重新定义CSS中的布局方式。很遗憾的是最近规范变动过多，导致各个浏览器对它的实现也有所不同。这些例子目前只能在支持 flexbox 的 Chrome 浏览器中运行，基于最新的标准。
+ 使用flex实现垂直居中。

###垂直居中
####实现垂直居中的几种方式
+ 把div的display设置长表格，使用表格的veritical-align属性来居中
+ 使用绝对定位的div，把它的top设置为50%，top margin设置为负的content的高度。
+ 推荐使用的方法：
  这种方法，在 content 元素外插入一个 div。
  设置此 div height:50%; margin-bottom:-contentheight;。
  content 清除浮动，并显示在中间。
  优点：适用于所有浏览器 没有足够空间时(例如：窗口缩小) content 不会被截断，滚动条出现
  缺点:唯一缺点需要额外的空元素了(也没那么糟，又是另外一个话题)
+ 使用一个 position:absolute，有固定宽度和高度的 div。
  这个 div 被设置为 top:0; bottom:0;。但是因为它有固定高度，其实并不能和上下都间距为 0，因此 margin:auto; 会使它居中。
  使用 margin:auto;使块级元素垂直居中是很简单的。
+ 把line-height的值设置为height的值，使用于左右的浏览器，但是只对文本生效，对块元素无效。
+ 使用flex进行垂直居中的实现。
####垂直居中布局举例
垂直居中部分是两栏布局。

  
