---
comments: false
date: 2017-07-27 09:44:41
permalink: resume
---
# 联系方式
* 手机：18601224166
* Email：shenyangkai1994@gmail.com
* QQ：237497819

# 个人信息
* 沈扬凯 / 男 / 1994
* 湖北文理学院 / 物联网工程专业 / 学士
* 技术博客：http://xkcoding.com

# 工作经历
## 图迹信息科技（2016年8月 ~ 至今）
### 风电场功率预测管理平台（v2.0）
根据国网电力系统二次安防的要求，加入正向隔离，对原有v1.0平台进行重构。服务端程序改用oracle做数据库，并搭建了 Rac 实现高可用。前端引入了 echarts 组件，用于展示全国发电散点图，以及全国风场各省份发电信息的对比。现场端传输逻辑重构，由原有的 UDP 协议同步内外网数据，设计成保存为 json 数据文件，使用隔离传输 json 文件至内网服务器，内网程序解析 json 文件，来做到内外网的数据同步，反之，内网同步数据也通过隔离传输 json 数据文件至外网服务器来实现。现场端程序的在线升级也采用文本的方式进行，将 zip 压缩文件，通过BASE64 encode 成 byte[] 写入文本文件，通过隔离传输至内网后，decode 回 zip 文件，然后进行程序包的升级。

主要负责服务端的整体重构，现场端的数据同步逻辑，以及在线升级程序的实现。
### 风功率预测管理平台（v1.0）
风功率预测管理平台分为现场端和服务端程序，服务端程序主要用于数据的展示，以及风电场短期预测文件的获取，现场端程序分为内网程序和外网程序，外网程序主要是与服务端进行数据的同步，以及采集各个测风塔与风机的实时数据，并按照调度要求定时生成调度 E 文件，传输给内网程序，内网程序收到调度文件，通过102协议或者 FTP 将文件传输至调度，并将传输结果返回给外网程序。

主要负责服务端获取短期预测文件的设计，使用 Spring Quartz 定时从 FTP 获取文件并解析入库；以及实时数据的获取和使用模板技术定时生成调度文件。

设计技术：服务端使用 restlet 做 MVC 层；现场端使用 Swing 做界面；百度echarts展示各个风场发电趋势；Spring Quartz 和 Freemarker 定时生成统一调度文件；使用 modbus4j 读取并解析设备实时数据。
### 图迹售电资料检索平台、晶见资讯
独自完成基于 ElasticSearch 搭建售电资料检索平台，售电资料通过 Python 抓取网上售电信息资料，每天保存在服务器指定文件夹，然后用 Java 定时监听文件夹内容，将新文件解析并存入 ES ，支持的文件格式包括 txt、word 2003、word 2007、pdf，方便公司售电人员在内网在线查找售电资料。同时搭建了`晶见资讯`小程序，方便手机端下载售电相关资料。

设计技术：JFinal；ElasticSearch；IK中文分词；PDF和word文件处理；微信小程序
最自豪的事：开始了解前端 ES6 语法
## 武汉金智维科技有限公司（2015年6月——2016年7月）
### 襄阳变电站设备检测管理系统
主要对襄阳市各个变电站站点的运行监控，以及设备资源数据管理，对站点的运行提供故障分析和解决方案，对设备的运行提供实时校准、检修、验收的管理体制，保证了所有站点和运行设备正常运行，和对数据的分析、统计；设备的购置和费用报销由公司财务人员及有关部门领导共同介入审核，保证录入数据的准确性，合理性；并实现公司每个站点资料图书管理，方便的为公司技术人员提供最新的设备图书资料，给公司技术人员提供强大的技术支持；使用开源的echarts图表组件，生成设备运行情况，有利于技术人员做故障分析。

负责开发模块包括技术设施维护管理、站点管理、图书资料信息管理、系统管理4个功能模块，实现系统的功能设计与开发、页面设计与开发、数据库设计。除实现功能代码外，并编写系统的概要设计、详细设计文档及用户使用手册。

涉及技术：POI 导入和导出；富文本编辑器 Ueditor 处理多格式文本内容；quartz定时备份数据库；echarts 来展示设备年月周的运行情况。
### 华中科技大学教室管理系统
为了简化华中科技大学每年繁重的教室分配和分发权力，让各院老师或者学生自己去借用教室，而学校只需要从中调节一下不合理的教室申请就可以了，免去了以前查教室，然后考虑该教室是否可用等一系列繁复的操作，只保留现在的审核就可以了。也符合了现在信息化管理的条件，与时俱进，迎合了现代人的想法化繁为简，也简化了老师们的工作量。

主要负责教室申请整个流程的设计，流程分为老师（学生）申请、院系审核、教务处审核等一些功能的实现，并且设计相应的表结构和以及后台逻辑的开发。主要使用了jquery与ajax实现前端效果展示与前后台的数据交换工作，以及struts2自带的上传文件功能。

### 谷城县再生资源回收利用平台
主要是提供一个在线的可再生资源信息发布平台，包括的内容有信息的发布和求购，网点的分布和资源你的推送。实现再生资源线上预约线下回收、分拣、交易、拍卖一体化的再生资源回收交易服务平台。 利用基于LBS的全方位O2O模式为产废、收废、利废环节搭建成一个最权威、最安全、最快捷、最方便的再生资源回收交易服务平台。该系统在功能上包括用户管理、公告管理、信息发布、审批管理、评论、位置服务、线上支付、首页管理。

主要负责信息发布、用户管理模块的开发，并且配合参与审批管理以及框架的搭建和数据库的设计。我的任务重心在信息发布上、主要使用JQuery与Ajax完成异步交互，后台使用内部MVC框架实现数据的交互。
# 技能清单
**以下均为我熟练使用的技能**
语言：Java
框架：Spring Boot / Spring Mvc / JFinal / Mybatis / Hibernate / Struts2
模板：JSP / Velocity / FreeMarker / Beetl / Thymeleaf
前端：Twitter Bootstrap / Semantic UI / jQuery / JavaScript / Require JS / CSS / jQuery Template / 百度 Echarts 图表 / Vue.js
定时任务：Cron4j / Spring Quartz
测试：Junit
数据库：MySQL / SQL Server / Oracle
版本管理：Git / Svn
缓存：Redis / Memcached
搜索：Lucene / ElasticSearch
脚本：Shell
系统：Linux / Windows

**以下为我了解的技能**
语言：Python
消息队列：ActiveMQ / RabbitMQ
前端框架：React / AngularJS

# 致谢
感谢您花时间阅读我的简历，期待能有机会和您共事。