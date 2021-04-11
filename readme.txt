git add readme.txt          //新增或修改文件
git commit -m "提交和注释"  //提交到仓库
git status  //查看当前是否有为提交的修改
git diff    //查看修改了哪些
git log     //查看版本的历史记录
git log --pretty=oneline  //查看历史记录的简洁
git reset --hard HEAD^    //回退到上一个版本
git reset --hard commit_id//回退到某个版本，commit_id  表示版本id，只需要前前面几位就好
git reflog  //查看每一条记录，避免执行 reset 之后，想恢复原本最新的版本时，找不到版本号，而 git reflog 可以记录每一条操作
// 工作区 -git add-> 版本库 stage 区 -git commit-> 版本库 master
//执行 git add 之后再修改文件再执行 git commit，只提交了第一次修改的记录，这也说明了 git 是面对修改而非面对文件