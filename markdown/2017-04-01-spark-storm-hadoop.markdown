---
layout:     post
title:      "Spark Storm Hadoop"
subtitle:   "大数据相关"
date:       2017-04-01
author:     "ZhangZhe"
tags:
    - 大数据
---

# Hadoop vs Storm

以下内容[`摘录自`](http://www.oschina.net/news/73939/hadoop-spark-%20difference)：

Hadoop实质上更多是一个分布式数据基础设施: 它将巨大的数据集分派到一个由普通计算机组成的集群中的多个节点进行存储。Hadoop还会索引和跟踪这些数据，让大数据处理和分析效率达到前所未有的高度。
Spark，则是那么一个专门用来对那些分布式存储的大数据进行处理的工具，它并不会进行分布式数据的存储。

相反，Spark也不是非要依附在Hadoop身上才能生存，但它没有提供文件管理系统。所以，它必须和其他的分布式文件系统进行集成才能运作。这里我们可以选择Hadoop的HDFS,也可以选择其他的基于云的数据系统平台。但Spark默认来说还是被用在Hadoop上面的，毕竟，大家都认为它们的结合是最好的。

MapReduce是分步对数据进行处理的: ”从集群中读取数据，进行一次处理，将结果写到集群，从集群中读取更新后的数据，进行下一次的处理，将结果写到集群，等等…“ Booz Allen Hamilton的数据科学家Kirk Borne如此解析。

反观Spark，它会在内存中以接近“实时”的时间完成所有的数据分析：“从集群中读取数据，完成所有必须的分析处理，将结果写回集群，完成，” Born说道。Spark的批处理速度比MapReduce快近10倍，内存中的数据分析速度则快近100倍。

如果需要处理的数据和结果需求大部分情况下是静态的，且你也有耐心等待批处理的完成的话，MapReduce的处理方式也是完全可以接受的。
但如果你需要对流数据进行分析，比如那些来自于工厂的传感器收集回来的数据，又或者说你的应用是需要多重数据处理的，那么你也许更应该使用Spark进行处理。
大部分机器学习算法都是需要多重数据处理的。此外，通常会用到Spark的应用场景有以下方面：实时的市场活动，在线产品推荐，网络安全分析，机器日记监控等。

# Spark
有待补充