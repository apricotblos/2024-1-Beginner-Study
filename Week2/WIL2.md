# 2024.03.26 GDSC 개발 입문 스터디 정리
## 1. Fork/Star
### - Fork : 다른 사용자의 Repository를 자신의 계정으로 복사하여 독립적으로 수행하고 관리
#### + (1) 기여 및 수정 : Fork를 하면 자신의 계정에 해당 프로그램의 복제본이 생성됨. 이를 통해 원본 프로젝트와는 분리된 환경에서 자유롭게 수정하고 개선할 수 있음.
#### + (2) 변경 사항 제안 : Fork한 프로젝트에서 변경 사항을 가지고 자신의 계정으로 변경을 가할 수 있음. 이 변경 사항을 원본 프로젝트에 제안할 수 있으며, 이는 Pull Request를 통해 이루어짐.
#### + (3) 자신만의 버전 관리 : 자신만의 버전으로 관리 할 수 있음. 이를 통해 원본 프로젝트와는 독립적으로 발전시킬 수 있음.
#### + (4) 시험 및 실험 : Fork를 통해 다른 사람의 프로젝트를 자신만의 버전으로 관리할 수 있음. 이는 원본 프로젝트에 영향을 주지 않고 자유롭게 실험할 수 있는 환경을 제공함.
### + (5) 개인 작업 영역 : Fork한 프로젝트를 자신의 작업 공간으로 활용할 수 있음. 자신의 작업이나 실험 등을 원본 프로젝트와 분리하여 관리할 수 있음.
### - Star : 관심 있는 Repository나 프로세서에 star를 달아 북마크와 같이 관리
## 2. Issue
### - Repository에서 작업 계획, 토론 및 추적을 위해 활용
## 3. Branch
### - 기존 브랜치에서 분기되어 생성되는 별도의 작업 공간
### - fork와 달리 같은 Repository에 생성됨
### * Branch Naming Convention
#### - type/<issue 번호>-<간략한 설명>
## 4. Pull Request
### - 분기된 Branch를 다시 병합하기 위한 절차
### - 새로운 변경을 제안하거나 병합 시 발생하는 충돌을 해결
### - Merge에 앞서 코드 리뷰
## 5. Merge
### - 세 가지 옵션 Create a merge commit, Squash and merge, Rebase and merge
### (1) Merge commit 
#### + 두 브랜치를 공통 분모로 하는 새로운 commit "E"를 만듦
#### + A, B, C의 커밋이 그대로 main 브랜치로 병합
### (2) Squash and Merge
#### + A, B, C의 커밋을 'squash'
#### => 하나의 커밋으로 main 브랜치로 병합
### (3) Rebase and Merge
#### + A, B, C 커밋의 base를 재설정
#### + 모두 새로운 커밋으로 변경
#### + commit hash*가 변경됨
#### + 무수한 충돌을 경험할 수 있으니 사용에 주의
##### * commit hash : Commit Id는 commit의 식별을 위해 사용하는 40자 길이의 16진수임. 중복 확률을 2의 80제곱 분의 1이며 SHA-1 해시 합수를 사용
##### + git은 분산 버전 관리 시스템이기 때문에 어떤 상황에도 commit을 할 수 있어야 함. hash를 사용하면 온/오프라인 어떤 환경에서도 commit이 가능하므로 Commit Id를 hash로 사용함.

https://github.com/apricotblos/2024-1-Beginner-Study/pull/6