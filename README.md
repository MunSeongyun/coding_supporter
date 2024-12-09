1. git clone --recursive https://github.com/MunSeongyun/coding_supporter.git
2. cd coding_supporter
3. docker compose run --rm --no-deps nest /bin/bash
4. nest 컨테이너 안에서
   <br/>
   a. apt install libnss3-tools<br/>
   b. wget -O mkcert https://github.com/FiloSottile/mkcert/releases/download/v1.4.3/mkcert-v1.4.3-linux-amd64<br/>
   c. chmod +x mkcert<br/>
   d. cp mkcert /usr/local/bin/<br/>
   e. mkcert -install<br/>
   f. mkcert -key-file key.pem -cert-file cert.pem localhost 127.0.0.1 ::1<br/>
   g. exit<br/>
6. docker compose run --rm --no-deps react /bin/bash
7. react 컨테이너 안에서<br/>
   a. apt install libnss3-tools<br/>
   b. wget -O mkcert https://github.com/FiloSottile/mkcert/releases/download/v1.4.3/mkcert-v1.4.3-linux-amd64<br/>
   c. chmod +x mkcert<br/>
   d. cp mkcert /usr/local/bin/<br/>
   e. mkcert -install<br/>
   f. mkcert -key-file key.pem -cert-file cert.pem localhost 127.0.0.1 ::1<br/>
   g. exit<br/>
8. nest, react 폴더안의 .env.example를 복사해서 .env로 이름 변경후 환경변수 값 입력
9. docker compose up -d
10. docker compose exec nest /bin/bash
11. npm run typeorm migration:run -- -d ./src/ormconfig.ts
12. exit
