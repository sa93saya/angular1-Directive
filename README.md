# angular1-Directive
@：单向引用父域的值，传递的值必须是字符串且在指令里引用时必须加上{{}}；

=：双向绑定子域和父域；

&：单向绑定父域，以便在其中运行函数


指令中compile与link函数的详解：
①一旦ng调用过指令的compile函数,就会创建一个template element的element实例对象,并且为它提供一个scope对象,这个scope有可能是新实例,也有可能是已经存在,可能是个子scope,也有可能是独立的scope,这些都得依赖指令定义对象里的scope属性值
②如果你在定义指令的时候只使用了一个link函数,那么ng会把这个函数当成post-link来处理
③当linking发生时,这个实例element以及scope对象已经是可用的了,并且被ng作为参数传递到post-link函数的参数列表中去
④ng为我们提供了一个附加的hook机制,那就是pre-link函数,它能够保证在执行所有子指令的post-link函数之前.运行一些别的代码.
一个元素的pre-link函数能够保证是运行在它所有的子指令的post-link与pre-link运行之前执行的

详情：http://www.jb51.net/article/58229.htm
