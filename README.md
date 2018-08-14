· 大型网站架构模式

    · 综述

    · 分层
         将系统在横向维度上切分成几个部分，每个部分负责一部分相对比较单一的职责，然后通过上层对下层的依赖和调用组成一个完整的系统
   
    · 分割
        从纵向方面对软件进行切分，将不同功能和服务分割开来，包装成高内聚低耦合的模块单元
    
    · 分布式
        分层和分割的一个主要目的是为了切分后的模块便于分布式部署，即不同模块部署在不同服务器上，通过远程调用协同工作。
    
    · 集群
        通过负载均衡技术为一个应用构建一个多台服务器组成的集群，共同对外提供服务
    
    · 缓存
        将数据存放在距离计算最近的位置。
    
    · 异步
        单一服务器内部可通过多线程共享内部队列方式实现异步，业务操作前面的线程将输出写入队列，后面的线程从队列读取数据处理
    
    · 冗余
        任何服务都必须部署至少两台服务器构成的一个集群
    
    · 自动化
        减少人为干预，减少故障
    
    · 安全
        

· 网站前端性能优化
    
    · DOM 树
    
    · CSS 优化

    · JavaScript 优化

    · 图片

https://wy-ei.github.io/2016/09/fe-performance-optimization.html


https://github.com/wy-ei/notebook/issues/15

http://stevesouders.com/hpws/js-middle.php

https://csstriggers.com/

https://github.com/wy-ei/notebook/issues/34

https://www.cnblogs.com/netoxi/p/7258895.html#%E7%BB%BC%E8%BF%B0

https://www.cnblogs.com/lei2007/archive/2013/08/16/3262897.html

https://blog.csdn.net/smiple9102/article/details/78890600

