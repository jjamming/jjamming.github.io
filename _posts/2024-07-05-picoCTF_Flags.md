---
title : "[picoCTF] Flags 문제 정답과 풀이"
excerpt : "picoCTF 입문을 해보자"
categories : 보안 picoCTF
tags : 보안 picoCTF Flags
date : 2024-07-05
last_modifed_at : 2024-07-05
---
2주차 해킹 학회에 참석하여 picoCTF 라는 것을 알게 되었다. CTF는 Capture the Flag의 약자로, 컴퓨터 보안 대회이다. Flag를 찾아서 정답을 입력하면 되는 대회이다. picoCTF 사이트에서는 CTF대회에 나왔거나 다른 사용자들이 만들어놓은 문제들을 풀 수 있다. 보안계의 백준? 같은 느낌이다.

## Flag 문제와 풀이
### 문제 : What do the flags mean?<br>
이게 문제의 끝이었다. 처음 푸는 문제기도 하고 달랑 저 문장 하나만 있길래 뭐지? 싶었다. 정답의 형식을 보니 picoCTF{flag}라고 되어있었고 flag값을 찾아내서 입력하면 되는 것 같다. 문제를 잘 살펴보니 flags에 사진 다운 링크가 걸려있었다. 사진을 다운받아 열어보자.

<img width="764" alt="스크린샷 2024-07-05 오후 1 54 48" src="https://github.com/jjamming/jjamming.github.io/assets/162856159/cbb491fa-357a-43b8-85bb-1e7217bc89f1">
<br>

이런 사진 파일이 있었다. 잘 살펴보니 7개의 국기가 있고 {} 가 있다. 정답 형식과 비슷한 것 같다. 아마 picoCTF{**********} 형식인 것 같은데 f와 t는 알겠지만 다른 국기들이 무슨 문자를 의미하는지 몰라서 고민했다.

### 해답
국기 코드, flag code 등을 구글 검색해보던 중 (~~구글링 없이 못살아..~~) 이 코드가 marine signal flags 라는 것을 알아냈다. 선박들끼리 통신을 위해 국기별로 코드를 매칭하고, 각 코드가 어떤 의미인지도 공식 표준이 있었다. 

![image](https://github.com/jjamming/jjamming.github.io/assets/162856159/6734f806-68a9-4065-a673-1643ec4ee5e3)


이런 느낌이다. 이제 문제에서 제공해준 이미지 파일에 있던 국기들에 해당 코드들을 대입해보면 정답이 나온다.

정답을 여기 그대로 작성하면 좀 그러니까 다들 표를 보고 하나하나 대입해보길 바란다!