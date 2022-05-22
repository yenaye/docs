1. GitHub SSH Token 생성
```
1) 우측 상단 프로필 [클릭]
2) Settings [클릭]
3) Developer settings [클릭]
4) Personal access tokens [클릭]
5) Generate new token [클릭]
6) Note [입력]
   repo, admin:org, admin:repo_hook [체크]
7) Generate token [클릭]
8) token [복사]
```

2. Jenkins Credentials 생성
```
1) (메인화면 좌측 메뉴) Jenkins 관리 [클릭]
2) 시스템 설정 [클릭]
3) GitHub >  Credentials > Add > Jenkins [클릭]
4) Domain: Global credentials (unrestricred) [선택]
   Kind: Username with password [선택]
5) Add [클릭]
```
or
```
1) 프로젝트 [클릭]
2) 구성 [클릭]
3) 소스 코드 관리 > Git > Credentials > Add > Jenkins [클릭]
4) Domain: Global credentials (unrestricred) [선택]
   Kind: Username with password [선택]
5) Add [클릭]
```

3. Jenkins Credentials 설정
```
1) (메인화면 좌측 메뉴) Credentials [클릭]
2) 추가된 Credentials Name [클릭]
3) Update [클릭]
4) Username: GitHub ID [입력]
   Password: GitHub ssh token [입력]
   Description: GitHub Name [입력]
5) Save [클릭]
```

4. Jenkins Credentials 적용
```
1) 프로젝트 [클릭]
2) 구성 [클릭]
3) 소스 코드 관리 > Git > Credentials > 생성/설정한 Credentials [선택]
4) 저장 [클릭]
```


참고 사이트: https://goddaehee.tistory.com/258
