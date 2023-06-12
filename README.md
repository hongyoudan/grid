# 使用 HTML 和 CSS 实现图片宫格布局

在本文中，我们将介绍如何使用 HTML 和 CSS 实现图片宫格布局，实现3行3列的效果。

首先，在 HTML 中，我们需要定义一个 div 元素作为容器，并使用 grid-container 和 grid-item 类名，然后使用 repeat(3, 1fr)
来定义每行的列数，即 3 列。同时，为了让图片不会重叠，我们还需要使用 grid-gap 属性来设置间距。

```html

<div class="grid-container">
```

然后，在 CSS 中，我们需要定义 grid-container 元素，并使用 display: grid 将其转换为弹性盒子，然后使用 grid-template-columns 和
grid-gap 来定义每行的列数和间距。

```css
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 10px;
}
```

接下来，我们需要定义每个 grid-item 元素，使用 display: flex 来将其转换为弹性单元格，然后使用 align-items: center 和 margin:
10px 来设置元素的水平和垂直居中以及外边距。

```css
.grid-item {
    display: flex;
    align-items: center;
    margin: 10px;
}
```

最后，我们需要将图片插入到每个 grid-item 元素中，并使用 width: 100% 来让图片充满整个单元格。

```css
.grid-item img {
width: 100%;
}
```

经过上述步骤后，我们就可以得到一个3行3列的图片宫格布局。
