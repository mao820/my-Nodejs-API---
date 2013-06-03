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
       被这个指数标记的对象：表示了此对象是有问题的, 而且已经计划改变。请不要信任此对象, 用了有此标记的对象将会导致警告,
       基本上不会在向后兼容。
   
   stabiliy 1: experimental(实验性的)
       这个特征是最近才介绍的, 标记了这个指数的对象表式将在未来的版本中改变或者移除。请尝试用一下这个指数并提供反馈。
       如果它解决了一个对你来说很有用的案例, 请告诉Node core team。
       
   stabiltiy 2: Unstable(不稳定的)
       该API是在沉淀的过程中, 但尚未有足够的现实世界中的测试被认为是稳定的。如果合理，将保持向后兼容。
   
   Stability 3: Stable(稳定的)
       该API已经被证明是令人满意的, 但是底层的代码清理会带来轻微的改变。肯定会保持向后兼容。
       
   Stabiltiy 4: Frozen(冻结)
       该API已经在产品中进行了最终测试, 基本永远不会改变。
   
   Stability 5: Locked(锁定)
       除非严重的Bug被发现, 这篇区域的代码将永远不会改变。请不要试图在这个区域进行建议, 这将会被拒绝。

JSON Output
   Stability 1: Experimental(实验性的)
       每个markdown 下面的 HTML文件都会拥有一个有着相同信息的JSON文件, 
       这个特征是在node v0.6.12版本中刚加入 it's experimental
      
Synopsis(简介)
   利用Node 部署的一个简单胡响应"helloworld"的web服务器的例子：
       var http = require("http");
       http.createServer(
         function(request, response) {
           responseWriteHead(200, {'Content-Type': 'text/plain'});
           response.end("hello world\n");
         }
       ).listen(8124);
       console.log('Server running at http://127.0.0.1:8124/');
   运行这个服务, 把代码放入一个名为example.js 的文件中, 用Node program 去执行它
     > node example.js
     Server running at http://127.0.0.1:8124/
   所有这个文档的例子都能类似的执行。

Global Objects(公共对象)
   这些object 在所有模块中都是可见的, 一些Objects实际上不是在全局代码里, 单是在模块代码里, 这些将会被注意。

global
    .{Object}the global namespace object(全局的命名空间object)
    在浏览器：最高级别的范围就是global scope, 那就意味着在浏览器端 如果你在全局范围内定义一个变量它将是一个全局变量
    单是在Node范围内这将是不同的, 在Node中最高级别的范围不是global; 定义一个变量在某一个Nodule Module, 那这个变量将
    属于这个Node Module。


       
