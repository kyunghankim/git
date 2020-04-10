# Git

> Git은 분산버전관리시스템(DVCS) 중 하나이다.

수업 내용은 [git bash](https://gitforwindows.org/)를 기반으로 설명한다.

## Git 기초 흐름

### 0. 저장소 설정

```bash
$ git init
Initialized empty Git repository in C:/Users/student/Desktop/폴더/.git/
(master) $ 
```

* git 저장소를 만들게 되면 해당 디렉토리 내에 `.git/` 폴더가 생성된다.
* `git bash` 에서는 `(master)` 라는 표기가 같이 등장한다.
  * 현재 작업 중인 브랜치를 의미한다.

### 1. `add`

```bash
# a.txt를 만든 상황
$ git status
On branch master

No commits yet
# 트래킹 되고 있지 않은 파일들
# => git으로 버전을 남긴적이 없는 파일
Untracked files:
  # staging area에 포함시키려면, git add
  # (커밋될 파일 목록)
  (use "git add <file>..." to include in what will be committed)
        a.txt
# 커밋할 내용 없지만, 트래킹 되지 않는 파일은 존재한다.
# => WD O, Staging Area X
nothing added to commit but untracked files present (use "git add" to track)
```

* staging area에 추가

  ```bash
  $ git add a.txt      # a.txt 파일
  $ git add myfolder/  # myfolder 폴더
  $ git add .          # 현재 디렉토리
  ```

* 추가 후 상태

  ```bash
  $ git status
  On branch master
  
  No commits yet
  # 커밋될 변경사항들 (staging area)
  Changes to be committed:
    (use "git rm --cached <file>..." to unstage)
         # a.txt 새로 생성됨
          new file:   a.txt
  
  ```

### 2. `commit` 

> 커밋 메시지는 현재 버전에 대한 내용을 명확하게 작성

```bash
$ git commit -m '커밋메시지'
[master (root-commit) 41a723a] Init
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 a.txt
```

* 커밋 이력을 확인하기 위해서는 아래의 명령어를 입력한다.

  ```bash
  $ git log
  commit 41a723a3626a9737a7eb822441f4ba0aede37d9d (HEAD -> master)
  Author: edutak <edutak.ssafy@gmail.com>
  Date:   Fri Apr 10 10:45:22 2020 +0900
  
      Init
  $ git log -1   # 최근 한개 커밋
  $ git log --oneline # 간략한 로그
  $ git log --oneline -1 # 최근 한개의 커밋을 간략하게
  ```

  



## Git 원격저장소 활용(Github)

