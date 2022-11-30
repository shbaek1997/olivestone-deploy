# \*_Project Upload and Download Olivestone Lab (Deploy)_

## 서비스 소개

- Docker-compose를 활용하여 빌드된 react-app과 express 서버를 nginx 환경에서 배포
- 서비스 설명과 웹사이트 제작에 사용된 기술 정보는 아래의 두 링크를 참조
- 서버 Repository는 이 [링크](http://swrnd.olivestonelab.com:32790/shbaek1997/project-upload-download-server/-/blob/develop/README.md)를 참조
- 클라이언트 Repository는 이 [링크](http://swrnd.olivestonelab.com:32790/shbaek1997/project-upload-download/-/blob/develop/README.md)를 참조

## 기술 스텍

- Docker-compose/ docker : [Docker](https://www.docker.com/)
- nginx : [Nginx](https://www.nginx.com/)

## 개발 환경

- Docker desktop version: 4.14.1
- Docker-compose 내부 Node: 18.12.1 - alpine 3.15
- Docker-compose 내부 Nginx: 1.23.2 - alpine 3.16

## Set Up & 실행 방법

- docker-compose.yml 파일 확인
- 위의 서비스 소개 링크의 client와 server repository가 현재 docker-compose.yml파일이 위치한 폴더 내부에 존재하는지 확인
- 폴더 구조 (아래 같이)
- Project
  - README.md
  - docker-compose.yml
  - nginx
  - backend
    - Dockerfile
  - frontend
    - build ...
- 클라이언트 폴더가 빌드가 잘 되어있는지 확인하고, 서버가 정상 동작하는 상황인지 확인
- 배포에 맞게 클라이언트 폴더의 config안의 변수가 수정되어있나 확인
- nginx 폴더 안의 nginx.conf가 제대로 설정 되어있는지 확인
- docker-compose.yml의 volumes 경로와 build context의 경로가 정확한지 확인
- 터미널을 docker-compose.yml이 있는 디렉토리에서 `docker-compose up -d ` 실행
- http://localhost:80 에 접속하여 사이트가 정상 동작하는지 확인
