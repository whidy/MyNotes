使用WORDPRESS已经有很多年了,作为一个以技术内容为主的网站,经常会在文章内引用到各种语法的代码,在wordpress插件管理中,我们同样能够找到很多关于语法高亮的插件,有的十分完美,体积却异常庞大,比如我之前使用的"Crayon Syntax Highlighter",若果博主们对自己的服务器很有信心,又喜欢强大的配置管理,这款插件实在是省事,可是我总觉过于臃肿,因为很多功能用不到,于是后来我找到了另一个插件"SyntaxHighlighter Evolved",这款插件相对来讲很简洁,并且它所使用的高亮JS是很多大型网站都在用的,可是不知道为什么我这里看起来感觉怪怪的,并且它使用起来需要用到类似[html][/html]的标签,如果一旦放弃使用这个插件,恐怕就杯具了.虽然之前经过慎重考虑,选用了此插件,但是高亮效果感觉并不满意,最终寻找到了或许更好的或说更适合我的"高亮插件"--"Highlight.js"!

今天我就来简单介绍一下如何使用这个Highlight.js(如果喜欢自己琢磨,可以直接访问官方网站[highlight.js](http://highlightjs.org/)查看相关说明)

当然我也是看了官方文档说明,总结给懒人看的.

首先,既然是使用它,那必须是需要一个highlight.js了,这个js可以自定义生成,这一点非常适合我,毕竟我只是一个小小小小的前端工作者,我只需要高亮显示html,css,js,json,最多加个php,sql了.于是,在这里,自定义配置这个js[Custom package](http://highlightjs.org/download/),此处勾上自己需要的,然后点击Download按钮,很快一个zip文件就下载好了,这便是我们需要的所有文件.

然后,提取压缩包内的"highlight.pack.js"和"styles"目录,放在一个我稍后想要测试的效果的文件夹中,例如testHighlight,并创建一个测试用的index.html,那么该目录内就有index.html,highlight.pack.js和styles目录了,文件准备妥当,进行下一步.

最后,编辑index.html,按照说明我做了个[DEMO](),引用的是官方的示例代码,需要说明的是,我这里没有把所有的css文件放入styles目录,中间删除了大量的我不会用到的样式,省略,大家可自行通过官方[live demo](http://highlightjs.org/static/test.html)来取舍适量的样式.我这个demo中有个小问题,关于引用html的高亮代码时,由于嵌套关系,他会解析成其他的内容,于是只好将标点其转换成字符编码后,才可正常预览.

于是乎,关于本地静态页面中的highlight.js就算测试完成.接下来我测试整合入wordpress后的效果.
