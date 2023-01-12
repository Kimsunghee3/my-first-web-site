## 웹브라우저에서 요청하면 서버(apache, nodejs)에서 해당 정보를 전달해줌

## nodejs: apache와 동일하게 웹서버로 사용할 수 있음 

## 변수(variable): 변할 수 있는 수
## 상수: 항상 같은 수

## 변수의 기능 데이터에 이름을 붙여줌

## Template literals

## http://opentutorials.org:3000/main?id=HTML&page=12

## http(hyper text transport protocol): protocol
## opentutorials.org: host(domain)
## 3000: port


## http:웹브라우저 웹서버가 서로 데이터를 주고 받기 위해 만든 통신 규칙

## host(domain): 인터넷에 접속되어 있는 각각의 컴퓨터 호스트라고 함

## 3000: 포트번호, 3000포트에 연결되어있는 서버와 통신,  포트번호의 기본 값(default)은 80임

## path: 컴퓨터 안에 있는 어떤 디렉토리의 어떤 파일

## query string
-쿼리스트링 값을 변경하면 앞에 있는 웹서버의 어떤 데이터를 전달할 수 있음
-읽고 싶은 정보는 html이고 12페이지이다.
-쿼리스트링의 시작은 ?이고, 값과 값은 &(앤퍼센트)를 쓰기로 약속되어있고
-값의 이름과 이름은 이퀄로 구분하기로 약속되어있다.

쿼리스트링은 var url = request.url; 이다.

url, fs, http는 모듈이라는 것인데 노드js가 갖고 있는 수많은 기능들을 비슷한 것끼리 그룹핑해둔 것을 모듈이라고한다.

var url = require('url') // url이라는 노드는 url이라는 변수를 통해서 사용할 것이다.

프로그램이라는 것은 입력에 대하여 프로그램이 어떤 정보에 대하여 출력하는 부분 입력하는 부분을 파라미터 또는 argument라고 한다.
파라미터는 입력되는 정보의 형식이며, 그 형식에 대해 입력한 값을 argument라고 한다.

input과 output을 줄여서 io라고 함

url을 통해서 입력 값을 

response.writeHead(200);
console.log(__dirname + url);

`` 그레이브 엑센트, 백틱...?

파일읽기 
var fs = require('fs');
fs.readFile('sample txt', function(err, data){
    console.log(data);
});

localhost:3000 // path 정보가 붙지 않은 상태가 root이다.


Array data type 배열

var url = require('url');   //url이라는 모듈을 사용할 것이라고 nodejs에게 알려준 것

var app = http.createServer(function(request,response){      
var _url = request.url;     //_url은 모듈 url을 가르킴
var queryData = url.parse(_url, true).query;     //querystring에 따라 파일명이 생성


## npm : 패키지 매니저

## pm2 :node js 껏다 켯다 할 필요 없이 도와주는 툴
$ npm install pm2 -g
$ pm2 start main.js[켜고 싶은 파일명]
$ pm2 monit   //현재 pm2에 의해서 실행되고 있는 프로그램들이 보인다.
$ pm2 stop [끄고 싶은 파일명]
$ pm2 list 실행되고 있는 목록 보기
$ pm2 log 에러 메시지 보기
$ pm2 start [파일명] --watch

create: 생성
update: 수정
delete: 삭제
