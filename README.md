# 1) Fork
# 2) 로컬 클론 + upstream 연결
git clone https://github.com/<student>/<REPO>.git
cd <REPO>
git remote add upstream https://github.com/<YOUR_ORG_OR_ID>/<REPO>.git
git fetch upstream

# 3) 본인 학번 브랜치로 체크아웃
git checkout -b students/<학번> upstream/students/<학번>

# 4) 본인 폴더만 수정
#    submissions/<학번>/solution.py
git add submissions/<학번>/*
git commit -m "Solve: <설명>"
git push origin HEAD

# 5) GitHub에서 PR 생성
#    base: upstream/main  ←  compare: origin/students/<학번>
