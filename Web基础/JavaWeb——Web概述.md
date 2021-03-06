> 已经很久没有更新博客了，过年忙着吃喝玩乐，就怠惰了一小下下？幸好这学期新开的课程都比较有趣——Java Web和Android。至少对于我自己来说，既充满挑战，又富有趣味。



![](https://upload-images.jianshu.io/upload_images/7896890-ca84d140e887c28f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



## ——【1.Web概述】——
#### 什么是Web?
Web在计算机网页开发设计中就是网页的意思。网页是网站中的一个页面，我们平常浏览网站时，看到的都是一个一个的页面，通常它们都是**HTML**格式的。网页可以展示文字、图片、媒体等内容，而这些都是需要通过浏览器来阅读。


#### Web应用程序的工作原理？
Web应用程序大体上可以分为两种，**静态网站**和**动态网站**。

早期的Web应用主要是静态页面的浏览，即静态网站。这些网站使用**HTML**描写，通常来说随着html代码的生成，页面的内容和显示效果就基本上不会发生变化了——除非你修改页面代码。这些代码放在Web服务器上，用户使用浏览器通过**HTTP协议**请求服务器上的Web页面，服务器上的Web服务器接受到用户的请求处理后，再发送给客户端浏览器，显示给用户。整个过程就像下图：

![静态网站的工作流程](https://upload-images.jianshu.io/upload_images/7896890-91273d9ca08bd7f7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

而动态网页则不然，页面代码虽然没有变，但是显示的内容却是可以随着时间、环境或者数据库操作的结果而发生改变的。这些网站通常使用**HTML**和**动态脚本语言（入JSP、ASP或者是PHP等）**编写，并将编写后的程序部署到Web服务器上，由Web服务器堆动态脚本代码进行处理，并转化成浏览器可以解析的**HTML**代码，返回给客户端浏览器，显示给用户。

> **值得一提的是：**动态网页并非是那些带有动画效果的网页，而是指具有交互性、内容可以自动更新，并且内容会根据访问的时间和访问者而改变的网页。这里所说的交互性是指网页可以根据用户的要求动态改变或响应。
> 由此可见，静态网页就像是老式的手机，只能使用系统自带的铃声和功能，而动态网页就像是现代的手机，可以自行添加/删除或者说更改铃声和其他一些设置。

![](https://upload-images.jianshu.io/upload_images/7896890-9d622d90b9c1182d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## ——【2.Web的发展历程】——


自从1989年由 **Tim Berners-Lee(蒂姆·伯纳斯·李)** 发明了 **World Wide Web** 以来，Web 主要精力了3个阶段，分别是静态文档阶段（指代 Web 1.0）、动态网页阶段（指代 Web 1.5）和 Web 2.0 阶段。

#### ① 静态文档阶段

处理静态文档阶段的 Web ，主要是用于静态 Web 页面的浏览。用户通过客户端的 Web 浏览器可以访问 Internet 上各个 Web 站点。在每个 Web 站点上，保存着提前编写好的 HTML 格式的 Web 页，以及各 Web 页之间可以实现跳转的超文本链接。通常情况下，这些 Web 页都是通过 HTML 语言编写的。由于受低版本 HTML 语言和旧式浏览器的制约，Web 页面只能包括单纯的文本内容，浏览器页只能显示呆板的文字信息，不过这已经基本满足了建立 Web 站点的初衷，实现了信息资源共享。

随着互联网技术的不断发展以及网上信息呈几何倍数的增长，人们逐渐发现手工编写包含所有信息和内容的页面，对人力和物理都是一种极大的浪费，而且几乎变得难以实现。另外，这样的页面也无法实现各种动态的交互功能。这就促使了 Web 技术进入了发展的第二阶段——动态网页阶段。

#### ② 动态网页阶段

为了克服静态页面的不足，人们将传统单机环境下的编程技术与 Web 技术相结合，从而形成新的网络编程技术。网络编程技术通过在传统的静态网页中加入各种程序和逻辑控制，从而实现动态和个性化的交流与互动。我们将这种使用网络编程技术创建的页面称为动态页面。动态页面的后缀通常是**.jsp、.php、和.asp**等，而静态页面的后缀通常是**.htm、.html和.shtml**等。

#### ③ Web 2.0 阶段

随着互联网技术的不断发展，又提出了一种新的互联网模式——Web 2.0。这种模式更加以用户为中心，通过网络应用（ Web Applications ）促进网络上人与人间的信息交换和协同合作。

Web 2.0 技术主要包括：博客（ BLOG ）、微博（ Twitter ）、维基百科全书（ Wiki ）、即时信息（ IM ）等。

![](https://upload-images.jianshu.io/upload_images/7896890-cdcdf462b4a89f14.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## ——【3.网络程序开发的体系结构】——

随着 Web 2.0 时代的到来，互联网的网络架构已经从传统的 C/S 架构转变为更加方便、快捷的 B/S 架构，B/S 架构大大简化了用户使用网络应用的难度，这种人人都能上网、人人都能使用网络上提供的服务的方法也进一步推动了互联网的繁荣。

> 理解 C/S 和 B/S 可以通过一些实际的例子。C/S 就像是桌面 QQ 等一些**运行在桌面的程序，**，在**服务端主要就是一个数据库，把所有业务逻辑以及界面的渲染操作交给客户端**去完成。而 B/S 就是我们的浏览器，**把业务逻辑交给服务端完成，客户端仅仅只做界面渲染和数据交换。**

B/S 架构带来了以下两个方面的好处：

- **客户端使用同一的浏览器（ Browser ）。**由于浏览器具有统一性，它不需要特殊的配置和网络连接，有效的屏蔽了不同服务提供商提供给用户使用服务的差异性。另外，最重要的一点，浏览器的交互特性使得用户使用它非常简便，而且用户行为的可继承性非常强，也就是用户只要学会了上网，不管使用的是哪一个应用，一旦学会了，在使用其他互联网服务时同样具有了使用经验，因为它们都是基于同样的浏览器操作界面。

- **服务端（ Server ）基于统一的 HTTP 。**和传统的 C/S 架构使用自定义的应用层协议不同，B/S 价格使用的都是统一的 HTTP。使用同一的 HTTP 也为服务提供商简化了开发模式，使得服务器开发者可以采用相对规范的开发模式，这样可以大大节省开发成本。由于使用统一的 HTTP，所以基于 HTTP 的服务器就有很多，如 **IIS、Tomcat** 等，这些服务器可以直接拿来使用，不需要服务开发者单独来开发。不仅如此，连开发服务的通用框架都不需要单独开发，服务开发者只需要关注提供服务的应用逻辑，其他一切平台和框架都可以直接拿来使用，所以 B/S 架构同样简化了服务器提供者的开发，从而出现了越来越多的互联网服务。

![CDN 架构图](https://upload-images.jianshu.io/upload_images/7896890-509e8e690f29d89f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


#### B/S 网络架构概述

B/S 网络架构从前端到后端都得到了简化，基于统一的应用层协议 HTTP 来交互数据，与大多数传统 C/S 互联网应用程序采用的长连接的交互模式不同，**HTTP 采用无状态的短连接的通信方式，**通常情况下，一次请求就完成了一次数据交互，通常也对应一个业务逻辑，然后这次通信连接就断开了。采用这种方式是为了能够同时服务更多的用户，因为当前互联网应用每天都会处理上亿的用户请求，不可能每个用户访问一次后就一直保持这个连接。

基于 HTTP 本身的特点，目前的 B/S 网络架构大多采用 **[CDN](https://baike.baidu.com/item/CDN/420951)** 的架构设计（如上图），既要满足海量用户的访问请求，又要保持用户请求的快速响应，所以现在的网络架构也越来越复杂。

当一个用户在浏览器里输入 *www.taobao.com* 这个 URL 时，将会发生很多操作。首先它会请求 DNS 吧这个域名解析成对应的 IP 地址，然后根据这个 IP 地址在互联网上找到相对应的服务器，向这个服务器发起一个 get 请求，由这个服务器决定返回默认的数据资源给访问的用户。在服务器端实际上还有很复杂的业务逻辑：服务器可能有很多台，到底指定哪一台服务器来处理请求，这需要一个负载均衡设备来平均分配所有用户的请求；还有请求的数据是存储在分布式缓存里还是一个静态文件中，或是在数据库里；当数据返回浏览器时，浏览器解析数据发现还有一些静态资源（ 如 CSS 、JS 或者图片 ）时又会发起另外的 HTTP 请求，而这些请求很可能会在 CDN 上，那么 CDN 服务器又会处理这个用户的请求，大体上一个用户请求会设计这么多的操作。每一个细节都会影响这个请求最终是否会成功。

> 不管网络架构如何变化，时钟有一些固定不变的原则需要遵守。
> - **互联网上所有资源都要用一个 URL 来表示。**URL 就是同意资源定位符，如果你要发布一个服务或者一个资源到互联网上，让别人能够访问到，那么你首先必须要有一个在世界上独一无二的 URL 。**不要小看这个 URL ，它几乎包含了整个互联网的架构精髓。**
> - **必须基于 HTTP 与服务端交互。**不管你要访问的事国内的还是国外的数据，是文本数据还是流媒体，都必须按照套路出牌，也就是都得采用统一打招呼的方式，这样人家才会明白你要的是什么。
> - **数据展示必须在浏览器中进行。**当你获取到数据资源后，必须在浏览器上才能恢复它的容貌。

> 只要满足上面的几点，一个互联网应用基本上就能正确地运行起来了，当然这里面还有很多细节。


#### 参考资料：
①《Java Web 程序设计 慕课版——明日科技·出品》
②《深入分析Java Web技术内幕——许令波 著》


---

> 欢迎转载，转载请注明出处！   
> 简书ID：[@我没有三颗心脏](https://www.jianshu.com/u/a40d61a49221)  
> github：[wmyskxz](https://github.com/wmyskxz/)  
> 欢迎关注公众微信号：wmyskxz
> 分享自己的学习 & 学习资料 & 生活
> 想要交流的朋友也可以加qq群：3382693