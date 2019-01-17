## 用户

I2UP 默认内置以下类型用户：
* [X]租户系统管理员（tenant admin）：租户相关操作，登录名为`system`, 后续版本开放功能。
* 系统管理员（system admin）：用户增删改、用户权限管理，登录名为 `sysadmin`
* 业务管理员（business admin）：业务相关操作管理员，权限类似于6.x的系统管理员，登录名为 `admin`
* 业务操作员：具有业务操作权限, 需要系统管理员对不同功能模块进行授权，登录名为 `operator`
* 审计员：查看系统的操作日志，登录名为 `auditor`

>* 内置用户的初始密码全部是 Info1234， 建议登录后修改默认密码。
>* 只有“启用”状态的账号，才能登录到控台进行相关的操作。


* [用户管理](system_management/user_management.md)
* [角色管理](system_management/role_management.md)