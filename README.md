

# Git 실습 1

## 1. test 폴더 생성후 깃생성

```bash
$ git init
Initialized empty Git repository in C:/Users/sku11/Desktop/test/.git/

```

## 2. a.txt파일생성

```bash
$ touch a.txt

~/Desktop/test (master)
$ ls
a.txt

```

## 3. a.txt 를 add하지 않고 commit한경우

```bash
$ git commit -m "Fistcommit"
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        a.txt

nothing added to commit but untracked files present (use "git add" to track)
```

## 4. 새로운 랜덤파일 생성 후 상태메시지

```bash
$ touch k.docx

sku11@DESKTOP-NLSF6RL MINGW64 ~/Desktop/test (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        a.txt
        k.docx

nothing added to commit but untracked files present (use "git add" to track)
```

## 5. a.txt 파일만 add

```bash
sku11@DESKTOP-NLSF6RL MINGW64 ~/Desktop/test (master)
$ git add a.txt

sku11@DESKTOP-NLSF6RL MINGW64 ~/Desktop/test (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   a.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        k.docx
```

## 6. 모든파일 add

```bash
sku11@DESKTOP-NLSF6RL MINGW64 ~/Desktop/test (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   a.txt
        new file:   k.docx
```

## 7. 커밋 및 커밋 후 상태메시지

```bash
sku11@DESKTOP-NLSF6RL MINGW64 ~/Desktop/test (master)
$ git commit -m "secondcommit"
[master (root-commit) ac81427] secondcommit
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 a.txt
 create mode 100644 k.docx
 
sku11@DESKTOP-NLSF6RL MINGW64 ~/Desktop/test (master)
$ git status
On branch master
nothing to commit, working tree clean
```

## 8. a.txt 파일 수정 후 상태

```bash
sku11@DESKTOP-NLSF6RL MINGW64 ~/Desktop/test (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   a.txt

no changes added to commit (use "git add" and/or "git commit -a")

sku11@DESKTOP-NLSF6RL MINGW64 ~/Desktop/test (master)
$ git add a.txt
```

## 이후 깃 커밋 하면됨

## 깃헙의 사용자정보

```bash
sku11@DESKTOP-NLSF6RL MINGW64 ~/Desktop/test (master)
$ git config --global -l
user.name=yw
user.email=kimyw80@gmail.com
core.autocrlf=true
```

```bash
sku11@DESKTOP-NLSF6RL MINGW64 ~/Desktop/test (master)
$ git remote add origin https://github.com/kim-bob/github_test.git

sku11@DESKTOP-NLSF6RL MINGW64 ~/Desktop/test (master)
$ git push origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 212 bytes | 106.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/kim-bob/github_test.git
 * [new branch]      master -> master
git remote add origin
```

```bash
git remote -v #verbose
orig
git remote add origin 
git remote add origin http://github.com/<username>/,<> 
```

