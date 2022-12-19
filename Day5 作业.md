## 一、写出案例，证明CSS属性的继承性

```html
<head>
    <style>
        div.box{
            color:red;
        }
    </style>
</head>
<body>
    <div class="box">
        <h1>
            标题
        </h1>
        <p>
            <span>hahaha</span>
            <strong>加粗</strong>0
        </p>
        <span>
        xixixi
        </span>
    </div>
</body>
```

## 二、写出案例，证明CSS属性的层叠性

```html
<html>
    <head>
        <style>
            .box{
                color:red;//红色
            }
            .box{
                color:aqua;//浅蓝色
            }
            .box{
                color:pink;//粉色
            }
            .box{
                color:orange;//橙色
                font-size:30px;
            }
            
        </style>
    </head>
    <body>
        <div class="box">
            哈哈哈哈
        </div>
    </body>
</html>
```

## 三. 默写出display常见的值，并且说出对应的特性，并且写出测试案例

- inline，行内显示，不可设置宽高，宽度由内容决定；

- block，块级显示（独占一行），可设置宽高，默认高度是内容的高度；

- inline-block，行内显示，可设置宽高，默认高度由内容决定。

  ```html
  <html>
      <head>
          <style>
              .box{
                  boder:1px solid red;
                  display:inline-block;
                  padding:10px 20px 30px 40px;
              }
          </style>
      </head>
      <body>
          <div class="box">
              我是一个div元素
          </div>
      </body>
  </html>
  ```

  ## 四. 总结元素隐藏的方法，并且说出他们的区别

  - display: none（隐藏不占据空间）
  - visibility: hidden（占据空间）
  - rgba -> alpha（透明度：0~1,0透明、1不透明）
  - opacity -> 设置透明度
    - 所有的子元素都会跟着一起设置

  ## 五. 说说你对margin的传递和折叠的理解

  上下，左右传递折叠

  ## 六. 块级元素在设置padding/border的上下时，有什么特殊的地方？

  块级元素可以设定外边距,上右下左都有效;

  行内元素可以设定外边距,左右有效,上下无效。

## 七. 进行下面的案例练习

- 可以先不做两行显示不全的...
- 可以先不做评论的靠右内容

[![image-20220330230100029](https://camo.githubusercontent.com/df31e63e470245da3f173ce012cdf70b9607bb891c226cf3a1c0a3c730477966/68747470733a2f2f747661312e73696e61696d672e636e2f6c617267652f6536633964323465677931683073623031737831796a323037703039796466772e6a7067)](https://camo.githubusercontent.com/df31e63e470245da3f173ce012cdf70b9607bb891c226cf3a1c0a3c730477966/68747470733a2f2f747661312e73696e61696d672e636e2f6c617267652f6536633964323465677931683073623031737831796a323037703039796466772e6a7067)
