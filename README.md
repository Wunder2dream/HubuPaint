## 基于.net之仿Windows画板设计
	摘要：随着社会的不断发展以及计算机的不断普及，人们对绘图的要求越来越高，对绘图功能也提出了更高更全面的要求。不同年龄不同身份的人，需求有所不同。现在普通用户普遍使用的是Windows系统下自带的Windows画图工具，它可以实现最为基本的画图功能，但使用起来不够灵活，功能也不是很完善。基于此，本设计尝试按照Windows画图工具的设计思想，综合考虑多方面因素，通过c#程序语言开发设计一款基于.Net Framework的功能更为完善、使用起来更为灵活的WinForm窗体画图软件，使其不仅能够达到满足日常画图的需求，且具有便于存储编辑和展示、功耗小、易扩展、界面人性化等优点。
	关键词：c#  .Net Framework  WinForm窗体  画图软件

# 绪论
	随着操作系统不断的更新换代，其自带的画图板界面及功能也在不断变化，例如XP、Vista、Win10，它们画图板的界面布局风格以及功能都有所不同，这表明尽管是简简单单的一个操作系统自带画图板，系统设计人员也没有停止对它的不断研究与探索，他们在不断地寻找更为人性化、更能满足大众需求的设计模式。随着社会的不断发展以及计算机的不断普及，人们对画的要求越来越高，对绘图功能也提出了更高更全面的要求。许多用户由于自身的画图习惯或者是画视觉效果不同，对传统的画图工具可能感觉不是特别满意，就像孩子总是喜欢画可爱型，而成人则画实用的。不同年龄不同身份的人，需求不同。现在大众普遍使用的是Windows系统下自带的Windows画图软件，它可以实现一些简单的基本画图功能，但缺乏灵活性。本次课程设计就是基于Windows画图软件的思想，综合考虑多方面因素，尝试开发一款仿Windows画板，使其能达到满足日常画图的需求，便于存储编辑和展示，且要求功耗小且界面人性化，功能易扩展。课题的研究背景

## 1.1 课题的目的与意义
### 1.1.1课题的目的
	随着社会的快速发展，科技日新月异，各类应用软件开始趋于有偿使用。不收费的应用软件功能简单并且有诸多限制条件；收费的应用软件功能齐全，但价格高昂，往往只有公司专业人士才会使用。这种商业模式无疑给普通用户带来了极大的不便，就拿Windows画板来说，作为Windows操作系统自带的画图软件，它自然不像微软旗下的Visio那样功能齐全，它只能进行最基本的画图操作，而且使用起来也十分的不灵活，难以满足普通用户多方面的需求。因此，我们试图仿照Windows画板设计一款免费的功能更加齐全的画图工具，综合考虑多方面因素，使画图软件能达到满足日常画图的需求，便于存储编辑和展示，且要求功耗小且界面人性化，功能易扩展。
### 1.1.2 课题的意义
	日常生活中，有很多方面都会用到画图来解决阐述一些问题，传统的手工绘图是一项细致、复杂和冗长的劳动，主要是借助三角板、丁字尺、圆规等简单工具，不但效率低、质量差，而且周期长，不易于修改。于是，人们便发明了一种更为高效、高质的绘图技术——计算机绘图软件，它借助于计算机来进行，能简单解决这些问题。计算机绘图软件的发展趋向于用户需求导向，在很多领域中发展迅猛，例如教学演示、软件设计、工程建设、服装设计、影视制作等，由此可见计算机绘图软件俨然成为当今日常生活中不可或缺的一部分。
## 1.2 课题的研究现状
### 1.2.1 国外的研究现状
	国外普及性较高的画图软件有微软的Visio 以及新兴的Lucidchart、Cacoo、Creately、Coggl和Draw.io等，其中微软的Visio是付费软件，下载安装以及“授权”都是问题，而后续的几个都是功能十分强大的在线网络画图工具，无需下载安装即可使用，有提供免费功能，但要进行大型的开发工作，也是要收费的。
### 1.2.2 国内的研究现状
	国内目前普遍使用的画图工具有Windows画板、百度脑图和ProcessOn，其中Windows画板只适合最基本的画图示意；百度脑图仅仅只支持思维导图功能，功能单一；ProcessOn算是国内垂直领域最好用的作图工具了，基本上已经完全实现了其他作图工具的所有功能，而且与其他工具相比，ProcessOn还提供了小组、活动等很多社交性质的功能。

## 1.3 课题的研究内容
	本文通过对Windows操作系统自带的Windows画板的分析和学习，结合实际应用的特点和课程设计的需求，通过c#程序语言开发设计一款基于.Net Framework的功能相较于Windows画板更为完善、使用起来更为灵活的WinForm窗体画图软件，具体研究内容如下：
