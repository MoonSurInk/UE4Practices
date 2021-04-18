# UE4Practices
Repository dedicated for UE4 practices

## UE4GitPlugin 安装  
0. 前提
操作系统必须事先安装 Git 软件 以及 Git LFS （Large File Storage）
```  
git config --global user.name "XXX"  
git config --global user.email XXX@gmail.com  
git lfs install  
```  

1. 为 UE4 安装 Git 插件  
从开发者Github获取最新的Release版本：https://github.com/SRombauts/UE4GitPlugin/releases  
**注意Engine的版本**  

下载后，将其解压到项目的 <YourGameProject>/Plugins 目录下  
*只能放在项目中不能放Engine下*  


2. 使用Git对资源进行版本控制  
  - 在你的项目主目录下Clone Git仓库，创建成功后会在主目录下出现 .git 目录。  
  - 使用UE4编辑器打开 MyProject 项目，通过Connect To Source Control-> 选择Git lfs 2。  
  - 勾选两个LFS选项  
  *Git软件所处的路径通常默认在C盘，如果不是，请手动重新指定*  
or  
  - 直接打开项目，通过Connect To Source Control-> 选择Git lfs 2 
  - 输入Root Url  
  - 勾选两个LFS选项
  - 在弹出的登入框中登陆GitHub

### Supported features
- initialize a new Git local repository ('git init') to manage your UE4 Game Project
  - can also create an appropriate .gitignore file as part of initialization
  - can also create a .gitattributes file to enable Git LFS (Large File System) as part of initialization
  - can also enable Git LFS 2.x File Locks as part of initialization
  - can also make the initial commit, with custom multi-line message
- display status icons to show modified/added/deleted/untracked files, not at head and conflicted
- show history of a file
- visual diff of a blueprint against depot or between previous versions of a file
- revert modifications of a file (works best with "Content Hot-Reload" experimental option of UE4.15, by default since 4.16)
- add, delete, rename a file
- checkin/commit a file (cannot handle atomically more than 50 files)
- migrate an asset between two projects if both are using Git
- solve a merge conflict on a blueprint
- show current branch name in status text
- Configure remote origin URL ('git remote add origin url')
- Sync to Pull (rebase) the current branch if there is no local modified files
- Push the current branch
- Git LFS (Github, Gitlab, Bitbucket), git-annex, git-fat and git-media are working with Git 2.10+
- Git LFS 2 File Locks
- Windows, Mac and Linux
