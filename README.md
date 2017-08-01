# pitfalls-git

#### 2017-07-29 (六)

情景：公司所有人提交代码的时候，遇到以下问题。

```
git -c diff.mnemonicprefix=false -c core.quotepath=false -c credential.helper=sourcetree push -v --tags origin refs/heads/luyonghe:refs/heads/luyonghe refs/heads/master:refs/heads/master 
Pushing to http://192.168.11.20/gitlab/snaillove/platform-ios-library-cloud-music.git
POST git-receive-pack (2240 bytes)
remote: error: unable to create temporary file: No space left on device        
remote: fatal: failed to write object        
error: unpack failed: unpack-objects abnormal exit
To http://192.168.11.20/gitlab/snaillove/platform-ios-library-cloud-music.git
 = [up to date]      0.0.1 -> 0.0.1
 = [up to date]      0.0.10 -> 0.0.10
 = [up to date]      0.0.11 -> 0.0.11
 = [up to date]      0.0.12 -> 0.0.12
 = [up to date]      0.0.13 -> 0.0.13
 = [up to date]      0.0.14 -> 0.0.14
 = [up to date]      0.0.15 -> 0.0.15
 = [up to date]      0.0.16 -> 0.0.16
 = [up to date]      0.0.17 -> 0.0.17
 = [up to date]      0.0.18 -> 0.0.18
 = [up to date]      0.0.19 -> 0.0.19
 = [up to date]      0.0.2 -> 0.0.2
 = [up to date]      0.0.20 -> 0.0.20
 = [up to date]      0.0.21 -> 0.0.21
 = [up to date]      0.0.22 -> 0.0.22
 = [up to date]      0.0.23 -> 0.0.23
 = [up to date]      0.0.24 -> 0.0.24
 = [up to date]      0.0.25 -> 0.0.25
 = [up to date]      0.0.27 -> 0.0.27
 = [up to date]      0.0.28 -> 0.0.28
 = [up to date]      0.0.29 -> 0.0.29
 = [up to date]      0.0.3 -> 0.0.3
 = [up to date]      0.0.30 -> 0.0.30
 = [up to date]      0.0.31 -> 0.0.31
 = [up to date]      0.0.32 -> 0.0.32
 = [up to date]      0.0.33 -> 0.0.33
 = [up to date]      0.0.34 -> 0.0.34
 = [up to date]      0.0.35 -> 0.0.35
 = [up to date]      0.0.36 -> 0.0.36
 = [up to date]      0.0.37 -> 0.0.37
 = [up to date]      0.0.38 -> 0.0.38
 = [up to date]      0.0.39 -> 0.0.39
 = [up to date]      0.0.4 -> 0.0.4
 = [up to date]      0.0.40 -> 0.0.40
 = [up to date]      0.0.41 -> 0.0.41
 = [up to date]      0.0.42 -> 0.0.42
 = [up to date]      0.0.43 -> 0.0.43
 = [up to date]      0.0.44 -> 0.0.44
 = [up to date]      0.0.5 -> 0.0.5
 = [up to date]      0.0.56 -> 0.0.56
 = [up to date]      0.0.6 -> 0.0.6
 = [up to date]      0.0.8 -> 0.0.8
 = [up to date]      0.0.9 -> 0.0.9
 = [up to date]      v0.0.45 -> v0.0.45
 = [up to date]      v0.0.50 -> v0.0.50
 = [up to date]      v0.0.51 -> v0.0.51
 = [up to date]      v0.0.52 -> v0.0.52
 = [up to date]      v0.0.53 -> v0.0.53
 = [up to date]      v0.0.54 -> v0.0.54
 = [up to date]      v0.0.55 -> v0.0.55
 = [up to date]      v0.0.57 -> v0.0.57
 = [up to date]      v0.0.58 -> v0.0.58
 = [up to date]      v0.0.59 -> v0.0.59
 = [up to date]      v0.0.60 -> v0.0.60
 = [up to date]      v0.0.61 -> v0.0.61
 = [up to date]      v0.0.62 -> v0.0.62
 = [up to date]      v0.0.63 -> v0.0.63
 = [up to date]      v0.0.64 -> v0.0.64
 = [up to date]      v0.0.65 -> v0.0.65
 = [up to date]      v0.0.66 -> v0.0.66
 = [up to date]      v0.0.67 -> v0.0.67
 = [up to date]      v0.0.68 -> v0.0.68
 = [up to date]      v0.0.69 -> v0.0.69
 = [up to date]      v0.0.70 -> v0.0.70
 = [up to date]      v0.0.71 -> v0.0.71
 = [up to date]      v0.0.72 -> v0.0.72
 = [up to date]      v0.0.73 -> v0.0.73
 = [up to date]      v0.0.74 -> v0.0.74
 = [up to date]      v0.0.75 -> v0.0.75
 = [up to date]      v0.0.76 -> v0.0.76
 = [up to date]      v0.0.80 -> v0.0.80
 = [up to date]      v0.0.82 -> v0.0.82
 = [up to date]      v0.0.83 -> v0.0.83
 = [up to date]      v0.0.87 -> v0.0.87
 = [up to date]      v0.46 -> v0.46
 = [up to date]      v0.47 -> v0.47
 = [up to date]      v0.48 -> v0.48
 = [up to date]      v0.49 -> v0.49
 = [up to date]      v0.80 -> v0.80
 ! [remote rejected] luyonghe -> luyonghe (unpacker error)
 ! [remote rejected] master -> master (unpacker error)
error: failed to push some refs to 'http://192.168.11.20/gitlab/snaillove/platform-ios-library-cloud-music.git'
Completed with errors, see above
```

解决方法：初步推测，是后台服务器空间已经满了。后来经过确认，是备份的数据太多，占用了很大的空间，清理了之后，解决了这个问题。

情景：在 GitHub 中通过 pull/request 形式 contribute 一个项目，提交内容被合并之后，发现 contributor 列表中却没有自己。

问题分析：一般来说，这种问题是你提交时候的个人用户名/邮件（主要是邮件），与你 GitHub 上的邮件地址不一致导致的。

解决方案：将两者的邮件地址保持一致。


#### 2017-07-19 (三)
情景：有一个其他已经被Git管理的项目，整个文件夹复制到一个原有的被Git管理的项目中，出现被复制过来的项目不能被Track。  

解决方案：删除掉被复制过来的项目中的.git隐藏文件夹即可。

今天遇到一个iOS项目，先从Github上clone下来一个项目，然后将已经有的项目再Copy进去，发现新增的内容并没有被Track，后来发现是因为，新Copy进入的项目中也包含有Git信息，将此Git信息删除掉即可（备注：.git隐藏文件夹）。

#### 2017-06-24 (六)
情景: Git 默认对于文件名大小写不敏感，如果仅仅文件名大小写变化需要被 track 的话，需要通过以下命令行生效。

解决方案：在Git仓库根目录下输入命令行：git config core.ignorecase false

#### 2016-04-24 (日)
情景: 使用SourceTree第三方版本管理提交代码时, 出现部分文件无法提交的情况, 且不能进行Commit, Ignore等操作.

解决方案：此时可考虑使用终端命令: git add . 完成提交.

注意: 要保证在.git文件目录下使用命令.
