**特别说明：**
源类型为db2备份，支持备份类型为db2的在线备份，所以备份之前，应该满足db2备份做在线备份的要求
*  在线备份db2数据库应处于归档模式

  db2 update db cfg for xxx using LOGRETAIN ON
 
  ![说明: 1](/assets/backup06031.png)

*  如果做全备+增量的数据库备份，需要开启数据库的增量模式

  db2 update db cfg for xxx using TRACKMOD on

*  开启归档模式以及启用数据库增量模式，需要做一次离线全备

  ![说明: 1](/assets/backup06032.png)
  


*   “启用模板”： 客户可以选择自己已经保存的模板，便于节省时间；
*   “备份名称”：备份规则的名字可按照自己的习惯填写
*   “工作机”：系统自动列出该用户创建的所有工作机节点和混合节点
*   “灾备机“：系统自动列出所有灾备机节点和混合节点
*   “源类型”：源类型分为四类 文件，块设备，oracle，mssql server
*   “目标类型”：文件，raw数据

  源类型与目标类型的对应关系：文件-&gt;文件，文件-&gt;raw数据，块设备-&gt;文件，块设备-&gt;raw数据，oracle-&gt;文件，mssql server-&gt;文件

选择 db2-&gt;文件即db2备份
*   “超时阈值”：超过时间阙值还没有完成备份则产生告警
*   “灾备机目标路径”：工作机需要保护的文件或者目录将要备份到此目录下
*   “db2数据库名称”：需要备份的db2数据库名称










