---
layout: post
title:  "Feb 23, 2021, TIL (Today I Learned) "
summary: "iOS 커리어 스타터 캠프 2기"
author: inwoodev
date: '2021-02-23 22:35:23 +0530'
category: SwiftProgramming
thumbnail: /assets/img/posts/light-bulbs.jpg
keywords: git, github, ios, swift, programming, startercamp, day2
permalink: /blog/TIL(Today I Learned)/
usemathjax: true

### 학습내용

---

![Git의 구조](/Users/hwang-in-u/Downloads/downloaded pictures/Git의 구조.png)

*출처: 야곰의 강의자료*

**Working Directory**

- 작업하는 일반적인 local 공간

  *`add`를 통해 Stage Area로 옮길 수 있음

**Stage Area**

- add된 자료가 모이는 공간

  *`commit`을 통해 Repository로 넘겨줄 수 있음

- git ignore의 활용

  *git ignore를 통해서 추적하고 싶지 않은 파일을 지정해줄 수 있음

**Repository** (내부 저장소(local repository) / 공유저장소(remote repository))

- 변경이력이 있는 저장소

  *`push`를 통해서 local repository → remote repository로 자료 업로드

  

#### Git 사용법 & Terminal 명령어

**Terminal 명령어**

- `cd 저장소_아이디`: 특정한 저장소로 디렉터리 경로를 이동한다.
- `mkdir 디렉토리_이름`: 디렉토리 생성
- `ls -a`: 현재 디렉토리 전체파일 확인
- `open 파일이름`: 파일 열기
- `touch 파일이름` 파일 생성
- `rm -rf`: 디렉토리 제거



**Terminal & Git**

- `git init`: git을 활용하여 디렉토리 추적 시작
- `git remote add origin (원격저장소_주소)`: 특정 url을 원격 저장소로 지정 

- `git clone <레포지토리_주소>`:  Fork를 통해 생성한 개인 저장소를 내 컴퓨터로 Clone

- `git checkout -t origin/브랜치_이름`:  특정한 브랜치에 추적 옵션을 준다. 

  *저장소 복제 후 한 번만 하면 된다.

- `git checkout -b 브랜치_이름`: 브랜치 생성과 해당 브랜치로 이동
- `git branch -d 브랜치_이름`: 브랜치 제거

- `git add`: 명령어를 통해서 Working Directory → Staging Area에 인덱스 등록

​	 `git add 파일명(또는 *) // 특정(또는 모든) 파일 추가`

- `git commit -m "코멘트_작성해주세요"`: 커밋 실행, 인덱스의 상태 기록하기

- `git push <저장소명> <브랜치명>`:  만들어진 커밋을 개인 저장소의 특정브랜치에 `push` 한다.

​	`ex) git push --set-upstream origin 브랜치_이름`

### 문제점 / 고민한 점

---

아직까지 `Terminal`을 활용하여 Git을 사용하기가 많이 어색하다. 아직까지 `branch`의 개념이 완벽하게 자리잡혀 있지 않아서 많이 해매는 감이 있다.



### 해결 방법

구글링하다 결국 선배 & 같은 팀원에게 도움을 요청했다.

리나, Fezz 그리고 다른 캠퍼분들께 여쭤보고 도움을 받으니 조금이나마 git에 대한 개념이 잡히는 것 같다. 자주 사용해서 얼른 익숙해 졌으면 좋겠다.



`git pull <저장소명> <브랜치명>`









