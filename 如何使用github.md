#为别人的项目做贡献
基本流程如下：

- 派生一个项目，并将项目保存在本地
  
-从 master 分支创建一个新分支

- 提交一些修改来改进项目

- 将这个分支推送到 GitHub 上

- 创建一个拉取请求

- 讨论，根据实际情况继续修改
 
- 项目的拥有者合并或关闭你的拉取请求

- 将更新后的 master 分支同步到你的派生中


申请pull request后，会进入一个和维护者的聊天界面，所有对该项目提交了pull request的人都会收到关于你这次聊天的消息。

**如果维护者要我们修改，我们就更新我们的分支，pull request会自动更新**


当我们fork别人的项目后，我们的项目会独立出来，git不会自动帮你更新原项目新的提交。需要我们自己git pull。

我们可以用这几行代码简化操作：
```
git add remote project <URL>

git branch --set-upstream-to=project/master master  跟踪分支

git config --local remote.pushDefault origin  设置默认push仓库
```

然后我们就可以
```
git pull

git push
```

#维护项目

可以在设置里面添加合作者 Collaborators。Collabotators拥有直接最项目push的权利。

##管理pull request请求
    当和贡献者交流完毕后，我们可以直接git pull <URL>/<Branch>或者把fork添加为一个remote ，再进行抓取合并。

    
    对于很琐碎的合并，github有'Merge'按钮，它是‘non-fast-foeward’合并。无论如何，会产生新的提交记录。