#### （1）能够绘制点、直线、折线、直角线、多边形、圆、椭圆、圆弧、椭圆弧、任意曲线、圆角矩形、矩形及其字符等多种基本的图形（采用鼠标拖曳法完成）； 
#### （2）实现图形的不同填充模式（单色填充、图案填充）对图形的填充，完成填充颜色的设置与修改（包括预先设置和修改）； 
#### （3）图形绘制时能实现5种以上的线型、1-20之间的任意线宽，基于调色板进行线色选择；
#### （4）能完成对图形的内裁剪与外裁剪；
#### （5）能实现单个或多个图元的选中，且选中后图形成高亮显示且热点被显示出来；
#### （6）能完成图形的组合与打散；
#### （7）能完成图形的对称、旋转、平移、缩放等操作；
#### （8）能实现图元系统的存储、加载及其重绘；
#### （9）能实现撤销与重复功能；
#### （10）能完成图形的多种对齐、图形的檫除；
#### （11）能完成屏幕背景的设置；实现标尺、导向线等功能；
#### （12）能实现图元的复制、剪切、粘贴。
# 软件需求分析
## 2.1 基本图形
	为了满足用户的基本画图需要，我们一共提供了22种基本图形，具体包括直线、曲线、椭圆、矩形、圆角矩形、任意圆弧、任意多边形、等腰三角形、直角三角形、菱形、五六边形、四五六角星、上下左右四个方向的箭头、圆角文本框、折线、直角线。

## 2.2 基本字符
	考虑到用户在绘图过程中，难免会有需要用到字符的时候，对此，我们提供了四种字符形式供用户选择，分别为汉字、字母、数字和符号。

## 2.3 样式选择
	为了避免线条样式的单一，我们提供颜色和线型两种选择。其中，颜色包括固定的颜色盘和允许自定义的调色盘；线型包括线形和线宽。具体介绍如下：
	颜色盘：颜色盘提供了固定的、最基本的十二种颜色；
	调色盘：允许用户自定义颜色；
	线形：线条的形状有五种，分别为直线、虚线、双点划线、点划线和双划线。其中，点线可以用来表示立体线框中可见的轮廓线；虚线可以用来表示立体线框中不可见的轮廓线；点划线、双点划线可以用来表示中心线；
	线宽：线条的宽度为1~20个像素单位；

## 2.4 基本操作

### 2.4.1 文件操作及加载
	用户画图，有时候并不是一次就能完成，往往需要先暂时保存，然后下次再接着绘制。因此，画板必须能够提供存储和再次打开，加载后继续编辑的功能。同时，存储格式决定了加载的速度，无论速度快慢，都应该显示加载的过程，这样才能告诉用户整个加载过程的进度如何，而不是让用户盲等，这样体验效果极其不佳。

### 2.4.2 撤销
	用户画图，绝不是一蹴而就，一帆风顺的，免不了出现各种错误，如若没有撤销功能，那么一旦出错就将前功尽弃，半天的心血化为一滩泡影，这是用户最不希望看到、最不能忍受的，因此必须具备撤销功能。对此，我们提供了两种撤销模式，分别为向前撤销和向后撤销。
	向后撤销：如果用户执行了一步操作后，觉得不满意，便可以通过向后撤销回到上一步
	向前撤销：如果用户撤销当前操作后，又后悔了，那么便可以使用向前撤销，回到撤销前的状态

### 2.4.3 复制、剪切、粘贴
	画图过程中，若需要频繁的使用某一种图形、并对其进行操作是一件非常繁琐的事情，若能直接在原图形上进行拷贝，再进行少量修改，将节省用户不少时间。因此，复制和粘贴这两种功能必不可少。
	剪切是删除和复制的结合体，它不同于删除，因为删除某个图形，那么这个图形便真的不复存在，但剪切相当于是将图形从画板上移到另一个地方保存起来，等到要用的时候，便把它再次取出来，以复制的形式进行粘贴，这也给用户的操作带来了便利。

## 2.5 核心操作

### 2.5.1 图形填充
	图形填充分为直接图形填充和区域填充两种形式，其中前者是选中图形，对图形内部进行填充；而后者则是指定一个闭合的区域，进行填充。相较于前者，后者具有更高的灵活性，但两者均可以通过调色板来选则填充的颜色。

### 2.5.2 画面裁剪
	画面裁剪分为内裁剪和外裁剪两种形式，裁剪框为虚线矩形。其中，内裁剪只保留裁剪框内部的内容，裁剪框外部的内容丢弃；外裁剪只保留裁剪框外部的内容，裁剪框内部的内容丢弃。两种模式均满足裁剪前是一个图形，裁剪后仍是一个图形的“封闭原则”。

### 2.5.3 图形选中
	图形的选中，是为了便于对图形进行各项操作，包括平移、缩放、对称等。因此，为了便于后面的操作，在图形选中这一板块，必须把图形用来进行操作的各个热点显示出来，包括矩形的四个顶点以及四条边的中点（用一个红色虚线矩形框将被选中图形包裹，表示该图形被选中）。

### 2.5.4 组合与打散
	画图过程中，难免会存在需要同时将两个或多个图形一起移动的情形或者用户希望将多个简单的基本图形组合为更为复杂的图形，那么组合与打散便是不可或缺的操作，它给用户大规模操作、自定义图形提供了便捷。

### 2.5.5 对称、旋转、平移、缩放
	画图中最基本的操作莫过于平移、对称、旋转和缩放，它允许用户随意的对图形的大小、位置、方向进行操作，以满足画图的需要，

