# Git 指令

----

## 終端機指令
| Windows    | MacOS/Linux | 說明                     |
| ---------- | ----------- | ------------------------ |
| pwd        | pwd         | 顯示目前所在路徑           |
| cd         | cd          | 切換目錄 change directory |
| mkdir      | mkdir       | 建立新的資料夾 make dir   |
| type null >| touch       | 建立新的檔案              |
| dir        | ls          | 列出目前資料夾的檔案列表 list |
| copy       | cp          | 複製檔案 copy  |
| move       | mv          | 移動檔案 move  |
| del        | rm          | 刪除檔案 remove |
| cls        | clear       | 清除畫面上的內容 |

----

### 把檔案從 工作目錄 加到 暫存區
git add a.txt

git commit -m "記錄這次提交的緣由"

### 查看 commit log
git log

### 反悔加入暫存區，但保留檔案
git rm --cached file

### 反悔加入暫存區，而且真的刪除檔案
git rm -f file

### 比較檔案的差異 確認後，可以按 q 離開
git diff

### 用 git commit -am 同時加入這次的修改與訊息
git commit -am "訊息"

----

## git log 指令的運用

### 看commitID跟歷史紀錄
git log
git log --oneline --graph //簡短的歷史紀錄只會顯示7碼

### 查看特定檔案的紀錄
git log a.txt

### 查看檔案修改細節
git log -p a.txt

### 查看統計的檔案修改細節（次數）
git log --stat

### 可以搜尋關鍵字
git log --grep="delete"

### 查看內容是誰編寫的
git blame hello.txt

### 從暫存區域回到工作目錄
git restore --staged {檔案名稱}

### 捨棄在工作目錄的改變(包括修改與刪除)
git restore {檔案名稱}

----

## 建立分支與合併

### vscode 套件: git graph

### 檢視分支
git branch

### 新增分支
git branch {branch-name}

### 切換分支
git switch {branch-name}
git checkout {branch-name}

### 合併分支, 例如把 feature-login 合併進去 main
### 先切換到 main
git switch main
### 再把 feature-login 合併進來
git merge feature-login

### 刪除本地分支
git branch -d {branch-name}
