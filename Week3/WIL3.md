# 2024.04.07 GDSC 개발입문스터디 정리
## 1. 사전 지식
### {1} git log
#### - commit 기록을 최신 순으로 확인
#### + --online 옵션을 사용하면 각 커밋을 한 줄에 요약
### (1) Commit Id
#### - WIL2에 있음
### (2) HEAD
#### - 현재 작업 중인 위치
#### - 현재 작업 중인 브랜치의 가장 최근 commit
#### - 다음 commit의 base가 되는 commit
#### - 새로운 commit이 생기면 HEAD도 변경됨
### {2} git status - 세 가지 상태에 따라 파일을 분류하여 확인
### 2. commit 되돌리기
### {1} commit --amend
#### - 마지막 commit의 내용에 변경이 있을 때 사용
#### - 완전히 새로운 commit으로 대체되므로 commit Id가 바뀜
#### - vim으로 진입하여 commit 메세지를 수정하게 됨
#### - git commit --amend -m "커밋 메세지" : vim 진입 없이 commit 메세지 수정
#### - git commit --amend --no edit : commit 메세지 수정 없이 commit 수정
#### !주의! 다른 사람이 작업 기반으로 삼공 있는 commit은 amend 금지!!
### {2} reset - commit 제거에 사용
### + commit을 공유하는 다른 브랜치에도 영향을 줄 수 있음
### + 돌아갈 commit의 id를 사용 : git reset '--option' "<commit id>"
#### (1) reset --soft
#### - 커밋만 취소
#### - 변경 사항이 Staging Area로 돌아감
#### (2) reset --mixed
#### - 커밋을 취소
#### - 변경 사항을 working directory
#### (3) reset --hard
#### - 커밋을 취소
#### - 변경 사항을 모두 제거하고 이전 커밋으로 돌아감
### {3} revert
### - commit을 제거하지 않고 되돌림
### - 되돌리기 위한 새로운 commit 생성
### - --edit 옵션이 default
#### (1) revert --no-edit
#### - 편집기 진입 없이 바로 revert 가능 : git revert --no-edit "<commit id>"
#### (2) revert --no-commit
#### - 직접 commit하지 않고 revert 내용을 Staging Area에 올림