# git常用命令
- 版本初始化
 ```shell
git init
 ```
- 添加到暂存区
```shell
git add 文件
```
- 提交
```shell
git commit -m  变更说明
```
- 查看变更记录
```shell
git log 
git log --pretty=oneline // 一行显示
```
- 回退版本
```shell
git reset --hard HEAD^ 回退到上个版本
git reset --hard HEAD^^ 回退到上上个版本
git reset --hard HEAD~100 回退到上100个版本
git reset --hard 版本号
```
- 查看版本所有历史记录(包括回退记录)
```shell
git reflog
```
- 撤销操作
```shell
git commit --amend //修正提交(覆盖上次提交)
git reset HEAD 文件 // 撤销暂存文件
git checkout -- 文件 // 撤销文件修改(回到当前版本或者当前暂存版本，对删除的文件可找回)
```
- 查看工作区状态
```shell
git status // 文件修改和暂存区信息
```
- 比较工作区和当前版本库的差异
```shell
git diff HEAD -- 文件
```
- 删除文件
```shell
git rm 文件 
git commit -m 删除说明
git checkout -- 文件 恢复删除的文件(从版本库中撤销删除)
//先手动删除文件，然后使用git rm <file>和git add<file>效果是一样的。
```
- git配置
```shell
git config --list //查看所有配置
git config user.name //查看用户名
git config user.email //查看邮箱
git config --global user.name "username" //设置全局配置
git config --global user.eamil "youname@email.com" // 设置全局邮箱
```
- git推送到远程
```shell
git remote add orgin git@github.com:username/repositoryname.git //添加远程仓库
git push -u origin master // 第一次推送到远程，关联本地和远程库
git push origin master //推动到远程
```
## 分支系统
- 创建分支
```shell
git checkout -b dev //创建并切换分支
git branch dev      //创建分支
git checkout dev    //切换分支
git branch          //查看分支
git merge dev       //合并分支
git branch -d dev   //删除分支
git switch  -c dev  //创建并切换分支
git switch dev      //切换分支
```
# 生成证书
- 在window 上生成证书
```shell
ssh-keygen -t rsa -C "youremail@example.com"
```
