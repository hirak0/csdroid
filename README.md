# csdroid_by:LinshaoSec
# cobaltstrike手机客户端
`最新编辑时间：2022年10月10日`


# 设计图

![image](https://user-images.githubusercontent.com/96420060/190606092-c3241505-e2de-4752-8260-38ec344ea4e7.png)

# 实物图
![image](https://user-images.githubusercontent.com/96420060/190607040-65c8a637-4035-4f85-88ac-defd390acab9.png)

# ------------------------------------------------------------------------------

# 使用

## 登录
登录默认版本：  
无需设置
   
 
登录魔改版本：   
点击登录设置,修改写入int值为，commom/SecureSocket.class文件拖入idea，authenticate()函数内第69行writeInt的数字(如48879):var3.writeInt(48879);   
修改写出int值为：commom/SecureSocket.class文件拖入idea，authenticate()函数内第83行的数字(如51966)：if (var4 != 51966) 

## 版本适配   
点击登录会提示再次点击登录按钮即可成功


# 简介   
c2d:方便在外时候参与多人运动

下步计划：   
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        已发布1.0版本,`2022年10月13日`  
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        之后看需求情况更新，需求不大的话就这样简简单单就差不多了，肝快没了
        
已实现功能：  
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        会话相关：  `实时上线下线`，`休眠时间设置`  
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        命令相关：  `命令执行shell`，`sleep`，`命令小偷`
        
待写功能：移除shell会话,创建删除监听器、生成shellcode、截屏、文件管理、进程查看、  



# 演示视频
等待上传


# Star
[![Stargazers over time](https://starchart.cc/linshaoSec/WaterExp.svg)](https://starchart.cc/linshaoSec/WaterExp)
***

  
开发进度：

2022年9月15日：已完成登录服务端，可获取到beacon信息

2022年9月17日：完成session上线布局，收到的session与界面activity绑定，实现实时刷新数据(出现bug，无法获取到新加入的会话)

2022年9月18日：通过调试研究处较好方案如下：

2022年9月20日：已经完成实时上线绑定，即时同步删除会话，(修复bug)切换界面保存当前会话状态  
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
               ` 已经实现根据服务端实时同步上线，更新心跳，会话移除`

2022年10月6日：
        1.实现`命令执行`的回显，（未区分beacon任务）  
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        2.（发现bug）：列表会话超过10个心跳停止更新

2022年10月7日：1.完美解决命令执行回显，（下步准备此页面添加休眠时间）    
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        （获取元数据的时候把历史命令执行结果存放到BeaconTasksLog里面    
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        ShellFragment里面通过pid去获取之前的命令执行结果，  
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        设置到页面，并开始监听以后的命令执行，结果写到BeaconTasksLog）  
        
2022年10月8日：1.添加`更改休眠`时间功能  
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        2.（bug）排查AndroidManifest中service的name属性少输入.导致无报错无反应  
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        3.通宵重构,把主要与服务器交互的组件由分散改为service集中处理  
        
2022年10月9日：1.通宵重构任务的上线，使代码清晰，管理会话更加清晰便捷  
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        2.导出命令完成界面的设计和实现  
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;

2022年10月10日： 1.`命令导出`已经实现功能，细节仍需处理  

2022年10月13日： 1.自动适配服务器cs版本进行登录，暂时4.3,4.5，4.4修改版测试成功