### 2.5.6 图形的对齐
	要想画图好看，少不了各种形式的对齐，对此，我们提供了三种对齐选择，分别为左对齐、右对齐和居中对齐。

### 2.5.7 图形的檫除
	图形的擦除又可以理解为图形的删除，对于已经操作了很久才发现的无用图形，是无法通过撤销而去除的，这时候就需要手动的擦除某个指定的图形，增加了图形操作的灵活性。

## 2.6 状态选择
	状态选择是为了给用户提供更好的界面效果，方便用户作图。对此，我们提供了三种画板状态，分别为标尺、网格线和状态栏，并且这三种状态用户可以根据自身需要随意组合。
	标尺：在画板周围显示刻度，方便用户衡量图形的大小
	网格线：网格线可以让用户更直观地观察直线是否水平或垂直、多个图形的相对位置和是否对齐
	状态栏：状态栏显示焦点坐标，方便用户掌握鼠标的位置
# 概要设计
## 3.1开发工具选型
	本软件考虑使用C#编程语言进行开发，选用微软公司开发的 Visual Studio 2017集成开发环境作为基础开发工具，使用便于移植的.Net Framework开发平台开发WinForm窗体画图软件。

### 3.1.1 c# 编程语言
	C#是微软公司发布的一种面向对象的、运行于.Net Framework和.Net Core(完全开源，跨平台)之上的高级程序设计语言。并定于在微软职业开发者论坛(PDC)上登台亮相。C#是微软公司研究员Anders Hejlsberg的最新成果。C#看起来与Java有着惊人的相似；它包括了诸如单一继承、接口、与Java几乎同样的语法和编译成中间代码再运行的过程。但是C#与Java有着明显的不同，它借鉴了Delphi的一个特点，与COM（组件对象模型）是直接集成的，而且它是微软公司 .NET windows网络框架的主角。 
	C#是一种安全的、稳定的、简单的、优雅的，由C和C++衍生出来的面向对象的编程语言。它在继承C和C++强大功能的同时去掉了一些它们的复杂特性（例如没有宏以及不允许多重继承），并且C#成为ECMA与ISO标准规范。C#看似基于C++写成，但又融入其它语言如Pascal、Java、VB等，C#综合了VB简单的可视化操作和C++的高运行效率，以其强大的操作能力、优雅的语法风格、创新的语言特性和便捷的面向组件编程的支持成为.NET开发的首选语言。

### 3.1.2 Visual Studio 2017 开发工具
	Microsoft Visual Studio（简称VS）是美国微软公司的开发工具包系列产品。VS是一个基本完整的开发工具集，它包括了整个软件生命周期中所需要的大部分工具，如UML工具、代码管控工具、集成开发环境(IDE)等等。所写的目标代码适用于微软支持的所有平台，包括Microsoft Windows、Windows Mobile、Windows CE、.NET Framework、.NET Compact Framework和Microsoft Silverlight 及Windows Phone。
	Visual Studio是目前最流行的Windows平台应用程序的集成开发环境。最新版本为 Visual Studio 2019 版本，基于 .NET Framework 4.5.2 。
	本次采用的版本是 Visual Studio 2017 ，它是微软于2017年3月8日正式推出的新版本，是迄今为止最具生产力的 Visual Studio 版本。其内建工具整合了 .NET Core、Azure 应用程序、微服务（microservices）、Docker 容器等所有内容。

### 3.1.3 .Net 开发平台
	.Net 是一个通用开发平台，它具有几项关键功能，例如支持多种编程语言、异步和并发编程模型以及本机互操作性，可以支持跨多个平台的各种方案。.Net 开发可以实现包括 .Net Framework、.Net Core 和 Mono。
	.Net 拥有惊人的性能和开发效率，并且拥有数百万的开发者。它允许应用程序在因特网上方便、快捷地互相通信，而不必关心使用何种操作系统和编程语言。从技术层面来说，Microsoft.Net平台主要包括两个内核，即通用语言运行时（Common Language Runtime,简称CLR）和Microsoft.Net框架类库, 它们为Microsoft.Net平台的实现提供底层技术支持。

### 3.1.4 WinForm 控件
	WinForm是 .Net开发平台中对Windows Form的一种称谓。Winform控件灵活、向导明确。它具有以下优点：
#### 1、控件灵活：WinForm控件是指以输入或操作数据的对象。比如ComponentOne是.net平台下对数据和方法的封装。有自己的属性和方法。属性是控件数据的简单访问者。方法则是控件的一些简单而可见的功能。包含在 .NET Framework 中的 Windows窗体类旨在用于 GUI 开发。您可以轻松创建具有适应多变的商业需求所需的灵活性的命令窗口、按钮、菜单、工具栏和其他屏幕元素。Windows窗体为开发人员提供了一套丰富的控件，并且允许开发人员自定义有特色的新控件。
#### 2、数据管理：方便的数据显示和操作：应用程序开发中最常见的情形之一是在窗体上显示数据。Windows窗体对数据库处理提供全面支持。可以访问数据库中的数据，并在窗体上显示和操作数据。
#### 3、向导明确：向用户提供创建窗体、数据处理、打包和部署等的分布指导。
	总之，WinForm 控件功能强大、操作方便并且使用安全。

