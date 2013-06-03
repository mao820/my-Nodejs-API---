my-Nodejs-API---
================

personal reading Node.js API
nodeJS module address:https://github.com/joyent/node/wiki/modules

about this document(关于这篇文档)
   .本文的最终目的是希望读者能够全面的了解NodeJS, 无论是从一个参考还是一个概念的角度来看, 接下来的每个部分都会描述一个内
   置模块或者一个高水平的概念。
   .在适当情况下的方法类型、属性参数、参数提供给的时间处理机制都详细的列举在主题标题栏下面。
   .每个.html文件都有一个包含相同信息相对应.json结构化文件, 这个特征尚处在试验阶段, 并有意于文档对于IDE编程环境或者其它工
   具的可编程化的事情。
   .每个.html和.json文件都是基于nodeJS源码文件 树目录结构 doc/api/下面 .markdown file, 这个.markdown file 是通过源代码
   中的 tools/doc/generate.js 生成的。这个HTML模板位于 doc/template.html。

Stability index(稳定性指数)
   .通过这篇文档, 你会看到每一种稳定性指数的适应性, NodeJS将会一直有些改变, 它成熟、稳定的部分将会比其它地方更加的稳定。
   一些已经被证明是可信赖的部分, 基本上不会在改变了, 其它的一些被标记为new、experimental、或者进程设计中已经被证明是危
   险性的。
   所有稳定性指数列表如下：
   stability 0: Deprecate(弃用)
       这个特征是最近才介绍的, 标记了这个指数的对象表式将在未来的版本中改变或者移除。请尝试用一下这个指数并提供反馈。
       如果它标记了一个对你来说很有用的案例, 请告诉Node core team
       (if it addressess a use-case that is importent to you, please tell Node core team)
   
   stabiliy 1: experimental(实验性的)
       
