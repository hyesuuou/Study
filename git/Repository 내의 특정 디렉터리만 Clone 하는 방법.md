2020.12.25

(내가 사용한 방법) ref - [https://velog.io/@byjihye/git-clone](https://velog.io/@byjihye/git-clone)

### 1. 다운로드 받을 디렉터리에서 터미널을 실행해 git을 초기화해준다.

```
$ git init
```

### 2. git 저장소를 원격 저장소와 연결한다.

```
$ git remote add 원격저장소별칭(origin) 원격저장소URL
```

원격 저장소 별칭은 서버 주소가 길기 때문에 쉽게 작업하려고 사용하는 별명이며, 중복해서 사용할 수 없다. 

원격 저장소가 연결되면 $ git remote -v 를 통해 원격 저장소 목록(별칭+URL) 을 확인할 수 있고 push(서버로 전송하는 동작)와 fetch(서버에서 가지고 오는 동작)의 두 주소를 출력한다.

### 3. git sparseCheckout 활성화

```
$ git config core.sparseCheckout true
```

제대로 되었는지는 ./git/config 문서에서 확인할 수 있다.

### 4. clone 하기 위한 폴더 경로 설정

```
$ echo 폴더경로 >> .git/info/sparse-Checkout
```

폴더 경로를 작성할 때 " " (큰 따옴표) 를 작성하면 작동하지 않는다. 어떤 Repository 안에 있는 A 라는 폴더 내용을 다운 받고 싶으면 A/* 형식으로 작성한다.

### 5. pull 명령어로 해당 폴더 다운받기

```
$ git pull origin main(master)
```
