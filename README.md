# pitfalls-git

#### 2017-06-24 (六)
情景: Git 默认对于文件名大小写不敏感，如果仅仅文件名大小写变化需要被 track 的话，需要通过以下命令行生效。

解决方案：在Git仓库根目录下输入命令行：git config core.ignorecase false

#### 2016-04-24 (日)
情景: 使用SourceTree第三方版本管理提交代码时, 出现部分文件无法提交的情况, 且不能进行Commit, Ignore等操作.

解决方案：此时可考虑使用终端命令: git add . 完成提交.

注意: 要保证在.git文件目录下使用命令.
