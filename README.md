# DotNetClub
A Tiny Club Written in Asp.Net Core

How to Build and Run:

*   Clone the repository
*   Restore the dependencies

    ```
    dotnet restore
    ```
*   Go to DotNetClub.Web directory

    ```
    cd src\DotNetClub.Web
    ```
*   Edit database connection string by SecretManagerTools

    ```
    dotnet user-secrets set ConnectionString YourConnectionString
    ```
*   Install Database

    ```
    dotnet ef database update
    ```
*   Install client libraries

    ```
    bower install
    ```
*   Run the project

    ```
    dotnet run
    ```

前言

盼星星盼月亮，Asp.Net Core终于发布啦！！

Asp.Net发布时我还在上初中，没有赶上。但是Asp.Net Core我从beta版本便一直关注。最初项目名叫Asp.Net VNext，然后改名叫Asp.Net 5。最煎熬的是RC1发布后，官方继续发布了改名和RC2延期的通告。这期间我已经做了一些demo项目，但是由于beta到RC2之间涉及到大量API的改动，包括dnx->dotnet cli，包括各种命名空间和工具名称的改动等等，因此这部分demo都已删掉。5月份，Github Asp.Net Core更新路线图，确定RC2于5月中旬发布，同时确定RC2会作为最终发布的版本基础。那段时间我疯狂的关注着Github，即使在国外度蜜月，也会在晚上蹭Wifi关注着动态（这里提一下，有空看一下各个项目的issue，可以积累很多知识。同时很多小道消息都可以在members的回复中看出来）。好在接下来没有再次跳票，开源、跨平台、高性能的Asp.Net Core终于来啦！

小型社区系统

首先看下项目截图：



项目布局参考了CNodeJS 前端采用了Bootstrap，数据库访问用了EntityFramework Core，同时自己用Middleware实现了一个简单的身份认证功能

目前完成的功能：注册，登录，发帖，回帖，收藏，置顶，精华等功能。

项目地址：GitHub

如何运行：

1. 首先安装基础环境

2. clone或者下载项目，先设置连接字符串，然后还原数据库，最后运行即可

详细流程请点击上方连接查看项目主页

开发感受

1. 对于初学者，Asp.Net Core的入门门槛还是挺高的。

没有了WebForm，无法再拖拖控件就完成一个Hello World Page。

MVC和WebApi合二为一，那么至少对这2种技术应该有些基础了解。

处理HTTP请求从传统的Handler、Page变成了Middleware，如果不熟悉nodejs(express)的话又是个新鲜事物。

搭建一个web项目，首先就用到依赖注入容器，又有多少初学者接触过依赖注入呢？

2. 对于.Net开发者，还有很多东西要学。

新的TagHelper和ViewComponent，看来是要培养起面向组建编程的习惯了。

前端可以方便的集成bower, gulp等，那么NodeJS, npm, bower, gulp等等都是需要学的。

project.json里面的东西涉及到编译、发布、部署等等一系列配置，再结合dotnet命令，可以很简单的实现自动化，想起来是不是很激动？

新的EntityFramework Core Migration，直接基于命令生成和更新数据库，看起来是不是很酷？

整个AspNet Core Framework都开源了，基础源码难道不想去看看？

最最最重要的是跨平台！现在我们再也没法逃避Linux啦，大家赶紧装虚拟机，从最基本的ls开始linux之旅吧！

3. 对于Asp.Net Core，还有很长的路要走

性能：从官方的性能测试看出，目前Asp.Net Core可以超过NodeJS，但是比JAVA的Netty还是差了太多（这个测试看起来还是RC1的版本）。首先我觉得大家应该培养起异步编程的好习惯，这篇文章讲述了异步编程是如何提升并发效率的；其次只能寄希望于微软继续提升性能，或者有第三方高性能web框架出现。

框架：Asp.Net Core从出生起就声明了只是.Net Framework的子集，但是部分基础框架的缺失还是带来了很大的不便。最最不方便的就是System.Drawing。

第三方库：作为一个婴儿，Asp.Net Core才刚出生，又经历跳票，因此这方面资源少得可怜。几大热门项目：Dapper，AutoMapper，Nlog等倒是很早就开始支持了。

开发人员流失：谁敢说身边没有从.Net转Java，转Android，转IOS的？？

后记

昨天加班到3点，今天早上继续上班，头都是晕的。个人技术不好，见解不够，以上都是自己的想法，希望大家多多交流，一起为.Net社区出力！！