### 3.1.5 GDI 图形库
	GDI是Graphics Device Interface的缩写，含义是图形设备接口，它的主要任务是负责系统与绘图程序之间的信息交换，处理所有Windows程序的图形输出。
	在Windows操作系统下，绝大多数具备图形界面的应用程序都离不开GDI，我们利用GDI所提供的众多函数就可以方便的在屏幕、打印机及其它输出设备上输出图形，文本等操作。GDI的出现使程序员无需要关心硬件设备及设备驱动，就可以将应用程序的输出转化为硬件设备上的输出，实现了程序开发者与硬件设备的隔离，大大方便了开发工作。
	GDI里面包含大量的绘图函数，例如设备上下文函数(如GetDC、CreateDC、DeleteDC)、 画线函数(如LineTo、Polyline、Arc)、填充画图函数(如Ellipse、FillRect、Pie)、画图属性函数(如SetBkColor、SetBkMode、SetTextColor)、文本、字体函数(如TextOut、GetFontData)、位图函数(如SetPixel、BitBlt、StretchBlt)、坐标函数(如DPtoLP、LPtoDP、ScreenToClient、ClientToScreen)、映射函数(如SetMapMode、SetWindowExtEx、SetViewportExtEx)、元文件函数(如PlayMetaFile、SetWinMetaFileBits)、区域函数(如FillRgn、FrameRgn、InvertRgn)、路径函数(如BeginPath、EndPath、StrokeAndFillPath)、裁剪函数(如SelectClipRgn、SelectClipPath)等，给开发人员画图给予了极大的便捷。本次画板设计，我们便是基于GDI的最基础画点函数去实现上述部分画图功能，以满足绘画板画图最基本的需要。
## 3.2功能设计
	本软件在Windows画板的基础上，不仅实现了基本功能，还扩展了新的功能，具体包括基本操作（文件的新建、保存、打开；正反向撤销；右键菜单的复制、剪切、粘贴）、绘图（基本图形、样式设置、字符选择、画图操作）和状态设置（标尺、导向线）三个部分。

### 3.2.1 基本图形设计

#### 3.2.1.1 直线
	直线通过DDA算法实现。DDA算法是计算机图形学中一种基于直线的微分方程来生成直线的方法，主要是根据直线公式y = kx + b推导出来的，其关键之处在于如何设定单位步进，即一个方向的步进为单位步进，另一个方向的步进必然是小于1的。算法的具体思路如下：
##### （1）获取直线的起点(X0,Y0)和终点(X1,Y1)；
##### （2）分别计算在x、y方向的坐标间距△X和△Y；
##### （3）确定单位步进，取MaxStep = max(△X,△Y)； 若△X >= △Y，则X方向的步进为单位步进，X方向每步进一个单位，Y方向步进△Y / MaxStep个单位；若△Y > △X，则Y方向的步进为单位步进，Y方向每步进一个单位，X方向步进△Y / MaxStep个单位；
##### （4）设置第一个点的像素值；
##### （5）令循环初始值为1，循环次数为MaxStep，x每增加一个步进单位，y增加对应的步进单位。

#### 3.2.1.2 曲线
	曲线采用”基数样条”内插法，通过在给定点之间插入指定数目的内插点，形成光滑曲线。基数样条是一组单个曲线按照一定的顺序连接而成的一条较大曲线。样条由一个点数组和一个张力参数描述。由于基数样条平滑地穿过数组中的每一个点，在曲线的密度上不会出现锐角和突变。
	物理样条是一小片木头或者其他柔性材质做成的。在数学样条诞生之前，设计人员采用物理样条来绘制曲线。它们将样条置于纸上然后定位一系列锚点，然后用铅笔沿着样条绘制曲线。给出的一系列点可能产生不同的曲线，这取决于物理样条的性质。例如，与一个极其易弯曲的样条相比，有较高的抗弯能力的一个样条将生产一条不同的曲线。
	数学样条的公式基于柔性杆的特性， 因此数学样条生产的曲线类似于曾经由物理样条生产的曲线。正如物理样条通过给定的一组点时在不同的张力下的将生成一条不同的曲线一样， 数学样条在张力参数不同的时候也将生成不同的曲线。下图显示了通过相同一组点集的4条基数样条。每条样条都标注了它的张力参数。注意张力系数为0的情况下相当于无限的物理张力，迫使曲线走点之间的最短路径(直线)。张力系数为1表示没有物理张力，此时样条采用最小弯程。如果张力系数大于1，此时的样条看起来就像被压扁的弹簧，被迫经过更长的路径。
	算法的具体思路如下：
##### （1）构建样条曲线类Spline，其中包含一个向量结构体Vec2和三个方法，分别为“贝塞尔”内插InterpolateBezier、内插基数样条InterpolateCardinalSpline和“基数样条”内插法CardinalSpline；
##### （2）接收指定路径点数组；
##### （3）通过方法InterpolateCardinalSpline计算每一小段的张力值；
##### （4）通过方法InterpolateBezier生成每段的内插点；
##### （5）通过方法CardinalSpline将每段的内插点拼接起来，返回最终的曲线路径数组；
##### （6）根据返回的曲线数组，绘制曲线。

