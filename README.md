# git_practive
깃 연습 리파지토리입니다.
아래 문서에서 `[]` 는 선택 사항을, `<>` 는 사용자 임의의 값을 의미합니다. 선택 항에서도 모든 경우의 수를 다루지는 않으니 필요한 경우 도움말을 이용하세요.

## 00. 깃 리파지토리 초기화
이번에는 깃 리파지토리를 생성하고 사용자 정보를 등록합니다.
그리고 최초 커밋/푸시를 합니다.

### CLI 명령어 기본
cli 에서 잘 모르겠을 때는 `--help` 옵션을 사용하세요.
```
$> git config --help
```
`config` 대신에 사용할 명령어를 넣으면 됩니다.

### 로컬에 디렉토리 생성하기
github/gitlab/bitbucket 등의 서비스에 원격 저장소를 생성했다고 가정하고 로컬에 작업 환경을 구축해 봅니다.
```
$> git init
$> git remote add origin <your_repository>
```
- init: 현재 디렉토리를 git 이 관리하는 root 디렉토리로 등록합니다. `.git` 디렉토리가 생성됩니다.
- remote: 리모트 명령으로 원격 저장소를 관리합니다
	- `git remote [add | remove] <remote_repository_alias> <remote_repository_url>`
	- `git remote -v`	

### 사용자 정보 등록하기
사용자 정보를 등록해두면 정보에 반영됩니다.
```
$> git config [--local | --global] [user.name | user.email] <your_value>
```

### 커밋과 푸시
커밋은 사용자가 변경한 내역을 `스테이지` 로 올리는 행위를 말합니다. 푸시는 스테이지에 등록된 정보를 바탕으로 변경점을 원격 저장소에 등록하는 행위입니다.
```
$> git add README.md
$> git commit -m 'Edit README.md'
$> git push <remote_repository> <remote_branch>
```
