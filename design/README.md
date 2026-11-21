# 共用设计源码

tokens.css 定义主题颜色，navigation.css 定义站间导航，sites.json 保存站点名称与地址，icons/ 保存 SVG 原稿。

消费者以 design.lock 中的完整 Git 提交为版本，在构建前运行 scripts/sync-design.py。生成目录不提交。更新时先修改锁文件并构建各站预览。回退时恢复旧锁文件后重建。主页通过 Hugo mounts 读取当前仓库内的同一份源码。
