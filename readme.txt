git add readme.txt          //新增或修改文件
git commit -m "提交和注释"  //提交到仓库
git status  //查看当前是否有为提交的修改
git diff    //查看修改了哪些
git log     //查看版本的历史记录
git log --pretty=oneline  //查看历史记录的简洁
git reset --hard HEAD^    //回退到上一个版本
git reset --hard <commit_id>//回退到某个版本，commit_id  表示版本id，只需要前前面几位就好
git reflog  //查看每一条记录，避免执行 reset 之后，想恢复原本最新的版本时，找不到版本号，而 git reflog 可以记录每一条操作
// 工作区 -git add-> 版本库 stage 区 -git commit-> 版本库 master
//执行 git add 之后再修改文件再执行 git commit，只提交了第一次修改的记录，这也说明了 git 是面对修改而非面对文件
git checkout -- readme.txt // 将 readme 文件撤销回最近一次 git add 或 git commit 时的状态。未提到暂存就恢复成版本库，已提交到暂存区，就恢复成暂存区。
git checkout -- <file> //表示撤销修改,若没有 -- 就是切换到另一个分支

git reset HEAD <file>  //把暂存区的修改回退到工作区

rm <file> 
删除文件后再 git 将改文件删除
 - git rm <file>
 - git commit -m ""
删除文件后恢复
 - git checkout -- <file> 

// 添加远程库
git remote add origin git@github.com:Michael-Bao/learngit.git
git remote add <remote-name> <remote-address> //添加远程仓库的地址

// 推送到远程库
git push -u origin master
git push -u <remote-name> <remote-address> // 第一次推送 master 加上 -u，还能起到本地和远程的 master 关联起来的作用，后续就无需加 -u，还能起到本地和远程的

// 查看远程库
git remote -v

// 删除本地与远程库的关联
git remote rm origin

// 从远程库克隆
git clone <remote-address>

// 创建与合并分支
git branch <branch-name> //创建分支
git checkout <branch-name> //切换到分支
git checkout -b <branch-name> //创建并切换到分支

// 查看分支
git branch

// 合并分支
git merge dev
// 合并模式：快进模式

// 删除分支
git branch -d <branch-name>

// xx 版本的 git 开始可以通过 switch 创建和切换分支
git switch <branch-name>    //切
git switch -c <branch-name> //创并切

//解决冲突
git merge <branch-name> //提示冲突并进入 master | merging 状态
//修改文件
git add . 
git commit -m "解决冲突" //合并成功
git log --graph --pretty=oneline --abbrev-commit //查看合并图；--pretty=oneline 展示更多；--abbrev-commit 缩写。

//禁用 fast forward


