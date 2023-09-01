This is a [Next.js](https://nextjs.org/) project bootstrapped with [ `create-next-app` ](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx` . The page auto-updates as you edit the file.

This project uses [ `next/font` ](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

* [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
* [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

## 有关 git 的一些基本操作

* 查看仓库的远程链接: git remote -v
* 修改远程链接: git remote set-url origin <NEW_REMOTE_URL>
 > 注释： NEW_REMOTE_URL 为新的远程仓库地址  
 > origin 是默认的远程仓库名称，可以通过 git remote rename 命令修改  
 > 每个远程仓库配置下有两个链接: fetch 和 push
 
    - fetch: 用于从远程仓库拉取代码
    - push: 用于将本地代码推送到远程仓库

* 查看本地分支: git branch
* 查看远程分支: git branch -r
* 查看所有分支: git branch -a
* 创建分支: git branch <branch-name>
* 切换分支: git checkout <branch-name>
* 创建临时分支: git checkout -b <branch-name>
* 提交更改: git commit -m <commit-message>
* 推送更改: git push <remote-name> <branch-name>
* 拉取更改: git pull <remote-name> <branch-name>
* 创建并切换分支: git checkout -b <branch-name>
* 删除本地分支: git branch -d <branch-name>
* 强制删除本地分支并丢弃更改: git branch -D <branch-name>
* 删除远程分支: git push origin --delete <branch-name>
* 删除远程分支: git push origin :<branch-name>
* 合并分支: git merge <branch-name>
* 丢弃提交(不改变提交历史): git revert <commit-hash>
* 丢弃提交(改变提交历史): git reset [--hard] [--soft] <commit-hash>
    - --hard: 丢弃提交并丢弃更改
    - --soft: 丢弃提交但保留更改

## 有关 git 的一些高级操作

- 历史重写: git rebase -i HEAD~n
    - n 是一个数字，表示要重写的提交数量
- 完成重写: git rebase --continue
- 取消重写: git rebase --abort
- 重命名分支: git branch -m <old-branch-name> <new-branch-name>
- 查看远程仓库的默认分支: git symbolic-ref refs/remotes/origin/HEAD
- 查看远程仓库的默认分支: git remote show origin
- 将远程仓库的`HEAD`指向全部分支列表: git remote set-head origin --auto
- 切换新的远程分支: git remote set-url origin <new-remote-url>


* 报错：fatal: refusing to merge unrelated histories
    - 确认是否需要合并历史： 首先，确保您真的需要合并这些不相关的历史。如果这两个分支是在不同的上下文中开发的，合并可能会引入混乱，因为它们可能没有相关性。  
    - 使用 --allow-unrelated-histories： 如果您确定要合并这些不相关的历史，可以在合并命令中使用 --allow-unrelated-histories 参数。例如，如果您要将 feature 分支合并到 master 分支，可以这样做：git merge --allow-unrelated-histories feature  
    - 创建新的共同基础分支： 如果您需要在两个不相关的分支之间保留共同的历史，可以考虑创建一个新的共同基础分支，将两个分支合并到这个基础分支上，然后继续开发。
* 报错: error: unable to delete 'master': remote ref does not exist
    - 分支名称错误
    - 远程仓库同步问题
    - 本地分支与远程分支不一致
    - 权限问题
 > 解决： 远程仓库不存在， 删除本地的引用: git remote prune origin
