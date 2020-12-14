###### tags: `note`

# GIT 小技巧

如何繼續使用 Git revert 的記錄
===

###### h6切換至原分支
```bash
git checkout [分支名稱]
```

###### 還原記錄
```bash
git reset --soft HEAD^
```

###### 將異動的檔案暫存起來
```bash
git stash
```

###### 開新分支
```bash
git checkout -b [新分支]
```

###### 將暫存的檔案還原
```bash
git stash pop
```

## Git 查詢及同時刪除本地及遠端分支


###### 設定一次刪除本地及遠端分支的指令

```bash
git config --global alias.rmbranch '!f(){ git branch -D ${1} && git push origin --delete ${1}; };f'
```

###### 查詢分支
```bash
git branch -a | grep '[分支名稱]'
```
