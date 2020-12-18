# 关于 hsl
![hsl](/static/hsl-color-wheel.png)

?>要理解HSL颜色，你首先需要从另一个角度来理解颜色。注意观察上面的色盘，你可以看到红、绿和蓝三种颜色。红色在最是那干嘛，被设置为0度，绿色是120度，蓝色是240度。它们将色盘分为三个部分。在它们的中间分别是黄色、青色和洋红（CMYK颜色系统）。它们的角度分别为60度、180度和300度。

?>从色盘的顶部开始顺时针方向旋转，是彩虹的七彩颜色。从60度开始，分别是：黄色、绿色、青色、蓝色、洋红和红色。

?>HSL颜色就是指上面颜色色盘中的多少度的颜色值。

?>例如，紫色在蓝色（240°）和洋红（300°）之间，所以他的HSL颜色是hsl(270,100%,50%)。如果想要紫色偏蓝，就要往色盘蓝色方向移动角度值，得到hsl(255,100%,50%)。

?>你会注意到角度后面还有两个百分比的值，第一个值是颜色的饱和度，也就是值颜色的“强度”。在色盘的最外层，颜色的饱和度为100%，最外层的颜色是最有“色彩”的。色盘越往中心移动颜色越灰。所以饱和度也可以理解为：颜色距离灰色有多远？HSL颜色的饱和度为0%时就都变为相同的灰色。

## HSL饱和度值和亮度
<vuep template="#hslsaturation"></vuep>
<script v-pre type="text/x-template" id="hslsaturation">
<style>
  main{
    width: 100%;
    display:flex;
    flex-direction:column;
  }
  .hsl span {
    display: inline-block;
    height: 160px;
    width: 160px;
    text-align: center;
    float: left;
    font-size: 1.2rem;
    padding-top: 60px;
    margin-top:20px;
    }
    .hsl2 span{
        display: inline-block;
        height: 160px;
        width: 160px;
        text-align: center;
        float: left;
        font-size: 1.2rem;
        padding-top: 60px;
        margin-top:20px;
    }

</style>
<template>
  <main class="main">
    <div class="hsl">
        <h5>HSL饱和度值: hsl(45,x%,50%)</h5>
        <span style="background-color:hsl(45,0%,50%);color:#fff">hsl(45,0%,50%)</span>
        <span style="background:hsl(45,25%,50%)">hsl(45,25%,50%)</span>
        <span style="background:hsl(45,50%,50%)">hsl(45,50%,50%)</span>
        <span style="background:hsl(45,75%,50%)">hsl(45,75%,50%)</span>
        <span style="background:hsl(45,100%,50%)">hsl(45,100%,50%)</span>
    </div>
    <div class="hsl2">
        <h5>HSL亮度值: hsl(90,100%,x%)</h5>
        <span style="background:hsl(90,100%,0%);color:#fff">hsl(90,100%,0%)</span>
        <span style="background:hsl(90,100%,25%)">hsl(90,100%,25%)</span>
        <span style="background:hsl(90,100%,50%)">hsl(90,100%,50%)</span>
        <span style="background:hsl(90,100%,75%)">hsl(90,100%,75%)</span>
        <span style="background:hsl(90,100%,100%)">hsl(90,100%,100%)</span>
    </div>
  </main>
</template>
<script>
</script>
</script>

?> HSL颜色的两个百分比值必须同时包含饱和度和亮度值才能正常显示。


当你熟悉了上面色盘的颜色分布的时候，你会发现在CSS中使用HSL颜色会比使用RGB颜色更加容易和便于管理。有时候，使用HSL颜色会有一些优势，这个话题我们将在下一篇文章中介绍。