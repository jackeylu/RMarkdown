## 废话

上周五，在南开河畔吹牛时，我对友人说，有一位朋友，必然将被科技史记住。

十年后，基于R+Markdown的科技写作方式将成为主流。而这一切，少不了来自这位朋友的重要开源贡献。他给这条生态链补上了最重要的一环。他，就是yihui。

好吧，观点摆出来了，趋势来临之际，总是人人觉得与自己没有关系。现在，让我讲清楚，R+Markdown与你可能有什么关系。逻辑结构如下：

* 写作会碰到什么难题？Markdown如何解决的？它为什么一定比Word强？
* 科技写作会碰到什么难题？Markdown+R如何解决的？它为什么一定比LaTex强？
* 如何学习Markdown+R？
* 示范


## 1. 写作与Markdown

### 1.1 写作会碰到什么难题？

写作一般而言，会碰到这么一些难题：

* 难以专心：写Word文档的时候，我们经常浪费大量时间在word本身上，比如找借口，ft，word又出问题了，又要升级了，哈哈，可以偷懒了；
* 浪费力气在排版上：使用word时，我们会花费大量力气去排版，试图让文档变得漂亮一些
* 难以自动的版本跟踪：每一位自杀的写作者的电脑文档里面，都必然有从V1.0到V20.0的无数个Word文档
* 难以共同协作：想想你让一位合作的编辑帮你改书有多么痛苦，一个word文档来，一个word去，难用的修订功能，你就理解了；

