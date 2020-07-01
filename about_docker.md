
# **1. 도커 개념**   
# **2. 도커 사용법**   
# **3. 도커 명령어**   
## **도커 이미지 가져오기**   
```
 docker pull [이미지 이름]:[태그]
 ```
## **컨테이너 생성**   
```
 docker create [옵션] [이미지 이름]:[태그]
 ```
 ## **컨테이너 실행**   
```
docker start centos:7
 ```
 ## **컨테이너 목록**   
 ```
 docker ps
 ```
 ## **컨테이너 삭제**   
 ```
 docker rm [컨테이너 이름]
 ```
 ## **이미지 삭제**
 ```
 docker rmi [이미지 이름[
 ```
 
# **4. 메뉴얼**   
## **none image 삭제**   
![Screenshot from 2020-07-01 13-55-10](https://user-images.githubusercontent.com/51132077/86204513-9fe67c80-bba2-11ea-8d96-610b3a573f7f.png)   
```
docker rmi $(docker images -f "dangling=true" -q)
```

