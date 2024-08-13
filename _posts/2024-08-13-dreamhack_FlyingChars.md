---
title : "[Dreamhack] Flying Chars 문제 정답과 풀이"
excerpt : "날아다니는 문자를 멈춰 플래그를 얻어보자"
categories : 보안 Web 
tags : 보안 Webhacking Dreamhack FlyingChars
date : 2024-08-13
last_modifed_at : 2024-08-13
---
## 문제
**날아다니는 글자들을 멈춰서 전체 문자열을 알아내세요! 플래그 형식은 DH{전체 문자열} 입니다.**

**❗첨부파일을 제공하지 않는 문제입니다.**

❗플래그에 포함된 알파벳 중 `x`, `s`, `o`는 모두 소문자입니다.

❗플래그에 포함된 알파벳 중 `C`는 모두 대문자입니다.

## 풀이
우선 첨부파일을 제공하지 않는 문제기 때문에 가상머신을 열어 사이트에 접속하였다. 문자들이 무수히 많이 날아다니고 있었는데, 우선 개발자 도구를 열어서 무엇이 있나 확인해보았다.<br>

<img width="428" alt="스크린샷 2024-08-13 오후 2 56 34" src="https://github.com/user-attachments/assets/7b94a6ba-f0a2-4d25-ae4e-0e84e692d2be"> <br>

이런 식으로 이미지 파일이 여러개가 있었다. 그리고 코드를 보면 img_files 라는 배열에 사진들이 특정 순서로 들어있었는데, 하나하나 비교해보면서 플래그를 확인할 수도 있을 것 같았다. 하지만 비교하면서 이미지 파일을 하나하나 열어보기는 너무 귀찮았기 때문에, 날아다니는 글자들을 멈추기로 결심했다.<br>

<img width="407" alt="스크린샷 2024-08-13 오후 2 57 27" src="https://github.com/user-attachments/assets/c9696cde-cfaa-4b27-a802-567beaa77abd"> <br>

아래에 해당 반복문이 있었는데, 원래는 anim 함수의 명령어의 뒤에 Math.random 어쩌고 하는 인자가 있었다. 랜덤한 속도로 날아다니게 하는 함수인 것 같았는데, 멈추게 하기 위해 과감히 지워버렸다. <br>

<img width="527" alt="스크린샷 2024-08-13 오후 2 58 15" src="https://github.com/user-attachments/assets/da20b3de-de67-491a-8ffd-ff8fd04a1d85"> <br>

글자가 멈추긴 했는데 너무 작아서 10px이던 글자 크기를 50px로 바꾸어주었다.

<img width="237" alt="스크린샷 2024-08-13 오후 2 58 48" src="https://github.com/user-attachments/assets/9f745af2-bc28-4a0b-aaea-9914f6aced1e"> <br>

답을 다 공개할 수는 없어서 초반 값들만 캡쳐해두었다. html과 js문법을 잘 모르는데 생각보다? 쉽게 풀려서 굉장히 뿌듯했다.
