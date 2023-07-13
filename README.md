# animation-study
动画学习库:
[gif动图生成工具](https://www.cockos.com/licecap/);
[css属性浏览器兼容性查询](https://caniuse.com/ciu/index);
[动画库推荐1](https://juejin.cn/post/7069945906518294536);
[动画库推荐2](https://juejin.cn/post/7136894824061501454);

### 基础知识学习
* CSS 动画与 JavaScript 动画的性能 ：[优先使用css动画库，其次js动画库](https://developer.mozilla.org/zh-CN/docs/Web/Performance/CSS_JavaScript_animation_performance)
* [浏览器的回流和重绘](https://juejin.cn/post/6844903569087266823)


#### 一、[Transition](https://developer.mozilla.org/zh-CN/docs/Web/CSS/transition) 
1. 浏览器兼容性

2. 需要事件触发，只有开始和结束状态
原生css:display属性会引起网页回流，不能触发transition
visibility虽然不会引起回流,但是不会触发事件，需要和opacity（其他属性）一起使用

3. 单独设置过渡属性 ``` transition-property: width , visibility; ```
![](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExNWg1OHByNTFiODlpb3Z6aGZiYmx2aWZrODY4bDJqbDAxNmc4aHkybyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/f2aoXetZLbjUWO3doB/giphy.gif)


#### 二、[Animation](https://developer.mozilla.org/zh-CN/docs/Web/CSS/animation-direction)

1. 和transition的区别
transition只可以定义开始和结束两种状态
animation可以定义每一帧的状态

2. animation-fill-mode 执行后保持状态(第一帧与animation-direction有关)
  ``` forwards 保持最后一帧的状态```
  ``` backwards 保持第一帧的状态```

![](https://media1.giphy.com/media/w1WKpB17wN18nsVUGN/giphy.gif)

3. 兼容性问题
  低版本浏览器需要加前缀（animation加前缀，keyframes 也加前缀）

#### 三、 [Vue Transition 组件](https://cn.vuejs.org/guide/built-ins/transition.html)
1. 使用场景

### 动画库

#### 一、[Animate.css](https://animate.style/)
  * 优点：轻量级，简单易上手，兼容性好
  * 缺点：灵活性差，动画实现有限性

1. 基本使用添加**class**
  ``` class="animate__animated animate__zoomIn" ```

2.  css直接使用动画名称(注意设置动画时间)```animation: zoomIn```

3. 修改动画参数
    (1)全局
    ```
    :root {
      --animate-duration: 2s;
      --animate-delay: 0.9s;
    }
    ```
    (2)单独对元素修改
    ``` 
    .test {
      --animate-duration: 2s !important;
    }
    ```

    (3)使用快捷类名
      * Delay classes ```animate__delay-2s ```
      * Slow, slower, fast, and Faster classes 
        ```
          default speed of 1s 
          animate__slow	2s
          animate__slower	3s
          animate__fast	800ms
          animate__faster	500ms
        ```
      * Repeating classes ```animate__repeat-1```

4. 最佳实践以及注意问题
  * Don't animate root elements
  * Always animate **block** or **inline-block** level elements
  * might create scrollbars on your web-thing. **overflow: hidden**
 
#### 二、[animejs](https://animejs.com/)
* 优点：轻量级，简单易用，兼容性较好（IE11及以上），加载速度快
* 缺点： 文档参考案例demo少

2. 使用参考
* [官网](https://animejs.com/documentation/#cssSelector)
* [参考1](https://blog.csdn.net/qq_50497708/article/details/128322505?spm=1001.2101.3001.6650.5&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7ERate-5-128322505-blog-110709995.235%5Ev38%5Epc_relevant_sort_base1&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7ERate-5-128322505-blog-110709995.235%5Ev38%5Epc_relevant_sort_base1&utm_relevant_index=10)
* [参考2](https://www.jianshu.com/p/39fc8a837b31)
