# Git_command

## .gitignore template
```
.idea/
.venv/
__pycache__
```

## **初始設置 (全局設置)**
```powershell
git config --global user.name "user_name"
git config --global user.email "user_email"
git config --global --list # check global setting
```

## **初始設置 (特定資料夾)**
```powershell
cd path/to/your/repository
git config user.name "user_name"
git config user.email "user_email"
git config --list (check local setting)
```

## **Clone file from URL**
```powershell
git clone URL
```

## **Set URL for the new folder**
```powershell
git init
git remote add origin URL
git pull origin main --allow-unrelated-histories
git push --set-upstream origin master #若還沒建立分支對應
#Check url
git remote -v
```

## **Change URL for the folder**
```powershell
git remote set-url origin URL
```
## **Add URL for the folder**
```powershell
git remote add <new_remote_name> URL
```

## **Add File to git and push**
```powershell
git add -u # 加入全部有更動的檔案
git add <file name> # 加入特定檔案
git commit -m "commit message" # 輸入commit訊息
git push origin main # 推送

git rm --cached filename.format # 移除追蹤的檔案
```

**設定不同的 fetch 和 push URL**
指定不同的遠端拉取或推送數據(需指定遠端的名稱 & 分支)<br>
```powershell
git pull <remote-name_A> <branch-name>
git push <remote-name_B> <branch-name>
```

**示例:**
(origin, backup, mirror)對應URL：(origin_URL, backup_URL, mirror_URL)

```powershell
# 拉取自 origin
git pull origin main

# 推送到 backup
git push backup main

# 同步到 mirror
git push mirror main
```
## 暴力pull 強制對齊origin
``` powershell
git fetch origin; git reset --hard origin/main; git clean -fd
```

## **Branch Setting**
```powershell
# 確保分支列表為最新
git fetch

# 查看本地（local）分支
git branch

# 查看所有遠端（remote）分支
git branch -r

# 查看本地 + 遠端的所有分支
git branch -a

# 本地新建一個分支並追蹤遠端的分支
git checkout -b new_branch_name origin/new_branch_name
git switch -c new_branch_name origin/new_branch_name (same)

```
