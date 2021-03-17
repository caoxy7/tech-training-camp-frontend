# 基于React和markdown-it实现的简易编辑器

最终还是选用了直接用现成的编译器，光是学习react就花了不少时间。

## v0.5
>只有简单的输入和预览功能，编辑框采用了monaco-editor。但是由于编辑框的使用有点复杂，暂时也没想好合理的办法来实现toolBar功能，暂时搁置。

## v1.0
>思前想后，还是决定再做一遍该项目，不想半途而废。不过编译器还是没用自己实现，原因是编译原理真的好抽象：（

### 预览界面

参考博客[借助Github Page把你的React项目部署到线上环境](https://juejin.cn/post/6844903821995409422)将项目部署到了线上环境，所以可以直接使用。
[Click Here!](https://caoxy7.github.io/tech-training-camp-frontend/)

### 技术栈

1. React
2. React Hooks
3. antd（最后引入了一点，还没使用熟练，所以前面的样式基本还是手写）

### 实现功能

1. 在线编辑与预览
2. 左右窗口同步滚动
3. 顶部功能栏（简陋）

### 待改进的点

1. 代码应该细分为各个组件，由于是第一次上手，就写在一起的方便操作，有时间应该分开一下。
2. css样式没有设计好，最后引入了antd写顶部工具栏，但是没有使得布局融合进已有的样式。
3. 顶部工具栏功能不全
4. 编译器未自己实现
5. 使用脚手架创建项目，后续可以使用以下Webpack重构一下，也相当于学习webpack了
6. hooks功能用的不多，用这个只是为了逃避this指针（雾
7. 真实从零开始，感觉js和react只学了一点点皮毛，用的很不好，也参考了很多别人的代码，自己的东西不够多。

### 明显存在的bug

1. 不存在光标的时候点击顶部工具栏插入会出现很糟糕的情况，推测可以研究下focus属性来解决这个问题，不过还没尝试
2. 使用顶部工具栏插入后不会及时更新预览框效果，需要再输入以触发函数更新预览框，原因排查到是因为我更新预览框的代码是通过`onInput`来监听的，不过目前没想到好的法子来改
3. 有序标签仍会被渲染为无序标签，可能是编译器的问题吧

### 参考博客

参考的博客很多，很多东西都是直接根据别人的来的，而且编译器也没有自己实现，很多功能也存在着bug，感觉从完成项目作业的角度来说还挺失败的，不过还是有学到不少知识，也算是有点收获（希望不要当众处刑我就好2333）.

[100行代码实现基于react的markdown输入+即时预览在线编辑器](https://blog.csdn.net/DeepLies/article/details/78909125):这篇博客教会了我如何实时输入markdown以及实现预览功能
[原生JS控制多个滚动条同步跟随滚动](https://blog.csdn.net/deeplies/article/details/78854032):实现了同步滚动功能，改进成了适合react的代码
[contenteditable 插入及粘贴纯文本内容](https://www.cnblogs.com/_error/p/8872996.html)：实现了在光标处插入文本的功能，根据这个功能实现了顶部工具栏。

### 个人总结

我从1月20号左右下定决心学前端，但正值放寒假，其实也就过了一遍html/css/js，也没有深刻体会到哪些功能有哪些作业，当时也没有动手实践过，所以从训练营开始，即2月24号左右，我差不多算是初学者了。

这一个月一共八次课，学到的知识不可谓不丰富。印象最深的就是css的布局了，弹性盒子和网格布局简直打开了新世界大门，之前看css的时候，弹性盒子看的时候很快就过了，没体会到有什么作用。课程上的时候才发现这东西是真的强大。
除此对position、浮动等属性也了解得更深了。更大的收获还是在于js，const、var、let的区别，显隐式转换等，都对学习js有很大的帮助。不过目前理解的也就是js变量类型的种种知识，其他的都还在慢慢学，光看视频学习果然还是不够，
最近有在看大量的博客，以及动手实践加深理解。

课外我主要学习了一下React组件，顺带着了解了Redux和Webpack，不过这俩仅限于知道是个啥，准备之后再动手实践一下，原因在于感觉这是比较深的东西了，一口吃不成胖子。Router、Hooks也有了解过，其中Hooks挺喜欢的，
虽然官网上说了很多条它的优点，不过我现在印象最深的还是使用起来方便，可以不使用烦人的this指针，以及可以把代码拆分的更小。我对它的理解是能更加有效地帮助程序员的开发，因为它使得代码的逻辑性更强，数据的流动管理更加直观，
React的单向数据流我是很喜欢的，因为它使得代码层次清晰，数据的流动一目了然，不同组件的定位更加明确，使得组件化的开发更加的有效以及后续的测试迭代。学的很浅，理解的也很浅，完全是自己的胡言乱语，最近也有在看别人的看法，
之后想多看看然后自己体会一下再更新自己的理解。

总的来说，虽然项目做得稀烂，要求也没达到，各种东西也只是学了个皮毛，但还是很庆幸很高兴自己学到了东西。虽然代码简陋，偷了不少东西，但是看到这个能用的东西还是很欣慰，虽然它确实很简单。