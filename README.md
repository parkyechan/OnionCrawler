# Onion Crawler 만들기

## 사전지식
Dark Web 혹은 Deep Web에 접근하기 위해서 사용하는 프로토콜은 Sock5이다.<br>
우리가 사용할 크롤링 편집기인 Scrapy는 Sock5를 지원하지 않으므로 http proxy로 변환해서 사용해야 한다.<br>
이를 시행하기 위해 사용해야 하는 프로그램은 pproxy이다.<br>
<br>
pip3 install pproxy<br>
pproxy - l http://:8080 -r sock5://127.0.0.1:9050 -vv<br>
