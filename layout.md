# [居中布局][]
[居中布局]:https://mp.weixin.qq.com/s?__biz=MzAxODE2MjM1MA==&mid=2651553836&idx=1&sn=1f9e378e61908fd8c6c0fd81810b77fd&chksm=802557edb752defba9f1c2e462f7f09be0d1abbcbbdeb90007b80a6c4a78c855abbb5f291e39&scene=0#rd

## 水平居中

1. 使用inline-block+text-align

    + 1 原理、用法
        + 原理：先将子框由块级元素改变为行内块元素，再通过设置行内块元素居中以达到水平居中。
        + 用法：对子框设置display:inline-block，对父框设置text-align:center。
    + 2 优缺点
        + 优点：兼容性好，甚至可以兼容ie6、ie7
        + 缺点：child里的文字也会水平居中，可以在.child添加text-align:left;还原

2. 使用table+margin

    + 1 原理、用法
        + 原理：先将子框设置为块级表格来显示（类似），再设置子框居中以达到水平居中。
        + 用法：对子框设置display:table，再设置margin:0 auto。
    + 2 优缺点
        + 优点：只设置了child，ie8以上都支持
        + 缺点：不支持ie6、ie7,将div换成table

3. 使用absolute+transform

    + 1 原理、用法
        + 原理：将子框设置为绝对定位，移动子框，使子框左侧距离相对框左侧边框的距离为相对框宽度的一半，再通过向左移动子框的一半宽度以达到水平居中。当然，在此之前，我们需要设置父框为相对定位，使父框成为子框的相对框。
        + 用法：对父框设置position:relative，对子框设置position:absolute，left:50%，transform:translateX(-50%)。
    + 2 优缺点
        + 优点：居中元素不会对其他的产生影响
        + 缺点：transform属于css3内容，兼容性存在一定问题，高版本浏览器需要添加一些前缀

4. 使用flex+margin

    + 1 原理、用法
        + 原理：通过CSS3中的布局利器flex将子框转换为flex item，再设置子框居中以达到居中。
        + 用法：先将父框设置为display:flex，再设置子框margin:0 auto。
    + 2 优缺点
        + 优点：
        + 缺点：低版本浏览器(ie6 ie7 ie8)不支持

5. 使用flex+justify-content

    + 1 原理、用法
        + 原理：通过CSS3中的布局利器flex中的justify-content属性来达到水平居中。
        + 用法：先将父框设置为display:flex，再设置justify-content:center。
    + 2 优缺点
        + 优点：设置parent即可
        + 缺点：低版本浏览器(ie6 ie7 ie8)不支持

## 垂直居中
...
