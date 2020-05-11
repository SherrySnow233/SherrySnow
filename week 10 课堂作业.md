#### week 10 课堂作业

1、试描述PHP程序的运行流程。

如果没有使用PHP、JavaScript等，HTTP协议传输只能是静态的HTML文件。也就是，HTML文件不会受到用户行为的影响，内容一直保持不变。

如果要实现动态网页，就需要使用PHP或JavaScript。PHP是用于服务器端的编程语言，JavaScript是多用于客户端的编程语言。

PHP代码是在服务器端被执行的。用户访问一个包含PHP代码的网页时，发送Request到服务器，其中包含网页的文件名。服务器收到Request后，找到文件名指向的文件，发现其中嵌有PHP代码，会调用PHP解释器处理该文件，然后将处理后的结果整理到Response，发送到客户端。PHP代码可以与服务器端的数据库或其他资源进行交互，或者根据用户的操作产生不同的页面。

因此，PHP脚本的触发是在服务器收到客户端的Request。收到一个Request后，服务器触发一个PHP脚本；处理完脚本后，返回结果到客户端，等待下一个Request。当收到下一个Request后，服务器触发另一个（或同一个）PHP脚本。两次PHP脚本的运行是相互独立的，第二次脚本的运行几乎不受前一次脚本运行的影响。

2、目前常用的服务器软件有哪些？

①Apache

Apache是世界使用排名的Web服务器软件。它几乎可以运行在所有的计算机平台上。由于Apache是开源免费的，因此有很多人参与到新功能的开发设计，不断对其进行完善。 Apache的特点是简单、速度快、性能稳定，并可做代理服务器来使用。

②IIS

IIS(Internet信息服务)英文Internet Information Server的缩写。它是微软公司主推的服务器。IIS的特点具有：安全性，强大，灵活。

③Nginx

Nginx不仅是一个小巧且高效的HTTP服务器，也可以做一个高效的负载均衡反向代理，通过它接受用户的请求并分发到多个Mongrel进程可以极大提高Rails应用的并发能力。

④Tomcat

Tomcat是Apache 软件基金会(Apache Software Foundation)的Jakarta 项目中的一个核心项目，由Apache、Sun 和其他一些公司及个人共同开发而成。Tomcat 技术先进、性能稳定，而且免费，因而深受Java 爱好者的喜爱并得到了部分软件开发商的认可，成为目前比较流行的Web 应用服务器。

⑤Lighttpd

Lighttpd是由德国人 Jan Kneschke 领导开发的，基于BSD许可的开源WEB服务器软件，其根本的目的是提供一个专门针对高性能网站，安全、快速、兼容性好并且灵活的web server环境。具有非常低的内存开销，CPU占用率低，效能好，以及丰富的模块等特点。支持FastCGI, CGI, Auth, 输出压缩(output compress), URL重写, Alias等重要功能。

⑥Zeus

Zeus是一个运行于Unix下的非常的Web 服务器，据说性能超过Apache，是效率的Web 服务器之一。

3、如何将PHP与Apache建立关联。

第一步，找到我们的apache当中conf文件夹下的httpd.conf文件，在文件当中加入如下的内容


将我们的php安装目录下的php.ini.development文件改成php.ini

在php.ini当中指定扩展模块路径extension_dir="php安装路径"/ext

进行测试,apace下建立一个Php文件

<?php

  phpinfo();

?>

4、主目录下面的子目录和虚拟目录有何不同？

虚拟目录包含存放网页内容的实际目录和用于访问网页的别名。该别名的输入方式是web客户端觉得所访问的目录是在原来网站的主目录下，而实际上该别名所对应的实际目录可以是在网络中的任何位置，甚至在另外一台计算机上。