#### 3.2.1.3 椭圆
	椭圆通过中点画椭圆算法实现。中点画椭圆算法是一种用于确定绘制一个椭圆所需像素点的算法，该算法的目标是找到一系列通过像素网格且尽可能接近x ^ 2/a^2 + y ^ 2 /b^2= r ^ 2的像素点。
	算法的具体思路如下：
##### （1）获取鼠标拖动的起点(X0,Y0)和终点(X1,Y1)；
##### （2）根据起点和终点，得到椭圆的相关参数：椭圆心o、a和b；
##### （3）把四分之一的椭圆分为上下两个部分，分界点为dy = dx；
##### （4）令F(x,y)=b^2*x^2+a^2*y^2-a^2*b^2，计算F(x,y)的全微分，得到图形在上下两部分的相对增量；
##### （5）根据增量，确定椭圆从点(X0+a,Y0)到点(X1,Y0+b)的四分之一路径；
##### （6）根据椭圆的对称性，画出整个椭圆；
##### （7）若要画圆，按下Ctrl键，默认r = max(a,b)。

#### 3.2.1.4 任意椭圆弧
	任意椭圆弧在椭圆的基础上增加了角度控制，而且逻辑也比椭圆复杂很多，具体实现原理如下：
##### （1）获取起点(b_x,b_y)、椭圆心(o_x,o_y)和终点(e_x,e_y)；
##### （2）根据三点计算出a、b和θ（取 0˚ < θ < 180˚）；
##### （3）计算出上下左右四个方向的边界，用来约束椭圆弧的绘制；
##### （4）根据起点、椭圆心、终点、四个边界画出指定的椭圆弧。

#### 3.2.1.5 任意多边形
	任意多边形在画直线的基础上增加了控制逻辑，以前一条直线的终点，作为下一条直线的起点，最后根据单击鼠标右键结束，自动首尾相连。具体实现过程如下：
##### （1）获取起点(X0,Y0)；
##### （2）通过鼠标Move触发事件实现鼠标移动效果；
##### （3）鼠标左键单击画板，获取中间节点(Xi,Yi)，根据起点(Xi-1,Yi-1)和终点(Xi,Yi)画线，保存已画轨迹；
##### （4）重复过程（2）、（3）；
##### （5）直到单击鼠标右键，将首点(X0,Y0)和尾点(Xn,Yn)相连，画图结束。

#### 3.3.1.2 其他图形
	除了最基本的直线、曲线、和椭圆以外，其他的任何图形均可由这三种最基本图形拼凑得到。例如矩形、圆角矩形、等腰三角形、直角三角形、菱形、五六边形、四五六角星、上下左右四个方向的箭头、圆角文本框、折线、直角线等，以圆角矩形的绘制为例。
	圆角矩形是通过将圆与直线拼接得到的，具体过程如下：
##### （1）获取鼠标拖动的起点(X0,Y0)和终点(X1,Y1)；
##### （2）根据起点和终点，得到圆角矩形的宽w和高h；然后通过指定比例，确定圆的半径r = min(w, h) * 0.3；
##### （3）半径r确定以后，就可以得到圆角矩形周围四条直线的起点和终点以及四个圆心的坐标；
##### （4）设置一个标志flag，用来判断画出圆的哪一部分；
##### （5）全部拼接，得到最终的圆角矩形轨迹。

### 3.2.2 基本字符设计
	字符采用64*64规模的点阵表示，通过保存字符的二维数组点阵，进而通过点阵的信息来确定相应位置像素的信息。在二维数组中，0表示该点像素不填充颜色，相反的，1表示该点的像素应填充对应颜色。再通过相应控件的操作方法将字符呈现在画板上。算法的具体思路如下：

#### （1）制作将要显示的字符点阵，如上图所示；
#### （2）将制作好的点阵信息以二维数组形式保存；
#### （3）编写对应的描点函数，遍历点阵信息，填充相应位置的像素点颜色；
#### （4）调用鼠标点击事件，获取鼠标点击时的位置，通过鼠标位置，设置描点函数的起始位置(x,y)；
#### （5）点击选中字符，可以实现字符的移动。



