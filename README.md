# HttpMethords
这个项目把我知道的网络请求总结起来了，并做简单的封装。    
注解框架使用了butterknife。  
在开发的时候，butterknife搭配ButterKnife Zelenzny插件来使用，能加快开发的速度和缩减代码量。 
##总结了哪些网络请求?  
HttpUrlConnection,HttpClient,android-async-http,Volley,OKHttp
####HttpUrlConnection
Android2.3以前有Bug，Android2.3以后推荐使用。API简单，体积小。有缓存机制，节省流量，提升速度，省电。
####HttpClient
Android2.3以前Bug相对较少，所以2.3前推荐使用。
####Volley
它是谷歌团队研发的。2013I/O大会退出。它在Android2.3底层使用HttpClient,Android2.3以后使用HttpUrlConnection。所以它灵活地避免了两个框架的缺点。而且它集成了ImageLoader的优点。    
总的来说，优点:对于多次，数据量较少的网络请求适用。且能较好压缩处理图片。缺点:对于大文件下载和数据量大的网络请求支持不好。
PS:Volley还可以设置为使用OKHttp为网络请求层。
####android-async-http   
是对HttpClient的封装，底层为HttpClient(已经不推荐适用)。网络请求和回调都是在子线程执行。
####OKHttp  
需要在Android2.3以后使用。从Android4.4开始HttpURLConnection的底层实现采用的是okHttp。


