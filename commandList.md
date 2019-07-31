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



