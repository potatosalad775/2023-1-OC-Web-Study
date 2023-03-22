# WIL2 - 2023-03-22

## Behind Web

### Resource

우리가 웹사이트에 접속하고자 할 때, 서버로부터 제공받는 자원을 리소스라고 한다.

여기에는 텍스트와 이미지를 비롯해서 html, css와 같은 다양한 파일들이 포함될 수 있다.

### DNS

DNS, Domain Name Server는 사람이 읽기 쉬운 '도메인' 이름을 기계가 읽기 쉬운 'IP 주소'로 변환해주는 서버이다.

### URL

원하는 리소스에 접근하기 위해 사용하는 것이 URL이다.

## git

git은 효율적인 코드 형상 관리를 위한 도구로, 크게 3가지 영역을 기반으로 동작한다.

* Working Directory : 작업 중인 프로젝트 공간
* Staging Area : 커밋될 파일에 대한 정보를 저장하는 공간
* Repository : 프로젝트 데이터가 저장되는 공간

공간 이외에도, Git은 파일을 4가지 상태로 분류하여 관리한다.

* Untracked : Working Directory에 있으나, Git으로 버전관리를 하고 있지 않는 파일
* Unmodified : 마지막 커밋 이후 새롭게 추가되거나 수정된 파일
* Modified : 수정 사항이 있는 파일
* Staged : Staging Area에 올라간 파일

### add

`git add`는 특정 파일이나 디렉터리를 Staging Area에 추가하는 명령어다.

`git add`의 arugment로 전달된 파일이나 디렉터리는 Staged 상태로 전환되어 Git이 추적하고 관리하게 된다.

추가로, Git이 이미 추적하고 있는 Modified 상태의 파일을 Staged 상태로 만들 때에도 `git add` 명령어를 사용한다.

### commit

수정된 파일들이 commit 되기 전, Staging Area에 정리된다.

Git은 Staging Area에 속한 스냅샷을 로컬 Repository에 기록한다. 이 때 `git commit` 명령어를 사용한다.

commit 이후, Staged 상태에 있던 파일들의 상태는 Unmodified로 변경된다.

### push

로컬 Repository에 기록된 스냅샷을 원격 Repository에 업로드하고 싶을 때 `git push` 명령어를 사용한다.

### fetch vs pull

`git fetch` 명령어는 원격 저장소로부터 프로젝트의 최신 정보를 확인하는 명령어이다. 이 때, 변경된 데이터를 로컬 Repository로 가져오지는 않는다.

`git pull` 명령어는 원격 저장소로부터 변경 사항을 확인할 뿐만 아니라, 최신 데이터를 복사해서 로컬 저장소로 가져와 합치는 기능을 한다.

이 때 변경된 내용들이 병합되면서 로컬에서 작업 중이던 내용들이 덮어씌워지는 일이 발생할 수 있다.