# git 특강

---

## 1일차

---

- ## **CLI 기초**

  CLI : 터미널을 통해 사용자와 컴퓨터가 상호 작용하는 방식

  GUI : 그래픽을 통해 사용자와 컴퓨터가 상호 작용하는 방식

  새 폴더 만들기 : mkdir new file

  root directory : 모든 파일과 폴더를 담고 있는 최상위 폴더

  home directory : 현재 로그인 된 사용자의 홈 폴더

  절대 경로 : 루트 디렉토리부터 목적 지점까지 거치는 모든 경로를 전부 작성한 것

  상대 경로 : 현재 작업하고 있는 디렉토리를 기준으로 계산된 상대적 위치를 작성한 것

  ./ : 현재 작업하고 있는 폴더

  ../ : 현재 작업하고 있는 폴더의 부모 폴더

  - 명령어

    1. touch : 파일 생성 명령어

    2. mkdir : 새 폴더 생성 명령어

    3. ls : list segments, 현재 작업 중인 디렉토리의 폴더, 파일 목록을 보여주는 명령어

       ls -a : 숨김파일까지 모두 보여주는 명령어 옵션

       ls -l : long 옵션, 용량, 수정 날짜 등 파일 정보를 자세히 보여줌

    4. mv : move 폴더, 파일을 다른 폴더로 이동하거나 이름을 변경하는 명령어

    5. cd : change directory , 현재 작업 중인 디렉토리를 변경하는 명령어

       cd : 홈 디렉토리로 이동

       cd .. : 부모 디렉토리로 이동

    6. rm : remove , 폴더, 파일을 지우는 명령어, 완전 삭제

    7. open . : 폴더, 파일을 여는 명령어

- ## **Markdown**

  : 일반 텍스트 기반의 경량 마크업 언어

  마크다운의 본질은 글에게 역할을 부여하는 것

  역할에 맞는 마크다운 문법으로 작성

  - 마크다운 문법

    기울임 : *별 하나* _아래 하나_

    굵게 : **별 두개** __아래 두개__

    취소 : ~~물결 두개~~

    코드 작성 

    1) inline code : `inline code` 백틱 사용
    2) 블록 코드 : 백틱 3번 ```python```

    링크 [표시할 글자](이동주소)

    [Git class](https://hphk.notion.site/hphk/Git-22-01-12-22-01-14-34c8e006d667493985e8ba4a22000e92?p=27af349484724f3b945633e9a4adb638)

    이미지 : ![대체텍스트](이미지주소)

    ![Git logo](https://git-scm.com/images/logo@2x.png)

    

    > 인용 : > 이용

    표 

    | 동물 | 종류 | 다리개수 |
    | ---- | ---- | -------- |
    |      |      |          |
    |      |      |          |
    |      |      |          |

    수평선 

    ---

- ## **Git 기초**

   로컬 저장소

  working directory : 사용자의 일반적인 작업이 일어나는 곳
  staging area : 커밋을 위한 파일 및 폴더가 추가되는 곳

  repository : staging area 에 있던 파일 및 폴더의 변경사항을 저장하는 곳

  w.d-> s.a -> repository  과정으로 버전관리 수행

  1) git init : 현재 작업 중인 디렉토리를 git 으로 관리한다는 명령어

  2) git status : working directory와 staging area 에 있는 파일의 현재 상태를 알려주는 명령어

     Untracked : git 이 관리하지 않는 파일

     tracked : git이 관리하는 파일

     unmodified : 최신 상태

     Modified : 수정되었지만 staging area에 반영되지 않은 상태

     staged : staging area 에 올라간 상태

  3) git add : working directory 에 있는 파일을 staging area 로 올리는 명령어

     git이 해당 파일을 추적, 관리할 수 있도록 만듬

  4) git commit : staging area에 올라온 파일의 변경사항을 하나의 커밋(버전)으로 저장하는 명령어

     커밋 메세지는 현재 변경사항을 잘 나타낼 수 있도록 작성

     root commit 은 해당 커밋이 최초의 커밋일 때만 표시

  5) git log : 커밋의 내역을 조회할 수 있는 명령어

     --oneline : 한 줄로 축약

     --graph : 브랜치와 머지 내역을 그래프로 보여줌

     --all : 현재 브랜치를 포함한 모든 브랜치의 내역을 보여줌

     --reverse : 커밋 내역 순서를 반대로 보여줌

     -p : 파일 내용도 같이 보여줌

- ## **GitHub**

  원격 저장소 : 로컬 저장소를 다른 사람과 공유할 수 있음, 협업을 위해 로컬 저장소와 원격 저장소 연동

  6. git remote : 로컬 저장소에 원격 저장소를 등록, 조회, 삭제할 수 있는 명령어
     - 원격 저장소 등록 : git remote add <이름> <주소>
     - 원격 저장소 조회 : git remote -v 
     - 원격 저장소 연결 삭제 : git remote rm <이름> 
  7. 원격 저장소 업로드
     - 로컬 저장소에서 커밋 생성 
     - git push <저장소 이름> <브랜치 이름>