# Git 원격 저장소 활용

> 부제 : 집에서 수업 내용 복습하는 법

* 집에 git 저장소가 없는 경우 `clone` 을 받는다.

  ```bash
  $ git clone {__url__}
  ```

## 시나리오

1. 멀캠

   1. `commit` 

      * 수업 종료 후 commit

      ```bash
      $ git commit -m '4/10 - 케라스 활용방법'
      ```

   2. `push`

      ```bash
      $ git push origin master
      ```

2. 집

   1. `pull`

      ```bash
      $ git pull origin master
      ```

   2. 복습 

   3. `commit` 

      ```bash
      $ git commit -m '4/10 - keras 복습(블로그 정리)'
      ```

   4. `push`

      ```bash
      $ git push origin master
      ```

3. 다음날

   ```bash
   $ git pull origin master
   ```

   * 수업을 잘 듣는다.