### 3.2.3 样式设计
	高仿Window自带的画板，结合Visio的特性制作而成
	（1）文件栏
	新建：新建一个画板图形进行操作
	打开：打开一个已存在的画板，在本画板当中是打开一个以.Xml的文件
	保存：对用户界面上的画板进行保存，存储类型为.Xml
	打印：将画板上的内容打印出来
	关于画板：画板的版本等
	（2）主页栏
	排列：
	裁剪按钮：实现图形的裁剪操作
	对称按钮：实现图形的对称操作（点对称）
	对称按钮：实现图形的对称操作（线对称）
	选择按钮：实现图形的旋转操作
	工具：
	画笔：基本的Pen
	填充：种子填充
	擦除：实现图形的删除操作
	颜色取样器：实现颜色的取样工作
	指针工具：实现其余排列栏的各类操作前的选择
	全选：对两个以上的图形进行选择
	对齐方式：实现左对齐、中对齐、右对齐，配合全选操作
	形状：
	直线、椭圆、矩形、多边形、曲线、三角形、直角三角形、五边形、六边形、圆角矩形、左箭头、右箭头、上箭头、下箭头、菱形、四角星、五角星、六角星、文本框、圆弧
	轮廓填充：实现对多边形的轮廓着色
	内部填充：实现对多边形内部的着色
	线型：
	线型：虚线、点划线等
	线宽：线的粗细大小
	颜色：
	画笔颜色：颜色1
	填充颜色：颜色2
	调色板：十种常用颜色、调色板
	文字：
	汉字：周洋、周寅莹、江春鹏、袁晓旭、蒋彬含
	字母：26个字母（大写）
	数字：0-9阿拉伯数字
	符号：+、-、*、/、#
	（3）查看栏
	标尺：实现定位
	网格线：背景的衬托
	状态栏：鼠标的定位
	（4）其他
	保存按钮：图形进行保存
	撤销按钮：对上一次画的图形进行撤销操作
	重做按钮：返回上一次
#### 3.2.3.1 线型
	在绘图应用中常用到的线条有实线、虚线、点划线、双点划线和双划线。其中，点线可以用来表示立体线框中可见的轮廓线；虚线可以用来表示立体线框中不可见的轮廓线；点划线、双点划线可以用来表示中心线；双划线可用来作边框。具体实现思路如下：
	（1）实线：不存在间断，直接实现
	（2）虚线：可通过在实线段之间插入与实线段等长的空白段来显示；
	（3）点划线：点与等长实线段的交错出现；
	（4）双点划线：连续两个点与等长实线段的交错出现；
	（5）双划线：不等长实线段的交错出现。

#### 3.2.3.2 线宽
	线宽是通过线刷子和方刷子来实现的。具体原理如下：
	（1）设直线斜率在[－1，1]之间，此时可把刷子置成垂直方向，刷子的中点对准直线某一端点，然后让刷子中心往直线的另一端移动，即可刷出具有一定宽度的线。
	（2）反之，若直线斜率不在[－1，1]之间，把刷子置成水平方向即可。
	
#### 3.2.3.3 颜色
	颜色分为固定颜色和调色板两种形式。其中，固定颜色是通过设置button背景颜色，响应时自动获取的，而调色板是通过直接调用方法colorDialog1.ShowDialog()得到的。
### 3.2.4 基本操作设计

#### 3.2.4.1 文件操作
	保存要求可以将已经在画板上面的图形的所有保存下来，包括它的边界点、填充色等等信息，以及画板的属性，背景颜色、填充颜色、图形栈等等信息。方便用户再一次进入画板时，可以继续用户之前未完成的工作，因此保存文件要求保存的速度要相对较快，保存的文件恢复速度快，而且保存的信息没有丢失。基于上述的这些需求，本小组将采用序列化与反序列的方法来进行图形对象的保存与恢复。
	文件 
	文件的基本概念 
	  所谓“文件”是指一组相关数据的有序集合。 这个数据集有一个名称，叫做文件名。 实际上在前面的各章中我们已经多次使用了文件，例如源程序文件、目标文件、可执行文件、库文件 (头文件)等。文件通常是驻留在外部介质(如磁盘等)上的， 在使用时才调入内存中来。从不同的角度可对文件作不同的分类。从用户的角度看，文件可分为普通文件和设备文件两种。

	  普通文件是指驻留在磁盘或其它外部介质上的一个有序数据集，可以是源文件、目标文件、可执行程序； 也可以是一组待输入处理的原始数据，或者是一组输出的结果。对于源文件、目标文件、可执行程序可以称作程序文件，对输入输出数据可称作数据文件。

	  设备文件是指与主机相联的各种外部设备，如显示器、打印机、键盘等。在操作系统中，把外部设备也看作是一个文件来进行管理，把它们的输入、输出等同于对磁盘文件的读和写。通常把显示器定义为标准输出文件， 一般情况下在屏幕上显示有关信息就是向标准输出文件输出。如前面经常使用的printf,putchar 函数就是这类输出。键盘通常被指定标准的输入文件， 从键盘上输入就意味着从标准输入文件上输入数据。scanf,getchar函数就属于这类输入。

	  从文件编码的方式来看，文件可分为ASCII码文件和二进制码文件两种。

	  ASCII文件也称为文本文件，这种文件在磁盘中存放时每个字符对应一个字节，用于存放对应的ASCII码。例如，数5678的存储形式为： 
	ASC码： 　00110101 00110110 00110111 00111000 
	     ↓ 　　　　↓　　　　↓ 　　　↓ 
	十进制码： 5　　　　　6　　　　7　　　　8 共占用4个字节。ASCII码文件可在屏幕上按字符显示， 例如源程序文件就是ASCII文件，用DOS命令TYPE可显示文件的内容。 由于是按字符显示，因此能读懂文件内容。

	  二进制文件是按二进制的编码方式来存放文件的。 例如， 数5678的存储形式为： 00010110 00101110只占二个字节。二进制文件虽然也可在屏幕上显示， 但其内容无法读懂。C系统在处理这些文件时，并不区分类型，都看成是字符流，按字节进行处理。 输入输出字符流的开始和结束只由程序控制而不受物理符号(如回车符)的控制。 因此也把这种文件称作“流式文件”。

	本章讨论流式文件的打开、关闭、读、写、 定位等各种操作。文件指针在Ｃ语言中用一个指针变量指向一个文件， 这个指针称为文件指针。通过文件指针就可对它所指的文件进行各种操作。定义说明文件指针的一般形式为： FILE* 指针变量标识符； 其中FILE应为大写，它实际上是由系统定义的一个结构，该结构中含有文件名、文件状态和文件当前位置等信息。 在编写源程序时不必关心FILE结构的细节。例如：FILE *fp； 表示fp是指向FILE结构的指针变量，通过fp 即可找存放某个文件信息的结构变量，然后按结构变量提供的信息找到该文件， 实施对文件的操作。习惯上也笼统地把fp称为指向一个文件的指针。文件的打开与关闭文件在进行读写操作之前要先打开，使用完毕要关闭。 所谓打开文件，实际上是建立文件的各种有关信息，并使文件指针指向该文件，以便进行其它操作。关闭文件则断开指针与文件之间的联系，也就禁止再对该文件进行操作。

	序列化：程序员在编写应用程序的时候往往要将程序的某些数据存储在内存中，然后将其写入某个文件或是将它传输到网络中的另一台计算机上以实现通讯。这个将程序数据转化成能被存储并传输的格式的过程被称为"序列化"（Serialization），而它的逆过程则可被称为"反序列化"（Deserialization）。
	.Net框架对序列化机制具有非常好的支持，它提供了两个名字空间（namespace）：System.Runtime.Serialization和System.Runtime.Serialization.Formatters以完成序列化机制的大部分功能。系列化这项技术可以应用在将程序产生的结果数据存储到文件系统中，但是它更主要的应用是在于.Net Remoting和Web服务的实现上。
	序列化机制的实现是依靠格式器（Formatter）而完成的，它是一个从System.Runtime.Serialization.IFormatter继承下来的类的对象。格式器完成了将程序数据转化到能被存储并传输的格式的工作，同时也完成了将数据转化回来的工作。.Net框架为程序员提供了两种类型的格式器，一种通常是应用于桌面类型的应用程序的，它一个是System.Runtime.Serialization.Formatters.Binary.BinaryFormatter类的对象，而另一种则更主要的应用于.Net Remoting和XML Web服务等领域的，它一个是System.Runtime.Serialization.Formatters.Soap.SoapFormatter类的对象。从它们的名称来看，我们不妨将它们分别称为二进制格式器和XML格式器。

