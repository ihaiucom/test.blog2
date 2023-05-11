---
layout: post
categories: [scala]
title: spark System memory must be at least
date: 2017-12-26
author: TTyb
desc: "System memory * must be at least *.Please increase heap size using the --driver--memory option or spark.driver.memory"
---

运行 `ScalaSpark` 程序的时候出现错误：

~~~ruby
System memory * must be at least *.Please increase heap size using the --driver--memory option or spark.driver.memory
~~~

<p style="text-align:center"><img src="/static/postimage/scala/systemmemory/20171226094546.png" class="img-responsive" style="display: block; margin-right: auto; margin-left: auto;"></p>

在 `Intellij IDEA` 里面找到：

~~~ruby
Run -> Edit Configurations -> Application -> Configurations 
~~~

<p style="text-align:center"><img src="/static/postimage/scala/systemmemory/20171226095003.png" class="img-responsive" style="display: block; margin-right: auto; margin-left: auto;"></p>

设置大小：

~~~ruby
-Xms256m -Xmx1024m
~~~

<p style="text-align:center"><img src="/static/postimage/scala/systemmemory/20171226095209.jpg" class="img-responsive" style="display: block; margin-right: auto; margin-left: auto;"></p>