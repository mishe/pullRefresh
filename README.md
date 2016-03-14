# pullRefresh
JQUERY pullRefresh 组件

基本配置
```javascript
var cfg = {
        offsetScrollTop: 5,     //滚动条偏移值，大于此值不触发下拉事件
        offsetY: 75,             //触摸起止Y偏移值，大于些值才会触发下拉事件
        pullTipBox:'.pull-refresh',
        pullMoving: function (moveNum) {
            $(this.pullTipBox).html('释放即可刷新_'+moveNum)
        },
        pullRefresh: function () {
            var obj=$(this.pullTipBox)
            obj.html('加载中...')
            setTimeout(function(){
                obj.html('');
            },500);
        },
        pullCancel: function (el) {
            var obj=$(this.pullTipBox)
            obj.html('下拉取消...')
            setTimeout(function(){
                obj.html('');
            },500);
        }
    }
```

使用方法：

$('body').pullRefresh()
