# 🚀 Git 협업 최초 설정 가이드
처음 레포를 클론 받고 작업을 시작하기 위한 기본 세팅 절차를 설명합니다.

## 1. Git 사용자 정보 설정 (최초 1회만 필요)
git config --global user.name "이름"
git config --global user.email "GitHub 이메일"

## 2. 레포지토리 클론 받기
git clone git@github.com:Eunhasuiin/LikeLion_Final_team_13.git

## 3. 자신의 작업 브랜치 만들기 (선택)
git checkout -b name/first-branch

## 4. 커밋 & 푸시 기본 명령어
- git add .
- git commit -m "feat: nameX 데이터 전처리 완료"
- git push origin your-branch-name

## 5. GitHub에 올라온 변경사항 반영하기 (푸시 전에 꼭!)
- git pull origin master
거의 그럴 일은 없겠지만 끌어와서 수정사항 바뀐걸 반영한 뒤에 올려주세요


