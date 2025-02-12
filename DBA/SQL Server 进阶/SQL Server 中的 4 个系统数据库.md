# SQL Server 中的 4 个系统数据库

#### master 数据库

​	记录SQL server 系统的所有系统级别信息。它记录所有的登录账户和系统配置设置。master数据库是这样一个数据库，它记录所有其他的数据库，其中包括数据库文件的位置，master数据库记录SQL server 的初始化信息，它始终有一个可用的最新master数据库备份。

#### model 数据库

​	model 数据库用作在系统上创建的所有数据库模板。当发出CREATE DATABASE 语句时，新数据库的第一部分通过复制model数据库中的内容创建，剩余部分由空页填充。由于SQL server 每次启动时都要创建 tempdb 数据库，model 数据库必须一直存在于SQL server 系统中。

#### msdb 数据库

​	msdb数据库供SQL server 代理程序调度警报和作业以及记录操作员时使用。

#### tempdb 数据库

​	用于保存所有的临时表和临时存储过程。它还满足任何其他的临时存储要求，例如存储SQL server 生成的工作表。