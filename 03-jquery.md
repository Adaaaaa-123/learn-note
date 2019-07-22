## jQuery
### 1.什么是jquery
- JQuery是js的一个库,包含多个js函数,把这些函数进行了封装,方便用户使用.
### 2. window.onload和$(document).ready事件
- window.onload事件会覆盖,所以一个页面中只能使用一个.而$(document).ready事件可以使用多个.
- 它们都是当页面或图片加载完执行.
### 3. 处理事件的过程
-  获取事件源
-  绑定事件
- 编写事件处理程序
### 4. 获取事件源
- 简单选择器:$('selecter'); 包含 class,id,标签,后代,子代,交集,并集等简单选择器  还有+ ~等选择器
- 过滤选择器:$('selecter:XX') 包括gt,lt,even,odd,first,last等选择器.
- 属性选择器: $(selecter[xx])通过属性名,属性名+属性名等来进行选择目标元素.
### 5. 关系查找:
- XX.find(select)  所有的select的后代元素
- XX.children()  所有子代元素
- XX.sibings() 所有兄弟
- XX.parent() 直接父元素
- XX.eq() 查找指定元素的第N个元素
### 6. mouseenter
### 7. Dom对象和JQ对象的转换
- jq->dom: $box[0]==box; $box.get(0)==box;
- dom>JQ: $(box)==$box:
### 8. Dom操作:
- 获取设置属性:xx.attr();
- 删除属性: xx.removeAttr();
- 内容: text(),html(),val();
### 9.操作类
- addClass(),removeClass(),toggleClass()(切换类名),hasClass()
### 10. JQ动画
- show()动画展示
- hide()动画隐藏
- sildeDown(),slideUp()划入划出
- slideToggle()切换
- fadeIn(),fadeOut() 淡入淡出
- fadeToggle()
- fadeTo()改变透明度
### 11. 自定义动画
- XX.animate(styles,speed,easing,callback)
- styles:要执行动画的CSS属性(必选)
- speed:持续时间(可选)
- easing:指定线性还是非线性(linner,swing)
- callback:动画执行完立即执行的回调函数
### 12. 停止动画
- 作用:停止正在执行的动画
- 参数1:stopAll:是否全部停止,默认为false
- 参数2:goToEnd:是否将停止动画停止到当前,动画的最后一个状态,默认为false
### 13.节点操作
- 创建节点:var $node = $('<p>不凡学院</p>');
- 插入节点:append() , appendTo() , prepend() ,after() , before()
- 复制节点:xx.clone();
### 14.删除节点
- 清空被选节点内容(文本,标签等):empty(),html()
- 会把对象自己也干掉:remove()
### 15.获取和设置属性
- 获取:prop('属性名')
- 设置: prop('属性名','属性值') 第二个参数默认false
### 16. 尺寸和位置操作
- height(),width():获取或者设置宽高 num类型
- offset():获取或设置元素相对于文档的位置(num)
- offset获取:xx.offset()或xx.offset().left
- 设置 xx.offset({l:0,p:0})
- position() 获取相对于其最近的具有定位的父元素位置,不能设置
- scrollTop() 获取或设置元素垂直方向滚动位置(卷进去的高度)
### 17. 用on方式绑定事件:off解绑
- $('box').on('click',function(){})
- $('.box').off() 取消所有事件(无参数)
- $('.box').off('.click') 取消指定事件
### 18. 事件委托
- $('.box').on('click','p',function(){})
### 19. 事件对象(事件发生时的附加信息)
- 在事件处理程序中加event形参
- event.currentTarget 等同于this 当前Dom对象
- event.Target 触发事件源,不一定等于this
- event.type 事件类型
- event.keyCode 键盘按键编码
- event.pageX/Y 鼠标相对于文档左/上边缘的位置
- event.witch 鼠标按键类型 左1中2右3
### 20. 组织冒泡和默认
- event.stopPropagation(); 组织冒泡
- event.preventDefault(); 阻止默认
### 21. each()方法:
- $('li').each(fuction(index,ele){
    ele 正在遍历的元素 dom对象
    index 当前遍历元素的下标
})





