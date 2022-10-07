# csdroid_by:LinshaoSec
# cobaltstrike手机客户端


  
# 如果您有期待，请点个star给与我开发的动力，Thanks
And post issues


# 设计图

![image](https://user-images.githubusercontent.com/96420060/190606092-c3241505-e2de-4752-8260-38ec344ea4e7.png)

# 实物图
![image](https://user-images.githubusercontent.com/96420060/190607040-65c8a637-4035-4f85-88ac-defd390acab9.png)

# ------------------------------------------------------------------------------

开发进度：

2022年9月15日：已完成登录服务端，可获取到beacon信息

2022年9月17日：完成session上线布局，收到的session与界面activity绑定，实现实时刷新数据(出现bug，无法获取到新加入的会话)

2022年9月18日：通过调试研究处较好方案如下：

2022年9月20日：已经完成实时上线绑定，即时同步删除会话，(修复bug)切换界面保存当前会话状态
               ` 已经实现根据服务端实时同步上线，更新心跳，会话移除`

2022年10月6日：
        1.实现命令执行的回显，（未区分beacon任务）
        2.（发现bug）：列表会话超过10个心跳停止更新
2022年10月7日
        1.完美解决命令执行回显，（下步准备此页面添加休眠时间）

下步实现：休眠更改

待写功能：创建删除监听器、生成shellcode、截屏、文件管理、进程查看、
  

![image](https://user-images.githubusercontent.com/96420060/190707124-e93e91ab-ac0d-422c-969b-f440e0cd5290.png)
![image](https://user-images.githubusercontent.com/96420060/194535361-ff974990-fb78-4280-ab64-ac980274dff1.png)



https://user-images.githubusercontent.com/96420060/191273173-c0037864-1d04-40af-8ea3-d0c9952935b9.mp4


