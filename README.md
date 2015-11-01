# glideDemo

Glide是一个高效、开源、 Android设备上的媒体管理框架，它遵循BSD、MIT以及Apache 2.0协议发布。Glide具有获取、解码和展示视频剧照、图片、动画等功能，它还有灵活的API，这些API使开发者能够将Glide应用在几乎任何网络协议栈里。创建Glide的主要目的有两个，一个是实现平滑的图片列表滚动效果，另一个是支持远程图片的获取、大小调整和展示。近日，Glide 3.0发布，现已提供jar包下载，同时还支持使用Gradle以及Maven进行构建。该版本包括很多值得关注的新功能，如支持Gif 动画和视频剧照解码、智能的暂停和重新开始请求、支持缩略图等，具体新增功能如下如下：

GIF动画的解码：通过调用Glide.with(context).load(“图片路径“)方法，GIF动画图片可以自动显示为动画效果。如果想有更多的控制，还可以使用Glide.with(context).load(“图片路径“).asBitmap()方法加载静态图片，使用Glide.with(context).load(“图片路径“).asGif()方法加载动画图片
本地视频剧照的解码：通过调用Glide.with(context).load(“图片路径“)方法，Glide能够支持Android设备中的所有视频剧照的加载和展示
缩略图的支持：为了减少在同一个view组件里同时加载多张图片的时间，可以调用Glide.with(context).load(“图片路径“).thumbnail(“缩略比例“).into(“view组件“)方法加载一个缩略图，还可以控制thumbnail()中的参数的大小，以控制显示不同比例大小的缩略图
Activity生命周期的集成：当Activity暂停和重启时，Glide能够做到智能的暂停和重新开始请求，并且当Android设备的连接状态变化时，所有失败的请求能够自动重新请求
转码的支持：Glide的toBytes() 和transcode() 两个方法可以用来获取、解码和变换背景图片，并且transcode() 方法还能够改变图片的样式
动画的支持：新增支持图片的淡入淡出动画效果（调用crossFade()方法）和查看动画的属性的功能
OkHttp和Volley的支持：默认选择HttpUrlConnection作为网络协议栈，还可以选择OkHttp和Volley作为网络协议栈
其他功能：如在图片加载过程中，使用Drawables对象作为占位符、图片请求的优化、图片的宽度和高度可重新设定、缩略图和原图的缓存等功能
另外，请大家注意，除了以上新引入的功能外，还具有Glide 2.x系列版本的所有功能，如背景图片的加载、内存和磁盘间的高效缓存、使用位图和资源池提高加载性能， 更多Glide3.0相关信息请登陆GitHub上的Wiki页面查看。
