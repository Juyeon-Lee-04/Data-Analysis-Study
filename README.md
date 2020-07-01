## Machine Learning with Python A Practical Introduction
This is my repository where I will upload my practice codes during taking edx course 'Machine Learning with Python: A Practical Introduction(IBM-ML0101EN)'. 
This course provides code lab for practicing and reviewing in each module, so after studying each module, I will upload my own application with different dataset.  
I might use data from Kaggle or Korean public big data portal. I will write the data source on the top of each code file.

course info: https://courses.edx.org/courses/course-v1:IBM+ML0101EN+1T2020/course/



## Git 두개의 로컬저장소 하나의 원격저장소와 연동하기 
(출처 https://wayhome25.github.io/git/2017/04/09/git-06-remote-repository/)

원격 저장소 만들기
원격 저장소의 별명을 설정할 수 있다. (저장소 주소가 길기 때문에)
여러개의 원격 저장소를 로컬저장소로 저장할 수 있다.
remote 저장소 설정
### 원격 저장소의 이름(별명)을 각각 origin , memo 지정한다.
❯ git remote add origin https://github.com/wayhome25/gitfth.git
❯ git remote add memo https://github.com/wayhome25/memo.git
❯ git remote
memo
origin

-----

원격 저장소를 지역 저장소로 복제
여기서는 github.com이라는 서비스를 소개하고, 이 서비스를 이용해서 이미 존재하고 있는 오픈소스의 원격저장소의 내용을 내 컴퓨터의 지역저장소로 가져오는 방법에 대해서 알아봅니다. 이 과정에서 git의 소스코드와 이 소스코드의 첫번째 커밋의 내용도 알아봅니다.

git의 소스코드를 지역저장소로 가져오기
git clone https://github.com/git/git.git 폴더이름
로그를 거꾸로 출력하기
git log --reverse
git의 첫번째 커밋으로 체크아웃하기
git checkout e83c5163316f89bfbde7d9ab23ca2e25604af290

-----

### 로컬저장소를 origin 원격저장소의 master 브랜치로 연결하여 push한다.
### 처음에 한번만 -u 설정을 하면 앞으로 git push 만 입력해도 origin의 master 브랜치로 push한다.
❯ git push -u origin master
remote 저장소 변경
현재 원격 저장소 상태 확인
❯ git remote -v
### 변경하고자 하는 원격저장소 설정
❯ git remote set-url origin https://github.com/wayhome25/fastcampus_school
이미 존재하는 원격 저장소를 새로운 로컬 저장소에 연결할 수 있다.
별도의 remote 설정없이 clone을 통해서 원격 저장소와 연결된다.
❯ git clone https://github.com/wayhome25/gitfth.git .
❯ git remote -v
origin	https://github.com/wayhome25/gitfth.git (fetch)
origin	https://github.com/wayhome25/gitfth.git (push)

------

### 집에서 (git_home/ 폴더)
git add f1.txt
git commit f1.txt
git push

### 회사에서 (git_office/ 폴더)
git pull
git add f1.txt
git commit f1.txt
git push