从2008年开始，我抛弃Word写作，几年来，几本书、十万字以上的长文档，几乎只是用word在最后做个转换与扫尾工作。刚开始是使用google doc，然后当[Markdown](http://en.wikipedia.org/wiki/Markdown)出现之后，毫不犹豫转到它上面来了。我的博客上，关于markdown鼓吹的文章已经足够煽情了。这里，就不再煽情。

### 1.2 Markdown是什么？

它实际上是个非常简单、非常容易学习的语法。这个语法简单到每个人都可以在5分钟以内学会。

更重要的是，语法所有要素，是与写作的习惯一脉相承的。比如：

* 要写引用了，就是这么写：[豆瓣](http://www.douban.com)
* 要引用一段文字，就是直接 >后面写引用
* 3个#号表示标题三级别，2个表示标题二级别。例如：###  ##，分别就代表标题三、标题二
* 要写列表了，就直接* * * ，分行下来
* 要强调什么内容了，直接写**强调的内容**

一切就这么简单。Markdown之所以在被我们鼓吹之后，越来越流行，不是因为它复杂，而是因为它足够简单。

### 1.3 Markdown如何解决这些难题的，为什么一定比Word强？

更重要的是，Markdown诞生于互联网时代，更是由深谙互联网文本之道的John Gruber等人设计。因为Ruby与github圈的极客们的热捧，从一开始，就建立一个完整的生态链。我们可以粗略看看，Markdown如何解决这些难题的。感兴趣的朋友可以去读我的老文：[理想的写作环境：git+github+markdown+jekyll](http://www.yangzhiping.com/tech/writing-space.html)

####  1.3.1 借助于github解决文档共享与版本自动跟踪问题

word共享难？我的所有文档都放在github或者其他任何支持git版本跟踪服务的服务器上。所以，可以极其方便的共享文档写作过程。看看，最近在与豆瓣友邻协作的一本书的截图：

![P220903450 1](/images/p220903450-1.jpg)

可以清晰地看到，我的所有写作过程，github都可以自动记录下来，从而不再担心写废。而，另一位豆瓣友邻的任何改动、编辑的修订意见，大家都可以实时完成。

#### 1.3.2 Markdown让我们专注写作，而不是关注排版

Markdown语法因为格式足够简单，所以，导致开发者非常容易生成非常漂亮的版式。在用Word写作的时候，经常浪费大量时间去思考排版，但是因为markdown足够简单，你无法思考排版，也没必要思考，所以，逼自己集中精力写作。

这是我在写的一篇长篇科普文章。大家可以看到，我一边写，一边就是非常漂亮的稿件出来了。同样，值得骄傲的是，这个写作软件，在世界范围，广受好评的[Mou](http://mouapp.com/)软件，也是另一位国人友人开发的:D 我们为这个时代，安静的创作者而骄傲。

![P220903450 3](/images/p220903450-3.jpg)

## 2. 科技写作与Markdown+R

###  2.1 科技写作会碰到什么难题？

如果你是纯文科生，一辈子写的都是豆瓣小酸文或者诗歌之类的，那么，看完上面这一部分就可以打住了。如果你还有写科技论文或者需要在网站上演示一些代码的需要，则继续往下看。

科技写作与一般写作最大的不同有这么一些地方：

* 数学公式：相信各位写过科学论文的，都会为数学公式的输出头疼不已；
* 格式转换：pdf是通用的，但是有时偏偏需要LaTex原始格式或者word原始格式；
* 参考文献：投稿给不同刊物，往往参考文献要根据对方的格式来调整。

解决这些难题，[LaTex](http://en.wikipedia.org/wiki/LaTeX)是国际科学界，尤其是偏数理类的学科的主流方案之一。当然，因为中国盗版office的流行，导致国内科技论文word更盛行，则是另一码事。word因为近些年在参考文献协作软件、数学公式方面的发力，也逐步成为科技界认同的论文投递标准之一。

每位提到LaTex的人们，常常有两种口气。一种是当做大神来敬仰的，当语言、软件变为传奇，路人皆知它的诞生历史时，于是，众多如你我这类文科生，只有抬头仰望的份了。另一类，则是不屑的口气，我靠，LaTex那么好学，你怎么都学不会！国际期刊都是用这个写的。。。

于是，我等文科生只好在被鄙视的眼光之下，快快走过LaTex。。。

但是，LaTex真的符合人们写作习惯吗？请记住当时的历史。那时的计算机，所见即所得，并不像今天这么流行。那时的计算机，处理能力也不像今天这么强大。更别提什么脚本语言了。

翻出上一份LaTex文档所用的APA模版，大家就知道它有多么坑爹了。。。

![P220903450 4](/images/p220903450-4.jpg)

### 2.2 Markdown+R如何解决的？它为什么一定比LaTex强？

老大，我仅仅是要写一篇论文而已。。。结果，非要让我们成为LaTex教的信徒。这种布局，真的美观吗？它较高的门槛，真的适合我强制推广给大家吗？更别提它的种种不变了。

于是，每位试图解决LaTex的不便，又试图保留它的优点的人们，都走上了一条不归路。

直到有一天，极其熟悉LaTex，也熟悉Markdown的yihui同学，意识到了，LaTex它可以作为最终格式生成。但是，我们中间的写作过程，完全可以用Markdown这么简单明了的语法来写，我们真正需要的，就是一堆数学公式、图表与参考文献而已。前2者，恰恰是R的强项。后者，则留给开源社区，下一步解决。

于是，在他的新作R包knitr中，果断提供了Markdown支持。并说服R社区主流编辑器厂家，开源软件RStudio提供 Markdown支持，从而，在最近诞生了Rmd这种新格式。我们有幸看到这个重要格式的诞生，国人的贡献如此重要。

### 2.3 Rmd 简介

Rmd 格式更详细的描述，去读 yihui 的文档：[自动化报告](https://github.com/yihui/r-ninja/blob/master/11-auto-report.md)

在这里，让我简单说明，如何最快上手Rmd格式。

#### 2.3.1 安装并配置RStudio

下载 [RStudio](http://rstudio.org/) 之后，打开配置选项，如下图所示：

![P220903450 5](/images/p220903450-5.jpg)

然后，进行如下配置：

![P220903450 7](/images/p220903450-7.jpg)

#### 2.3.2 新建Rmd文档

新建一个Rmd文档，然后，默认会出来一些内容，直接Knit HTML，就会生成相应的图片、Markdown文档。

是的，你要的一切图片都有了！这就是 yihui 所推崇的 文学性编程、可重复性概念的神奇。

更重要的是，还保留了对LaTex的无缝兼容。比如，大家可以敲下这段文字：


  The Normal Distribution
	=======================
	
	The normal distribution is defined as follows:
	
	$$latex
	f(x;\mu,\sigma^2) = \frac{1}{\sigma\sqrt{2\pi}} e^{ -\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2 }
	$$
	
	To generate random draws from a normal distribution we use the **rnorm** function:
	
	```{r block1}
	output <- rnorm(1000, 100, 15);
	```
	
	The normal distribution has the typical bell shape:
	
	```{r block2, fig.width=8, fig.height=5}
	ggplot2::qplot(output)
	```

其中，这一段，

	$$latex
	f(x;\mu,\sigma^2) = \frac{1}{\sigma\sqrt{2\pi}} e^{ -\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2 }
	$$

就是直接生成LaTex格式的数学公式！

没有安装RStudio，或者不熟悉R的朋友，可以在我搭建的一个在线演示APP里面，将上述代码，粘贴上去，然后看看神奇的效果！

网址是：[R Markdown App](http://r.psyapp.com/apps/markdown/) 效果如下图所示：

![P220903450 9](/images/p220903450-9.jpg)


### 2.4 这么做，有什么好处呢？

让我细数一下：

####  2.4.1 真正意义上的可重复性研究

发表论文或者审核同事的报告，有个最麻烦的事情，你不知道他的步骤或者计算是否有误。而现在，代码嵌在报告正文中，或者附录在报告末尾。而你，要做的，仅仅是一键生成。。。 这就是真正意义上的可重复性研究！

我写了一个今年指导的一篇社会网络分析论文的例子，大家可以看到：

网址是：[R Markdown App](http://r.psyapp.com/apps/markdown/)

一键生成之后，作者调用的数据、最终生成的报告图片一目了然。

#### 2.4.2 更强大的数学与制图能力

既兼容了LaTex的既有能力，同时，又广泛借助于R自身强大的作图能力。

更重要的是，未来，并不是非要用R语言作图。这个yihui 同学在关于钩子那段的描述已经极其清楚了。

#### 2.4.3 当然，还有，云计算

真正意义上的云计算，尤其是小型云计算，而非类似于各类忽悠的云计算。R+Markdown这种方式是最佳方式。我上述例子中提到的那个APP，就是搭建在云中。同时提供各类REST借口，被我们的Ruby程序员调用。

### 2.5 Markdown格式与LaTex、Word等格式的互转

点这里：[Pandoc](http://johnmacfarlane.net/pandoc/)

## 3. 如何学习Markdown+R？

好了，回到大家最关心的部分。分成两部分，先是如何学习Markdown，其次是如何学习R。

### 3.1 Markdown格式说明

* 参考：[Markdown](http://markdown.tw/)
* 更好的学习办法是直接读zh目录下的范本文件
* 更多资源参考[V2ex节点](http://v2ex.com/go/markdown)

### 3.2 Markdown编辑器

* Mac等平台下推荐Mou
* Windows平台推荐???  
* 可以直接在线通过github撰写与提交Markdown文件，github有自动的版本跟踪功能，不用担心写废与找不到改错的

### 3.3 Windows下的GitHub特别说明

* 如果碰到git、github等与windows不兼容的现象，不建议折腾，而是直接在线提交即可。
* GitHub最近发行了Windows版本，下载地址[在这里](https://github.com/blog/1127-github-for-windows)
* [如何高效利用github](http://www.yangzhiping.com/tech/github.html)

### 3.4 如何学习R

####  3.4.1 Rstudio

* Getting_Started_with_RStudio.pdf

#### 3.4.2 R语言入门读物

* R for SAS and SPSS Users.pdf ： 适合有SPSS基础的朋友
* Analysis of Questionnaire Data with R  ： 适合处理问卷数据的文科生
* 更多参考我的豆列：[技术派心理学](http://book.douban.com/doulist/1222833/)

## 4. 示范

### 4.1 文艺青年

文艺青年看这里：[想得越多越保守](http://xingfuke.net/think-less)

它的后台是我改造的一个在线Markdown写作软件，大家可以看到它的源代码格式，就这么简单：

![P220903450 8](/images/p220903450-8.jpg)

其中，这篇文档用到的语法有：

* ![]接着()  表示图片链接
* 2个##表示标题二
* []接着()表示链接

### 4.2 科学青年

看这里：[如何学习科学：开放科学工具箱](https://github.com/ouyangzhiping/openscience/blob/master/README.md)

点击RAW 即可看到原始格式。这是一个长文档的示范。

### 4.3 技术青年

[R Markdown App](http://r.psyapp.com/apps/markdown/)


