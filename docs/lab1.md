## Lab 1 - Check Local IP

`ipconfig` 을 command에 치면 내 ipv4가 나온다.

- 누가 이 IP를 내 PC에 할당했을까?
- 왜 이 주소를 인터넷에서 직접 사용하지 않을까?

---

`ping 127.0.0.1`

`ping localhost`

- 인터넷 연결을 끊어도 127.0.0.1에 ping이 될까?
- 가정: 자기 자신, localhost 이기 때문에 인터넷 연결과는 상관이 없다.
- 결과:

---

`python -m http.server 8000` 후 localhost 8000으로 접속하면
프로젝트의 디렉토리 구조 리스트가 나옴.

다른 터미널에서
`netstat -ano | findstr :8000` 을 하면 8000번 port를 사용하는 프로세스를 관찰할 수 있음.

브라우저 -> (http) -> 127.0.0.1:8000 -> python HTTP Server

인터넷 -> EC2:80 -> nginx

이것이 본질적으로 같은 개념?

---

`curl http://localhost:8000`
`curl -v http://localhost:8000`
이렇게 하면 우리가 봤던 웹사이트의 코드가 출력이 된다.
