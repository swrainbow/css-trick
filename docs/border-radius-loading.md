# 巧用css圆角实现有点意思的加载动画 

?> 掘金原文链接：:point_right: [链接](https://juejin.cn/post/6909281076368293902)

<vuep template="#border-width"></vuep>

<script v-pre type="text/x-template" id="border-width">
<style>
  main{
    width: 100%;
    display: flex;
  }
  .main > .w1 {
    border:100px solid #f3f3f3;
    border-radius:50%;
    border-top:100px solid #2842d8;
}
  .main > .w2 {
    border:100px solid #f3f3f3;
    border-radius:50%;
    border-top:100px solid #2842d8;
    border-right:100px solid #CDB540;
    border-bottom:100px solid #c05235;
    border-left:100px solid #61c570;
    margin-left:300px;
}

</style>
<template>
  <main class="main">
    <div class="w1"></div>
    <div class="w2"></div>
  </main>
</template>
<script>
</script>
</script>

# 添加动画效果

<vuep template="#border-width2"></vuep>

<script v-pre type="text/x-template" id="border-width2">
<style>
  .main2{
    width: 100%;
    display: flex;
  }


  .main2 > .w3 {
    border:100px solid #f3f3f3;
    border-radius:50%;
    border-top:100px solid #2842d8;
    animation:rotate 2s linear infinite;

}
  .main2 > .w4 {
    border:100px solid #f3f3f3;
    border-radius:50%;
    border-top:100px solid #2842d8;
    border-right:100px solid #CDB540;
    border-bottom:100px solid #c05235;
    border-left:100px solid #61c570;
    margin-left:200px;
    animation: rotate 2s linear infinite;
}
  @keyframes rotate {
    0% {transform: rotate(0deg)}
    100% {transform: rotate(360deg)}
  }

</style>
<template>
  <main class="main2">
    <div class="w3"></div>
    <div class="w4"></div>
  </main>
</template>
<script>
</script>
</script>


# 改变图案

<vuep template="#border-width3"></vuep>

<script v-pre type="text/x-template" id="border-width3">
<style>
  .main3{
    width: 100%;
    display: flex;
  }


   .main3 > .rotate-animate {
        border:16px solid #f3f3f3;
        border-radius:50%;
        border-top:16px solid #2842d8;
        width:100px;
        height:100px;
        animation:rotate 2s linear infinite;
    }
    .main3 > .rotate-animate.fill-color {
        margin-left: 200px;
        border-color: #2842d8 #d1b516 #cf4928 #27c965;
    }
  @keyframes rotate {
    0% {transform: rotate(0deg)}
    100% {transform: rotate(360deg)}
  }

</style>
<template>
  <main class="main3">
    <div class="rotate-animate"></div>
    <div class="rotate-animate fill-color"></div>
  </main>
</template>
<script>
</script>
</script>