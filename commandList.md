 command                   | description                                    
-|-
 git init                | 初始化一个Git仓库                               
 git add <file>          | 添加文件到仓库（但未提交）                      
 git commit -m <message> | 提交修改到仓库,  -m  后面输入的是本次提交的说明 
 查看文件差异与监控修改       |                                         
 git status                 | 查看工作区的状态                        
 git diff <file>            | 查看修改内容 (比较工作区和暂存区的区别) 
 版本跳转                     |                                         
  HEAD                        | 指向当前版本版本号                      
  git log                     | 可以查看提交历史                        
  git reflog                  | 查看命令历史                            
  git reset --hard commit_id  | 在版本的历史之间穿梭                    
 撤销修改                     |                                         
  git checkout -- <file>      | 在工作区撤销修改                        
  git reset HEAD <file>       | 在暂存区撤销修改                        
 删除文件                     |                                         
  git rm <file>               | 从版本库中删除该文件                    
 添加远程库                                                 |                                
 git remote add origin git@server-name:path/repo-name.git | 关联一个远程库                 
 git push -u origin master                                | 第一次推送master分支的所有内容 
 git push origin master                                   | 推送最新修改                   
 从远程库克隆                                               |                                
 git clone git@server-name:path/repo-name.git             | 给定仓库地址克隆仓库           


## 分支管理
 command                                                    | description                            
-|-
 创建与合并分支                                             |                                        
  git branch                                                | 查看分支                               
  git branch <name>                                         | 创建分支                               
  git branch -d <name>                                      | 删除分支                               
  git branch -D <name>                                      | 强制删除没有被合并过的分支             
  git checkout <name>                                       | 切换分支                               
  git checkout -b <name>                                    | 创建+切换分支                          
  git merge <name>                                          | 合并某分支到当前分支                   
  git merge --no-ff -m "xxx" <name>                         | 强制禁用  Fast forward  合并           
  git log --graph --pretty=oneline --abbrev-commit          | 查看分支合并图                         
 Bug 分支                                                   |                                        
  git stash                                                 | 将当前暂存区内容保持现场               
  git stash list                                            | 查看保存现场列表                       
  git stash apply <name>                                    | 恢复指定现场,不删除现场                
  git stash drop <name>                                     | 删除指定现场                           
  git stash pop                                             | 恢复并删除现场                         
多人协作                                                   |                                        
  git remote -v                                             | 查看远程库信息                        
  git push origin branch-name                               | 本地推送分支                           
  git pull                                                  | 抓取远程分支，如果有冲突，要先处理冲突 
  git checkout -b branch-name origin/branch-name            | 本地创建和远程分支对应的分支           
  git branch --set-upstream branch-name origin/branch-name  | 建立本地分支和远程分支的关联           
  git rebase                                                | 将本地未push的分支提交历史整理成直线   


# tag 指令
 command                                  | description                                       
-|-
  git tag <tagname>                       | 新建一个标签，默认为HEAD，也可以指定一个commit id 
  git tag -a <tagname> -m "blablabla..."  | 可以指定标签信息                                  
  git tag                                 | 查看所有标签                                      
  git push origin <tagname>               | 推送一个本地标签                                  
  git push origin --tags                  | 推送全部未推送过的本地标签                        
  git tag -d <tagname>                    | 删除一个本地标签                                  
  git push origin :refs/tags/<tagname>    | 删除一个远程标签                                  

