# 使用说明文档

功能概述：长按（时间可以自定义修改）可以DIY容器（DMO）里面子元素拖拽自定义排序位置

>1. 使用方法 页面加载完成之后在底部引入一下代码

```
<script src="./dragSort.js"></script>
<script type="text/javascript">
    $("#list1").dragsort({
        dragSelector: "li",
        dragBetween: true,
        dragEnd: saveOrder,
        placeHolderTemplate: "<li class='placeHolder'></li>"
    });

    function saveOrder() {
        var data = $("#list1 li").map(function () {
            return $(this).children().html();
        }).get();
    };
</script>
```
注释：li 可以自定义换成需要拖拽排序的目标元素，如div、tr、td等