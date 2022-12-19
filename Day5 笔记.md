Day5   笔记

# css继承-层叠-元素类型

## css的属性继承

- CSS的某些属性具有继承性(Inherited):
- 如果一个属性具备继承性, 那么在该元素上设置后, 它的后代元素都可以继承这个属性;
- 当然, 如果后代元素自己有设置该属性, 那么优先使用后代元素自己的属性(不管继承过来的属性权重多高);

## 常见的继承属性有哪些

[![img](https://camo.githubusercontent.com/93a9dfd906999a72c52ac1071fe4552dc820dc63dae4d3915aa455dc6f6181db/68747470733a2f2f696d672e6f6e6d6963726f736f66742e636e2f323032322f31322f31382f65313763383165312d336164642d346533322d613837342d6330393762353433356637322e706e67)](https://camo.githubusercontent.com/93a9dfd906999a72c52ac1071fe4552dc820dc63dae4d3915aa455dc6f6181db/68747470733a2f2f696d672e6f6e6d6963726f736f66742e636e2f323032322f31322f31382f65313763383165312d336164642d346533322d613837342d6330393762353433356637322e706e67)

## css属性的层叠

- css的反编译是层叠样式表，什么是层叠呢？
  - 对于一个元素来说, 相同一个属性我们可以通过不同的选择器给它进行多次设置;
  - 那么属性会被一层层覆盖上去;
  - 但是最终只有一个会生效;
- 那么多个样式属性覆盖上去, 哪一个会生效呢?
  - 判断一: 选择器的权重, 权重大的生效, 根据权重可以判断出优先级;
  - 判断二: 先后顺序, 权重相同时, 后面设置的生效;
- css属性所处的环境定义一个权值
  - !important：10000
  - 内联样式：1000
  - id选择器：100
  - 类选择器、属性选择器、伪类：10
  - 元素选择器、伪元素：1
  - 通配符：0

## HTML元素的类型

[![img](https://camo.githubusercontent.com/3d5543f6ad89ddf6df535fc3695d5716b72a1f1b2643abdb5aae19dc6bc7d8d9/68747470733a2f2f696d672e6f6e6d6963726f736f66742e636e2f323032322f31322f31382f64323532313563382d313835312d343939392d616461642d3737326537633739636439312e706e67)](https://camo.githubusercontent.com/3d5543f6ad89ddf6df535fc3695d5716b72a1f1b2643abdb5aae19dc6bc7d8d9/68747470733a2f2f696d672e6f6e6d6963726f736f66742e636e2f323032322f31322f31382f64323532313563382d313835312d343939392d616461642d3737326537633739636439312e706e67)

## css属性-display

- CSS中有个display属性，能修改元素的显示类型，有4个常用值
  - block：让元素显示为块级元素
  - inline：让元素显示为行内级元素
  - inline-block：让元素同时具备行内级、块级元素的特征
  - none：隐藏元素

## display值的特性（非常重要）

- block元素
  - 独占父元素的一行
  - 可以随意设置宽高
  - 高度默认有内容决定
- inline-block元素
  - 跟其他行内级元素在同一行显示
  - 可以随意设置宽高
  - 可以这样理解
    - 对外说，它是一个行内级元素
    - 对内说，它是一个块级元素
- inline：
  - 跟其他行内级元素在同一行显示
  - 不可以随意设置宽高
  - 宽高都有内容决定
- [![img](https://camo.githubusercontent.com/0525d5be2845b4c08ed138340f695d9d517d666342ead591699f8460a6eb9008/68747470733a2f2f696d672e6f6e6d6963726f736f66742e636e2f323032322f31322f31382f32356234323335352d383231332d343332332d383866382d3537663638333331393461362e706e67)](https://camo.githubusercontent.com/0525d5be2845b4c08ed138340f695d9d517d666342ead591699f8460a6eb9008/68747470733a2f2f696d672e6f6e6d6963726f736f66742e636e2f323032322f31322f31382f32356234323335352d383231332d343332332d383866382d3537663638333331393461362e706e67)

## 编写HTML时的注意事项

- 块级元素、inline-block元素
  - 一般情况下，可以包含其他任何元素（比如块级元素、行内级元素、inline-block元素）
  - 特殊情况，p元素不能包含其他块级元素
- 行内级元素（比如a、span、strong等）
  - 一般情况下，只能包含行内级元素

## css样式不生效技巧

- 为何有时候编写的CSS属性不好使，有可能是因为
- 选择器的优先级太低
- 选择器没选中对应的元素
- CSS属性的使用形式不对
  \* 元素不支持此CSS属性，比如span默认是不支持width和height的
  \* 浏览器不支持此CSS属性，比如旧版本的浏览器不支持一些css module3的某些属性
  \* 被同类型的CSS属性覆盖，比如font覆盖font-size

## 盒子模型

[![img](https://camo.githubusercontent.com/b26bb3f76114e25d879889c6893ab0668c12258dd0c17dc156c078ab81ea2ae6/68747470733a2f2f696d672e6f6e6d6963726f736f66742e636e2f323032322f31322f31382f62663466633465612d306435652d343561652d393766632d3131613763353336386363302e706e67)](https://camo.githubusercontent.com/b26bb3f76114e25d879889c6893ab0668c12258dd0c17dc156c078ab81ea2ae6/68747470733a2f2f696d672e6f6e6d6963726f736f66742e636e2f323032322f31322f31382f62663466633465612d306435652d343561652d393766632d3131613763353336386363302e706e67)

## 内容和高度

- 设置内容是通过宽度和高度设置的：
  - 宽度设置：width
  - 高度设置：height
- 注意：对于行内级非替换元素来说，设置高度是无效的！
- 还有以下属性的设置
  - min-width：最小宽度，无论内容多少，宽度都大于或等于min-width的值
  - max-width：最大宽度，无论内容多少，宽度都小于或等于max-width
  - 移动端适配时, 可以设置最大宽度和最小宽度;
- 下面两个属性不常用
  - min-height：最小高度，无论内容多少，高度都大于或等于min-height
  - max-height：最大高度，无论内容多少，高度都小于或等于max-height

## 内边距-padding

- padding属性用于设置盒子的内边距, 通常用于设置边框和内容之间的间距
- padding包括四个方向，所以有如下取值：
  - padding-top：上内边距
  - padding-right：右内边距
  - padding-bottom：下内边距
  - padding-left：左内边距
- padding单独编写是一个缩写属性：
  - padding-top、padding-right、padding-bottom、padding-left的简写属性
  - padding缩写属性是从零点钟方向开始, 沿着顺时针转动的, 也就是上右下左

[![img](https://camo.githubusercontent.com/a9aa51730acf459a2d833fb800aa563130c8c94f3a139d82dffbdbd2fa18be55/68747470733a2f2f696d672e6f6e6d6963726f736f66742e636e2f323032322f31322f31382f30633836313532652d306632382d346133662d613663392d3435646164616136366137652e706e67)](https://camo.githubusercontent.com/a9aa51730acf459a2d833fb800aa563130c8c94f3a139d82dffbdbd2fa18be55/68747470733a2f2f696d672e6f6e6d6963726f736f66742e636e2f323032322f31322f31382f30633836313532652d306632382d346133662d613663392d3435646164616136366137652e706e67)

## 边框-border

- 边框相对于于content/padding/margin来说特殊一些:
  - 边框具备宽度width;
  - 边框具备样式style;
  - 边框具备颜色color;
- 边框的宽度
  - border-top-width、border-right-width、border-bottom-width、border-left-width
  - border-width是上面四个属性的缩写
- 边框颜色
  - border-top-color、border-right-color、border-bottom-color、border-left-color
  - border-color是上面4个属性的简写属性
- 边框样式
  - border-top-style、border-right-style、border-bottom-style、border-left-style
  - border-style是上面4个属性的简写属性