#### 3.2.4.2 右键菜单功能
	复制：在选中图形并进行复制操作时，将选中的图形赋值给剪切板上的shape并改变shape里面的number编号以表示这是两个不同的图形,并将book_copy改为true,表示剪切板不为空。
	剪切：在选中图形并进行复制操作时，将选中的图形赋值给剪切板上的shape并改变shape里面的number编号以表示这是两个不同的图形,并将book_copy改为true,表示剪切板不为空。然后向shape_copy图形栈里面进一个空shape(即shape_show=false，其它属性都为空的shape)，然后将除被选中的图形以外其它所有图形重绘并赋给picture。
	粘贴：判断剪切板是否为空，若不为空则将剪切板的图形进shape_push栈并将其在画板上画出即可。画copy的图形过程如下：
	（1）记录所选中的图形中心点位置；
	（2）记录粘贴时鼠标位置；
	（3）计算平移量(x2-x1,y2-y1),将剪切板上的shape按此平移量平移得到copy后的图形；

#### 3.2.5.1 选中
	遍历存储图形的shape_push栈，判断鼠标点击位置是否在图形四个热点里面，当x1<x0<x2并且y1<y0<y3时，认为鼠标在四个热电里面，图形被选中。
	在图形被选中后显示虚线框和八个热点高亮以表示图形被选中，然后将选中以外其它所有图形在空的Bitmap上重绘并保存，其过程如下：
	（1）建立一个空的HashTable和空的Bitmap。
	（2）遍历shape_push栈，若图形的编号未出现在HashTable里面其不和选中图形编号相同并且此图形不为空,则在Bitmap上绘画此图形。
	（3）将绘画好的Bitmap赋给tempb保存起来。

