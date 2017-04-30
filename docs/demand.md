# 需求

## 功能需求（筹）

-|-
-|-
功能|创建事体
编号|FR-IO-001
优先级|高
用户场景|调研者、立项者
功能描述|使用事体笔记需要创建事体作为信息的容器，可以有匿名的事体被自动创建出来。
处理流程|检查当前账户下是否已经有事体存在，不存在则创建一个匿名事体
用户痛点|有了一个用于放所有项目文件的「文件夹」
补充说明|事体每次形成占意，都连接到 neo4j 时间树的起止日期上

-|-
-|-
功能|创建和编辑笔记
编号|FR-IO-002
优先级|高
用户场景|调研者、立项者
功能描述|将blob（二进制大文件）存到数据库里，blob可以是任何格式，并存放在某些事体里
处理流程|根据用户意愿将blob关联到至少一个事体上
用户痛点|用户可能上传任何文件，想把笔记系统当仓库云使用，而且还能添加「快捷方式」
补充说明|目前想存在 mongo 里

-|-
-|-
功能|创建子事体
编号|FR-IO-003
优先级|低
用户场景|调研者、立项者
功能描述|每个事体可以被分解为多个子事体，当分解得足够细致后，子事体就可能和以前出现过的其他子事体有相似之处，此时可以做推荐
处理流程|要求用户输入事体名称，用名称产生推荐，子事体创建后将其关联到父事体上
用户痛点|知识复用
补充说明|推荐难做，对目前来说是深坑一个

-|-
-|-
功能|查看笔记
编号|FR-UI-001
优先级|高
用户场景|调研者
功能描述|将blob以其格式展示在网页上
处理流程|根据blob格式，使用适当的插件渲染内容
用户痛点|PDF和markdown都可以查看
补充说明|主要支持 markdown，其他某些数据的格式可以是一段 JS 的地址，就用这段 JS 来渲染内容为 iframe

-|-
-|-
功能|查看相关事体和模因
编号|FR-UI-002
优先级|中
用户场景|调研者、阅读者
功能描述|在笔记边栏显示本笔记所在的事体、本笔记各段落相关的模因或事体。打开事体时显示各模因所属的事体
处理流程|随着笔记滚动，边栏同步滚动，并用有色线段标识出段落与模因或事体的相关性
用户痛点|方便用户通过摘要型模因进行知识探索或交互式搜索
补充说明|类似于「PROJECT XANADU®」或某些同步滚动的 Markdown 预览，也为类 quip 的文档评论提供了可能，还可以插入广告呢！

-|-
-|-
功能|渲染插件系统
编号|FR-PLUG-001
优先级|中
用户场景|阅读者
功能描述|用个性化的 JS 脚本渲染 blob（二进制大文件）
处理流程|
用户痛点|用户可能想看 CSV 格式渲染出来的标签云、想用自己的 Markdown 渲染器等
补充说明|还不会设计插件系统，需要时间学习（坑！）

## 非功能需求

### 安全需求

### 性能需求

暂不理会此类需求

### 日志记录

实现回滚或行为采集

### 文档需求

个人开发，原型系统，文档误国

### 盈利需求

大公无私，只求无过