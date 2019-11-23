# rebase使用

git rebase (变基)      使git记录简简洁

第一种：

    多个记录-->一个记录
   
第二种：

    使git记录简洁
第三种：
     
 1. 下班公司提交代码
 2. 回到家中拉取代码合并继续开发
 3. 开发完成提交代码
 4. 第二天回到公司git pull拉取代码合并
 
这样拉取肯定会产生分叉

git pull origin dev
换成
git fetch origin dev
git rebase origin/dev

* 注意：
git rebase 可能产生冲突
* 解决：
和meger一样根据提示
git add -A
git rebase --continue

快速解决冲突
     
 1. 安装beyond compare
 2. 在git中配置
    git config --local merge.tool bc3
    git config --local mergetool.path "安装路径"
    git config --local mergetool.keepBackup false
3、应用beyond compare解决冲突
git mergetool





·  git add -A  提交所有变化

·  git add -u  提交被修改(modified)和被删除(deleted)文件，不包括新文件(new)

·  git add .  提交新文件(new)和被修改(modified)文件，不包括被删除(deleted)文件