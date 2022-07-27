# TIL
## pull request (fork방식)
> 원격저장소 소유권이 없는경우 사용

- 원격저장소에서 fork 를 통해 내 원격저장소로 가져온다. 
- clone을 통해 내 로컬저장소로 복제해온다.
- 로컬과 원본 원격저장소를 연결한다.

```bash
 git remote add upstream <url>
```
- 브랜치를 생성하고 작업을 한다.
```bash
git switch -c <branch>
```

- 작업이 끝나면 origin에 브랜치를 push한다

```bash
git push origin <branch>
```
- github에서 pull request를 통해 upstream에 요청을 보낸다.
- 병합이 되었다면 pull로 upstream에서 로컬로 내용을 가져온다. 기존 로컬 branch는 삭제 
```bash
git pull upsteram master
git branch -d <branch>
```
- 이후 반복작업

## git reset, git revert

> 작업중 이전으로 돌아가고 싶을때 사용

1. git reset
    1. git reset --soft <commmit>
        - 돌아가려는 커밋으로 돌아가는데 이후 커밋된 것들은 staging area로 commit이전으로 되돌린다.
    2. git reset --mixed <commit>
        - 커밋들을 working directory로 add 이전으로 되돌린다.
    3. git reset --hard <commit>
        - 아예 커밋들을 삭제해버린다

    커밋들을 확인하려면 
    ```bash
    git reflog
    ```
2. git revert

    - 커밋을 삭제하는것이 아니라 이전커밋을 새로 덮어 씌운다는 개념

---
