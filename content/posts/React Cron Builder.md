+++
title = "React Cron Builder"
date = 2019-03-15T15:32:36+08:00
tags = ["React Cron Builder"]
categories = ["React"]
draft = false
+++

##React Cron Builder 使用小结

React Cron Builder 是基于react 组件来构建的cron
官方网址 https://www.npmjs.com/package/react-cron-builder
安装方法 npm install --save react-cron-builder
**********************************************************

引入的时候务必要把样式也一同引入

这个插件的样式比较丑，可以自己进行修改操作。
但踩坑的是，没有具体的dom操作，不太方便更改插件的英文。
###此插件有三个模式：
####第一个是定时在一个时间点
####第二个是定时在一个时间段
####第三个是定时在一个时间段循环执行

在Linux中时常用到cron来执行特定的文件。
cron的表达式是一个字符串 通常是 *5个或者6个or7个* 以空格隔开
["* * * * *"]
*"*"* 表示匹配该区域的任意值
第一个*代表的是秒(0-59)
第二个*代表的是分钟(0-59)
第三个*代表的是小时(0-23)
第四个*代表的是天(0-31，具体参考当月天数)
第五个*代表的是月(0-11)
第六个*代表的是一周(1-7)
第七个*代表的是年份(1970-2099)

“-”(5-20) 表示5到20分钟 每分钟触发一次
“/”(5/20) 表示从5分钟开始，之后每过20分钟触发一次，即25,45触发一次
“,”(5,20) 表示枚举，每5和20分钟触发一次

**************************************************************

cron只有两个值
一个是cronExpression 等于value 是字符串类型
一个是showResult 布尔类型，用于是否显示表达式结果，true和false
onChange 方法可以得到表达式结果。