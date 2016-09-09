# Windows server configuration

云件Windows服务器配置手册
## 基础配置（准备工作）
### 添加非管理员组策略
* run: mmc
* 文件 > 添加/删除管理单元
* 左边选择组策略对象编辑器 > 添加 > 浏览 > 用户 > 非管理员 > 确定 > 完成 > 确定
* 文件 > 另存为 > ummc.msc

> 后文中将该管理控制台称为**ummc**

## Internet Explorer

### 设置全局代理

* run: gpedit.msc
* 左边展开：计算机配置 > 管理模板 > Windows组件 > Internet Explorer
* 右边选择：按计算机（而不是按用户）进行代理设置 > 启用
* 设置Administrator代理

### 其他配置
* run: ummc
* 本地计算机\非管理员 策略 > 用户配置 > 管理模板 > Windows组件 > Internet Explorer
* 禁用更改主页设置
* 禁用更改连接设置
* 阻止更改代理设置
