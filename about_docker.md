![image](https://user-images.githubusercontent.com/51132077/86273937-ec19d700-bc0b-11ea-9a33-e00a0525e0de.png)
**※명령어 사용법은 3번부터**   

# **1. 도커 개념**   

VMware ,VirtualBox 같은 가상화 플랫폼과 비슷하면서도 아주 다릅니다. VMware, VirtualBox 같은 기존 가상화 방식은 주로 **OS (운영체제, Operating System)** 를 가상화하였습니다.   
![image](https://user-images.githubusercontent.com/51132077/86275290-005ed380-bc0e-11ea-8632-e4e0e0d62761.png)   
기존 가상화 방식은 위 그림처럼 **호스트 OS** 위에 **게스트 OS**를 두어 사용하는 방식입니다. 쉽게 말해서 PC 위에 새로운 PC를 설치하여 사용한다고 생각하시면 됩니다. PC 위에 PC를 두고 사용한다고 생각하니 상상만으로도 무거워보이고 느려보입니다. *실제로도 그렇습니다.*   
(※현재 저희가 우분투라는 OS를 설치한 방법은 호스트 PC 위에 설치한 것이 아니라 기존 호스트 OS와는 독립적으로 설치하여 호스트 OS를 하나 더 만들어서 사용하고 있기에 가상화 방식이 아닙니다.)   
이런 불편함을 극복하기 위해 나온 것이 바로 **도커**입니다. 도커는 **컨테이너 기반의 오픈소스 가상화 플랫폼**입니다. 
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
 docker rmi [이미지 이름
 ```
 
# **4. 메뉴얼**   
## **none image 삭제**   
![Screenshot from 2020-07-01 13-55-10](https://user-images.githubusercontent.com/51132077/86204513-9fe67c80-bba2-11ea-8d96-610b3a573f7f.png)   
```
docker rmi $(docker images -f "dangling=true" -q)
```

