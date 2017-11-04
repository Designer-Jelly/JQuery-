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
   


