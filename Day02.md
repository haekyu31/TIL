# 오늘 배운 내용을 작성해 봅니다!
github에 프로필을 만들었다
---
## .gitignore
> 특정 파일이나 폴더를 git이 관리하지 못하도록 지정한다
- `.gitignore`형식으로 만든다 
- [개발 환경에 맞는 `.gitignore` 찾는 사이트](https://www.toptal.com/developers/gitignore/)
---
### clone, pull ###
1. git clone
    > github에 있는 저장소에서 커밋내역을 가져와 로컬에 저장하는 방식
    로컬 컴퓨터에 원격저장소를 복제하여 로컬저장소를 만든다

2. git pull
   >원격저장소 커밋을 가져오는 형태 로컬저장소의 커밋을 원격저장소와 동기화 하고싶을때 사용한다. 

---
 ### branch ###
 branch는 나뭇가지로 master와 독립적으로 작업할수 있도록 만든 방식
 ```bash
 #브랜치 목록
 git branch
 #브랜치 생성
 git branch <>
 #브랜치 삭제
 git branch -d <> #병합된 브랜치
 git branch -D <> #브랜치 강제삭제
 ```
--- 
 ```bash
 git switch #브랜치 이동
 git switch -c <> #브랜치를 만들고 동시에 이동
 ```
- branch를 만들면 git branch로 어느 branch에 있는지 확인하고
- branch 에서 작업한다음 git add, git commmit을 해야한다.
- git push origin <branch> 로 github에 올려보낸다
- github에서 merge확인할수있다.

```bash
git merge <branch> #브랜치를 병합할때 사용하는 방법
#어느 branch에 있는지 확인해야한다.
#병합한 뒤에는 branch를 삭제한다
git branch -d <>
```