#### 3.2.5.2 二维几何变换
	图形的几何变换是指对图形的几何信息经过平移、比例、旋转等变换后产生新的图形，是图形在方向、尺寸和形状方面的变换。可将图形顶点的规范化齐次坐标与二维变换矩阵相乘，通过设置对应的参数，即可实现平移、对称、缩放、旋转等操作。
	（一）平移
	e1为拖动前鼠标位置，e2为拖动过程中鼠标实时位置，则Tx=x2-x1,Ty=y2-y1


	根据平移变换矩阵得到平移后图形轨迹并画出即可。平移具体过程如下：
	（1）判断是否有图形被选中；
	（2）若有图形被选中，将保存起来的tempb赋值给bmp，在pictureBox1_MouseMove函数里面使用bmp绘画实时图形并赋给picture,做到平移的实时呈现；
	（3）在鼠标up时认为一次平移完成，将此处的bmp保存到bitmap栈里面以便记录；
	（4）在pictureBox1_MouseUp函数里面将平移后的新shape保存到shape_push里面,保持平移前后shape的编号number相同以表示平移前后是同一个图形，在以后的从上到下遍历shape_push栈的时候只会遍历到平移后的图形。

	（二）缩放
	比例变换是指对p点相对于坐标原点沿x方向放缩Sx倍，沿y方向放缩Sy倍。其中Sx和Sy称为比例系数。
	其中：
	 (1) Sx＝Sy＝1 时，图形不变
	 (2) Sx＝Sy > 1 时，图形沿两轴方向等比例放大
	 (3) Sx＝Sy < 1 时，图形沿两轴方向等比例缩小
	 (4) Sx != Sy时，图形沿两轴方向作非均匀比例变换
	 （三）对称
	对称变换是指对p点坐标进行如下的运算：



	其中：
	(1) b＝d＝0, a＝-1, e＝ 1 时，x*＝ -x, y*＝ y, 	以y 轴对称
	(2) b＝d＝0, a＝1, e＝ -1 时，x*＝ x, y*＝ -y, 	以x 轴对称
	(3) b＝d＝0, a＝ e＝ -1 时，x*＝ -x, y*＝ -y, 以原点对称
	(4) b＝d＝1,  a＝e＝ 0 时，x*＝ y, y*＝ x, 以y = x 直线对称
	(5) b＝d＝-1, a＝ e＝ 0 时，x*＝ -y, y*＝ -x, 以y = -x 直线对称
	由上可知，我们可以通过设置对应的a、b、d和e来实现图形关于给定直线的对称变换。

	（四）旋转
	旋转变换是指对p点坐标进行如下的运算：
#### 3.2.5.3 填充
	图形填充采用种子填充算法，填充效果比较好。种子填充算法的思路如下：
	（1）初始化：种子像素入栈，当栈非空时，重复2～4的步骤；
	（2）栈顶像素出栈；
	（3）将出栈像素置为多边形颜色；
	（4）按右、上、左、下顺序依次检查与出栈像素相邻的四个像素，若其中某个像素不在边界上且未置成多边形色，则该像素入栈；
	（5）当堆栈为空时，算法终止。
#### 3.2.5.4 对齐
	对齐分为两个部分：组合图形的选中和组合图形的对齐。其中对齐有三种形式，分别为左对齐、右对齐和居中对齐，原理一样，这里只介绍左对齐，具体实现过程如下：
	（1）在选中图形的基础上，按下Ctrl键，添加其他的图形，被选中的图形用一个大的红色虚线矩形框包围；
	（2）其中虚线矩形框的大小取决于被选中图形集里面所有图形轨迹中最大、最小的横纵坐标；
	（3）根据虚线矩形框，我们可以很容易地得到左边界，对图形集里面的所有图形进行平移操作，就可以实现最终的对齐；
	（4）关键在于根据组合图形选中时求出的x最小和最大值，确定图形移动的距离，计算对齐后的轨迹点，然后重绘所有图形，即可实现对齐操作。

#### 3.2.5.5 裁剪
	裁剪采用的是Sutherland-Hodgeman多边形裁剪算法，为窗口各边界裁剪的多边形存储输入与输出顶点表。在窗口的一条裁剪边界处理完所有顶点后，其输出顶点表将用窗口的下一条边界继续裁剪。基本思想如下图所示：
	算法实施策略：
	（1）为窗口各边界裁剪的多边形存储输入与输出顶点表。在窗口的一条裁剪边界处理完所有顶点后，其输出顶点表将用窗口的下一条边界继续裁剪；
	（2）窗口的一条边以及延长线构成的裁剪线把平面分为两个区域，包含有窗口区域的一个域称为可见侧；不包含窗口区域的域为不可见侧。
# 参考文献
	[1]孙家广. 计算机图形学(第三版)[M]. 清华大学出版社, 1998.
	[2]基数样条https://blog.csdn.net/htt9931/article/details/9304835?locationNum=6&fps=1
	[3]由孙家广、胡事民编著的《计算机图形学基础教程》是普通高等教育"十一五"国家级规划教材。本书是在年出版的第一版的基础上修订而成的,基本涵盖了本科生和硕士研. 《计算机图形学基础教程》(第2版)[J]. 计算机教育, 2009(23).
	[4]佚名. 精通C#程序设计[M]. 2004.
	[5]陈锋. C#程序设计中自定义控件的创建与应用[J]. 软件导刊, 2013, 12(6):20-23.
	[6]佚名. C#程序设计实用教程[M]// C++程序设计实用教程. 2011.
	[7]佚名. C#程序设计及应用教程.第3版[M]// C#程序设计及应用教程-第2版. 2014.
	[8]佚名. Visual C# 2008控件使用范例详解[M]. 2009.
	[9]Stephens R. C# Graphics Programming[J]. Cengage Learning, 2010, 51(6):776-778.
	[10]Foley J, Dam A V, Feiner S, et al. Computer Graphics in C#: Principles and Practices[J]. J R Soc Med, 1996, 74(9):708-709.
