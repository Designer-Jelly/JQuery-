# JQuery-
My personal notes of learning Jquery

jQuery选择器之内容筛选选择器
:contains与:has都有查找的意思，但是contains查找包含“指定文本”的元素，has查找包含“指定元素”的元素
如果:contains匹配的文本包含在元素的子元素中，同样认为是符合条件的。
:parent与:empty是相反的，两者所涉及的子元素，包括文本节点

jQuery选择器之可见性筛选选择器
我们有几种方式可以隐藏一个元素：
CSS display的值是none。
type="hidden"的表单元素。
宽度和高度都显式设置为0。
一个祖先元素是隐藏的，该元素是不会在页面上显示
CSS visibility的值是hidden
CSS opacity的指是0
但是在Jquery中认为
如果元素中占据文档中一定的空间,元素被认为是可见的。
可见元素的宽度或高度，是大于零。
元素的visibility: hidden 或 opacity: 0被认为是可见的，因为他们仍然占用空间布局。
故上述的最后两个是不能实现可见性筛选的
   
jQuery选择器之属性筛选选择器
在这么多属性选择器中[attr="value"]和[attr*="value"]是最实用的

jQuery选择器之子元素筛选选择器
:first只匹配一个单独的元素，但是:first-child选择器可以匹配多个：即为每个父级元素匹配第一个子元素。这相当于:nth-child(1)
:last 只匹配一个单独的元素， :last-child 选择器可以匹配多个元素：即，为每个父级元素匹配最后一个子元素
如果子元素只有一个的话，:first-child与:last-child是同一个
 :only-child匹配某个元素是父元素中唯一的子元素，就是说当前子元素是父元素中唯一的元素，则匹配
jQuery实现:nth-child(n)是严格来自CSS规范，所以n值是“索引”，也就是说，从1开始计数，:nth-child(index)从1开始的，而eq(index)是从0开始的
nth-child(n) 与 :nth-last-child(n) 的区别前者是从前往后计算，后者从后往前计算

jQuery的属性与样式之.attr()与.removeAttr()
$('input:eq(1)').attr('value')
$('input:eq(2)').attr('value',function(i, val){
    		return '通过function设置' + val
    	})

jQuery的属性与样式之html()及.text()
.html() 不传入值，就是获取集合中第一个匹配元素的HTML内容
.html( htmlString )  设置每一个匹配元素的html内容
.html( function(index, oldhtml) ) 用来返回设置HTML内容的一个函数
$(".left div:first").html('整个div的子节点都被替换了')
$(".left a:first").text('替换第一个a元素的内容')
$(".left a:first").text(function(index,text){
            return '增加新的文本内容' + text
        })

