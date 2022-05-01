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

### 已經加入過的檔案，可以不用 git add 重加
### 用 git commit -am 同時加入這次的修改與訊息
git commit -am "訊息"
