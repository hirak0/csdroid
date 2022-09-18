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

    上线监听
	综下所述，最佳实现方式：
		1.获取sessions
			如果是map子类：(表示历史的session信息)以bid对key存放hashmap为all_object_sessions_obj
			如果是ChangeLog子类：(表示新上线的session)解析其key对象
				a)添加到all_object_sessions_obj,
				b)添加到curr_object_sessions_obj
				更新整个显示列表
		2.获取beacons的心跳
			没有结果：（表示session列表为空）则在curr_object_sessions_obj查询是否bid为空，
				不为空：则置空curr_object_sessions_obj列表来清空客户端，更新整个显示列表
				空：不进行操作
			有结果：（表示收到session心跳）则在curr_object_sessions_obj根据bid里查找对应的实体，
				有结果：（表示已经添加到显示列表），更新其子项的心跳
				没有结果：(表示为新的加入)，在all_object_sessions_obj查询其信息
					存在: 生成sessionbean添加到列表，
					不存在：显示无法获取对应的session会话，可以尝试重新调用ready来获取元数据


下步实现：
  修复bug，实时更新心跳

![image](https://user-images.githubusercontent.com/96420060/190707124-e93e91ab-ac0d-422c-969b-f440e0cd5290.png)

