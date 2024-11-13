# CSS 基本概念

## 一、CSS是什么

CSS 是层叠样式表，能对网页中元素位置的排版进行像素级精确控制，实现美化页面的效果，能够做到页面样式和结构分离。

## 二、CSS 基本语法规范

**选择器 + （一条/N条声明）**

- 选择器决定针对谁修改（找谁）
- 声明决定修改啥（干啥）
- 声明的属性是键值对

```css
<style>
    p {
	/* 设置字体颜色 */
        color: red;
        /* 设置字体大小 */
        font-size: 30px;
    }
</style>

<p>hello</p>
```

> [!NOTE]
>
> - CSS 要放到 style 标签中
> - style 标签可以放到页面仍和位置
> - CSS 使用 /* */ 作为注释

## 三、引入方式

### 1.内部样式表

写在 style 标签中，嵌入到 html 内部

理论上来说 style 放到 html 的哪都行，但是一般都是放到 head 中

- 优点：这样做能够让样式和页面结构分离
- 缺点：分离的还不够彻底，尤其是 CSS 内容多的时候

### 2.行内样式表

通过 style 属性，来指定某个标签的样式。

```html
<style>
    div {
        color: red;
   }
</style>
<div style="color:green">
    阿伟
</div>
```

这时红色被绿色覆盖了。

### 3.外部样式

实际开发中最常用的方式

1. 创建一个 css 文件
2. 使用 link 标签引入 css

```html
<link rel="stylesheet" href="[CSS文件路径]">
```

例如：

html文件：

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>外部样式</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div>上帝为你关上一扇门, 然后就去睡觉了</div>
</body>
```

style.css 文件：

```css
div {
    color: red;
}
```

- 优点：样式和结构彻底分离了

- 缺点：收到浏览器缓存影响，修改之后不一定立刻生效

  > 缓存时计算机中一种常见的提升性能的技术手段。
  >
  > 网页依赖的资源（图片/CSS/JS等）通常是从服务器上获取的。如果频繁访问该网站，那么这些外部资源就没有必要反复从服务器获取。可以使用缓存先存起来（就是存在本地磁盘上了），从而提高访问效率。
  >
  > 可以通过 ctrl +F5 强制刷新页面，强制浏览器重新获取 css 文件。

## 四、代码风格

### 1.样式风格

- 紧凑风格

  ```html
  p { color: red; font-size: 30px;}
  ```

- 展开风格

  ```html
  p {
      color: red;
      font-size: 30px;
  }
  ```

### 2.样式大小写

虽然 css 不区分大小写，但我们开发时统一使用小写字母

### 3.空格规范

- 冒号后面带空格
- 选择器和 "{" 之间也有一个空格
