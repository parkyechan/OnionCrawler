# Onion Crawler

## Preliminary Knowledge

### 왜 필요한가? 
넷플릭스 드라마 수리남을 보고 마약거래는 어떻게 어디서 이뤄지나 찾아보다가 Deep Web을 통해서 Contact하는 것을 확인하였다. 여러 범죄의 온상인 Deep Web의 범죄 공모등을 조기식별을 위해 모니터링할 수 있는 기술을 습득하기 위함이다.<br>
본 내용에서는 기초적인 Onion-Domain Crwaling을 진행한다.

### Install Scrapy
Scrapy는 Python으로 작성된 오픈소스 웹 크롤링 프로그램이며 해당 내용에서 사용한다. <br><br>
```# scrapy startporject sample_project```<br><br>

```# scrapy genspider spider_example example.com```

### Install PPROXY

Dark Web 혹은 Deep Web에 접근하기 위해서 사용하는 프로토콜은 Socks5이다.<br>
우리가 사용할 크롤링 편집기인 Scrapy는 Socks5를 지원하지 않으므로 http proxy로 변환해서 사용해야 한다.<br>
이를 시행하기 위해 사용해야 하는 프로그램은 pproxy이다.<br><br>
```# pip3 install pproxy```<br><br>
```# pproxy - l http://:8080 -r sock5://127.0.0.1:9050 -vv```<br><br>
백그라운드에서 작동하고 있어야 Socks5 통신을 통해서 .onion 도메인에 접근이 가능하다.<br>

  
