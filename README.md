# Upload files to jsdelivr CDN ( github )

### Reference
  - [www.jsdelivr.com](https://www.jsdelivr.com/)
  - https://okky.kr/article/438705
  - https://github.com/jsdelivr/jsdelivr#github
  - https://github.com/jsdelivr/jsdelivr
  - https://github.com/softm/jsdelivr
  - https://www.cdnperf.com/
  - https://codemcd.github.io/toy/jsdsLib-jsdsLib-jsDeliver/

  - https://cdn.jsdelivr.net/gh/softm/jsdelivr@v0.0.2/loaderjs/bar.js
  - https://www.jsdelivr.com/features
  - https://help.github.com/en/articles/changing-a-remotes-url
  - https://www.whatwant.com/377

### Flow
  1. Fock jsdelivr : https://github.com/jsdelivr/jsdelivr
  2. 파일추가 ( git add 파일명 )
  3. 버전 tag 작성
     > tag를 통해 버전관리함 ( git tag를 이용 version : semver v0.0.1 )
  4. pull request : jsdelivr
  5. cdn에 접근
     > https://cdn.jsdelivr.net/gh/[gitusername]/jsdelivr@v0.0.1/파일명

### Do ( using shell )
  1. fock jsdelivr : https://github.com/jsdelivr/jsdelivr
  2. make directory - cmd
     cd c:\
     mkdir jsdelivr_fock
     cd jsdelivr_fock
  3. git int
  4. git config
     git config user.email "myeamil@my.com"
     git config user.name "username"

  5. view git config
     git config user.email
     git config user.name

  6. write file ( ex : loader.js )

  7. git add loader.js

  8. git commit -m "init"

  9. git log --pretty=oneline
     - commit hash 확인
    15193151618121c91111f9122c2c6c0fc867f82f (HEAD -> master, tag: v0.0.1, origin/master) init

  10. git tag v0.0.1 15193151618121c91111f9122c2c6c0fc867f82f

  11. push
      - git push origin master
      - git push origin master --tags
      - if it doesn't work : git pull origin branchname --allow-unrelated-histories

  12. 다음 명령들 각각 실행해서 로컬 저장소와 깃허브에 적용하고, 깃허브에 접속해서 버전 태그가 달렸는지 체크

  13. cdn :
      https://cdn.jsdelivr.net/gh/softm/jsdelivr@v0.0.1/loader.js
     > format : https://cdn.jsdelivr.net/gh/user/repo@version/file
