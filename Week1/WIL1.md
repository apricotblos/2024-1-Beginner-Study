# 2024.03.19 GDSC 스터디 정리
## 1. GIT HUB를 쓰는 이유
    ### - 파일을 관리하기 위해
    ### - 파일의 수정 로그를 알기 위해

## 2. 파일의 생명주기
    ### - untracked
    ### - tracked = unmodified, modified, staged

## 3. GIT의 영역
    ### (1) Local
        #### - Working Directory
        #### - Staging Area
        #### - Local Repo
    ### (2) Remote
        #### - Remote Repo

## 4. GIT 관련 명령어
    ### + git init = 디렉토리에 Git 저장소 생성, 숨겨진 파일 .git 생성
    ### + rm -r .git = git으로 관리 그만하기
    ### + git add = Git으로 관리할 대상 등록
    #### + git add . = 모든 파일 한 번에, git add <파일명> = 하나씩, git rm --cacjed <file> = unstaged로 되돌리기
    ### + git commit = 파일 수정 후 로컬 저장소로 옮기기
    ### + git config --global user.name "<깃허브 이름>", git config --global user.email "<깃허브이메일>" =  깃허브와 연동
    ### - git commit -m "<commit message">
        ### * type
            ### + feat : 새로운 기능 추가
            ### + refactor : 기존 코드 개선
            ### + fix : 버그 수정 
            ### + chore : 코드 외의 설정 바꿈
            ### + docs : 문서화
            ### + test : 테스트 코드
    ### - GitHub에 파일 올리기
        ### * 올리기 전에
            ### + git remote add origin <주소>
            ### + git branch -M main
            ### + git push -u origin main
        ### * 올리기
            ### + git add <파일명>
            ### + git commit -m "commit message"
            ### + git push origin main
