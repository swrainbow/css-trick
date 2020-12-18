
# 关于 CSS

作为一名Web开发者，CSS是必备技能之一，总结下工作中遇到的CSS问题，形成文档，希望能为其他同学提供一定的参考！

在 MDN 中 [CSS](https://developer.mozilla.org/zh-CN/docs/Web/CSS) 的定义：

?> 层叠样式表 (Cascading Style Sheets，缩写为 CSS），是一种样式表语言，用来描述 HTML 或 XML（包括如 SVG、XHTML 之类的 XML 分支语言）文档的呈现。CSS 描述了在屏幕、纸质、音频等其它媒体上的元素应该如何被渲染的问题。

<!-- 笔者眼中的 CSS 定义：

?> 一门给予用户视觉上愉悦的“语言”，一门值得web开发者不断探索的语言。 -->

## 原则

减少代码重复，保持代码的DRY

```css
/* bad~bad~bad~ */

tips {
  color: #f4f0ea;
  border: 1px solid #f4f0ea;
}
tips:before {
  border-left-color: #f4f0ea;
}

/* good~good~good~ */

tips {
  color: #f4f0ea;
  border: 1px solid currentColor;
}
tips:before {
  border-left-color: inherit;
}
```

合理使用简写

```css
/* bad~bad~bad~ */

div {
  border-width: 2px 2px 2px 0;
}

/* good~good~good~ */

div {
  border-width: 2px; 
  border-left-width: 0;
}
```

适当的过渡效果

```css
/* bad~bad~bad~ */

input:not(:focus) + .popTips{
  display: none;
}

input:focus + .popTips{
  display: block;
}

/* good~good~good~ */

input:not(:focus) + .popTips{
  transform: scale(0);
  transition: transform .25s cubic-bezier(.25, .1, .25, .1);
}

input:focus + .popTips{
  transform: scale(1);
  transition: transform .4s cubic-bezier(.29, .15, .5, 1.46);
}
```

## 色彩

色彩可以参考同花顺UI规范。
[链接](http://datav.iwencai.com/resource/page/index.html#/hxmui-doc?markpath=%2F01.Mobile%2F00.Basic%2F01.%E8%89%B2%E5%BD%A9Color.html)
![color](https://u.thsi.cn/imgsrc/neican/d7ff7b8b3bd7226b0fd56b0c97b60ae6.png)

!> 文档中的示例样式兼没有添加浏览器前缀做兼容，建议使用Chrome，Firefox等主流浏览器访问，在生产环境中请使用[Autoprefixer](https://www.npmjs.com/package/autoprefixer)做兼容处理。
