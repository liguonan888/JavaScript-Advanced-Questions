# CSS 相关

*  请说明一下BFC，怎么实现BFC
* 常见选择器，以及他们的优先级
* position有哪些属性
* 隐藏元素有哪些方式:
  * display: none：渲染树不会包含该渲染对象，因此该元素不会在页面中占据位置，也不会响应绑定的监听事件。
  * visibility: hidden：元素在页面中仍占据空间，但是不会响应绑定的监听事件。
  * opacity: 0：将元素的透明度设置为 0，以此来实现元素的隐藏。元素在页面中仍然占据空间，并且能够响应元素绑定的监听事件。
  * position: absolute：通过使用绝对定位将元素移除可视区域内，以此来实现元素的隐藏。
  * z-index: 负值：来使其他元素遮盖住该元素，以此来实现隐藏。
  * clip/clip-path ：使用元素裁剪的方法来实现元素的隐藏，这种方法下，元素仍在页面中占据位置，但是不会响应绑定的监听事件
  * transform: scale(0,0)：将元素缩放为 0，来实现元素的隐藏。这种方法下，元素仍在页面中占据位置，但是不会响应绑定的监听事件。
* display:none与visibility:hidden的区别
* 盒子模型
* 替换元素的概念
* z-index属性在什么情况下会失效
 * 父元素position为relative时，子元素的z-index失效。解决：父元素position改为absolute或static；
 * 元素没有设置position属性为非static属性。解决：设置该元素的position属性为relative，absolute或是fixed中的一种
 * 元素在设置z-index的同时还设置了float浮动。解决：float去除，改为display：inline-block；
* 剩下的参考 链接： https://juejin.cn/post/6905539198107942919#heading-20

# JS相关
- 说下事件循环
- 输出什么 
  ```javascript
  new Promise((resolve, reject) => {
      console.log("1");
      resolve();
    }).then(() => {
      console.log("2");
      new Promise((resolve, reject) => {
           console.log("3");
           resolve();
       })
       .then(() => {
       console.log("4“);
       })
       .then(() => {
       console.log("6");
       });
   })
   .then(() => {
    console.log("5");
   });

  ```
  - map和forEach的区别
  - async和defer
  - 怎么判断NaN 
  -   forin和forof区别，对象怎么使用forof遍历
  -   Symbol的用途
   - Function.__proto__ === ?
  - 说一下继承的6种方法的优劣点
   -  sort方法内部的排序算法？
- 还有其它常见的比如0.1 +0.2 等常见问题也问过

    
# 其它
- webpack 优化
- 说说自己工作中最难的项目、比如在里面的角色、怎么解决的、用了什么技术等等
- 说一下从输入url到看到页面后中间发生了什么（只需要说明网络部分）
-  简述一下浏览器渲染原理【依次按（css）dom-样式计算-布局-绘制-合成-添加事件】的角度去说
 - http缓存最佳实践
- 说一下https的原理
  -说一下对http2.0的理解
- 移动端自适应方案
- 实现一个事件中心
- 阐述一下react Fiber
- vue2.x 版本的缺陷，它如何处理数组方法的
- vue2.x的nextTick实现
- new Vue 发生了什么
- react或者Vue如何做优化
- redux的工作原理，手写compose？
- redux和mobx区别？
- 说一下react 的hooks和类组件对应的生命周期
- 为什么说vue是渐进式的框架
- 在SSR的服务端怎么处理某些需要在挂载组件后执行的第三方库
- vue中watch和computed的区别
- 说一下常见的设计模式
- Vue 3.0 的优化点（diff算法、编译、静态提升、依赖收集等方面去说明）
- 跨端的本质是什么

# 算法
- 公共前缀和
- lru算法
- 最长递增子序列
- 快速排序
- 股票获利问题（动态规划）
- 链表翻转
- 二分查找