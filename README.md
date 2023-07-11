# animation-study
动画学习库[gif动图生成工具](https://www.cockos.com/licecap/)

### 浏览器的回流和重绘
[link](https://juejin.cn/post/6844903569087266823)

### transition 
[link](https://yxyuxuan.github.io/2017/08/02/CSS3%E4%B8%ADtransition%E5%B1%9E%E6%8as0%A7/)
1. 浏览器兼容性

2. 需要事件触发，只有开始和结束状态
原生css:display属性会引起网页回流，不能触发transition
visibility虽然不会引起回流,但是不会触发事件，需要和opacity（其他属性）一起使用

3. 单独设置过渡属性
``` transition-property: width , visibility; ```
![](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExNWg1OHByNTFiODlpb3Z6aGZiYmx2aWZrODY4bDJqbDAxNmc4aHkybyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/f2aoXetZLbjUWO3doB/giphy.gif)

