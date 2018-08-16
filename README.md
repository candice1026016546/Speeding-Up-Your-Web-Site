· 高性能网站架构模式



![image](https://github.com/candice1026016546/Speeding-Up-Your-Web-Site/blob/master/structure.png)



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
       XSS攻击
        A.反射型
        正常发送消息：
        http://www.test.com/message.php?send=Hello,World！
        接收者将会接收信息并显示Hello,Word
        非正常发送消息：
        http://www.test.com/message.php?send=<script>alert(‘foolish!’)</script>！
        接收者接收消息显示的时候将会弹出警告窗口
        
        B.持久型
        正常操作：
        留言板表单中的表单域：<input type=“text” name=“content” value=“这里是用户填写的数据”>
        用户是提交相应留言信息；将数据存储到数据库；其他用户访问留言板，应用去数据并显示。
        非正常操作：
        攻击者在value填写<script>alert(‘foolish!’)</script>【或者html其他标签（破坏样式。。。）、一段攻击型代码】；
        将数据存储到数据库中；
        其他用户取出数据显示的时候，将会执行这些攻击性代码
        
       注入攻击
         http://www.test.com/message.php?username='A';drop table users;--
        
       CSRF攻击
        攻击者盗用了你的身份，以你的名义发送恶意请求

· 网站前端性能优化
    
    · 页面呈现过程
     ·DOM 树
     ·CSSOM 树
     ·Render 树

![image](https://github.com/candice1026016546/Speeding-Up-Your-Web-Site/blob/master/DOM.jpg)    

    · 优化渲染性能
         ·JavaScript：改变元素样式，添加元素到 DOM 中等等
         ·Style：元素的类或者style改变了，这个时候需要重新计算元素的样式
         ·Layout：需要重新计算元素的具体尺寸 
         ·Paint：将元素的绘制的图层上
         ·Composite：合并多个图层
    
    
    · CSS 优化
        ·将样式表置顶
        ·避免使用CSS表达式
        .用<link>代替@import
        
    · JavaScript 优化
        ·将脚本置底
        ·使用外部Javascirpt和CSS文件
        ·精简Javascript和CSS
        
    · 图片
        ·CSS Sprite
        
        



