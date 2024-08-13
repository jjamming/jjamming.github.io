---
title : "[Dreamhack] Devtools-sources 문제 정답과 풀이"
excerpt : "개발자 도구를 활용해보자"
categories : 보안 Web 
tags : 보안 Webhacking Dreamhack Devtools
date : 2024-08-13
last_modifed_at : 2024-08-13
---
## 문제<br>
개발자 도구의 Sources 탭 기능을 활용해 플래그를 찾아보세요.

플래그 형식은 DH{...} 입니다.

## 풀이<br>
우선 첨부파일을 다운받으니 여러가지 html파일과 js파일들이 있었다.
<br>들어가서 개발자 도구를 실행시켜보았다.<br>

<img width="529" alt="스크린샷 2024-08-13 오후 2 27 04" src="https://github.com/user-attachments/assets/81569607-d7f1-4e0b-8abb-dfb32d28f66f">

소스 창에 들어가면 이런식으로 좌측에 해당 폴더에 있는 모든 파일들이 트리형식으로 정리되어있고 우측에는 소스 코드들을 볼 수 있다. 

플래그를 찾기 위해 cmd + F 키를 이용하여 플래그의 시작 부분인 DH{ 를 검색해보았다.

처음 했을 때는 나오지 않아서 이거 폴더에 있는 모든 파일들에 들어가서 검색을 하나하나 해보아야하나 고민이었다. 하지만 전체 폴더에서 검색하는 단축키가 있었다.

cmd + opt + F 를 통해 전체 폴더에서 검색을 할 수 있었다. 다시 DH{ 를 검색해보면<br>

<img width="491" alt="스크린샷 2024-08-13 오후 2 28 05" src="https://github.com/user-attachments/assets/6b8b09c6-b1cc-4452-b945-9398181488d6">

이런식으로 main.scss 파일에 주석처리된 플래그를 찾을 수 있었다.