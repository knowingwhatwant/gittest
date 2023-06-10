# gittest
git远程使用流程





一、在github上创建新仓库

二、在本地创建同名文件夹，按照流程在本地进行初始化

```shell
$ mkdir dir                     # 创建测试目录
$ cd dir/                       # 进入测试目录
$ echo "Git test" >> README.md     # 创建 README.md 文件并写入内容
$ ls                                        # 查看目录下的文件
README
$ git init                                  # 初始化
$ git add README.md                         # 添加文件
$ git commit -m "添加 README.md 文件"        # 提交并备注信息
[master (root-commit) 0205aab] 添加 README.md 文件
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

# 提交到 Github
$ git remote add origin git@github.com:tianqixin/runoob-git-test.git   #创建一个别名
$ git push -u origin master										# push推送并且建立关联
```

必须至少有一个新文件才能提交和初始化

三、提取远程仓库

1、从远程仓库下载新分支和数据

```shell
git fetch
```

2、从远程仓库提取数据并且尝试合并到当前分支

```shell
git merge
```

假设你配置好了一个远程仓库，并且你想要提取更新的数据，你可以首先执行 **git fetch [alias]** 告诉 Git 去获取它有你没有的数据，然后你可以执行 **git merge [alias]/[branch]** 以将服务器上的任何更新（假设有人这时候推送到服务器了）合并到你的当前分支。

四、推送到远程仓库

推送新分支与数据到某个远端仓库命令

```shell
git push [alias] [branch]
```

五、删除远程仓库

```shell
git remote rm [alias]
```

