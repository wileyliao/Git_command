# Git_command

## **初始設置 (全局設置)**
```
git config --global user.name "user_name"
git config --global user.email "user_email"
git config --global --list (check global setting)
```

## **初始設置 (特定資料夾)**
```
cd path/to/your/repository
git config user.name "user_name"
git config user.email "user_email"
git config --list (check local setting)
```

## **Clone file from URL**
`git clone URL`

## **Set URL for the new folder**
```
git init
git remote add origin URL
git pull origin main --allow-unrelated-histories
#Check url
git remote -v
```

## **Change URL for the folder**
`git remote set-url origin URL`

## **Add URL for the folder**
`git remote add <new_remote_name> URL`

## **Add File to git and push
`git add .` 全部加入
`git add <file name> `
`git commit -m "commit message"`
`git push origin main`

**設定不同的 fetch 和 push URL**
指定不同的遠端拉取或推送數據(需指定遠端的名稱 & 分支)<br>
```
git pull <remote-name_A> <branch-name>
git push <remote-name_B> <branch-name>
```

**示例:**
(origin, backup, mirror)對應URL：(origin_URL, backup_URL, mirror_URL)

```
# 拉取自 origin
git pull origin main

# 推送到 backup
git push backup main

# 同步到 mirror
git push mirror main
```
