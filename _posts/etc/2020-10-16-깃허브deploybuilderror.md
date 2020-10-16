---
title: "[jekyll] 깃허브 deploy build error"
date: 2020-10-16 13:00 GMT+0900
categories:
  - jekyll
tags:
  - jekyll
  - Git
---



잊어버려서 사진을 안찍어뒀는데...

로컬에서는 잘 돌아가고 심지어 github.io로 들어가도 잘 돌아가는데 깃헙 저장소에서만 deploy문제가 발생해서 문제가 생겼었다. 그리고 이것저것 찾아보다 문제를 찾았다.  지금 다른 문제(로컬에서는 글이 안보이는데 원격에서는 글이 보이는 문제)가 있어서 그거 해결한다고 push랑 checkout branch를 남발했더니 문제가 발생한듯 싶다..



## issue

원격이랑 로컬이랑 branch의 내용이 달라서 발생하는 문제였다.



## 해결

​```
$ git gc --prune=now
$ git remote prune origin
​```



요로케 하고 안되면 

​```
git fetch
​```

이거 한줄 더해주니까 문제 해결...ㅎ..
```
