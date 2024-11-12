1. git clone --recursive https://github.com/MunSeongyun/coding_supporter.git
2. cd coding_supporter
3. docker compose run --rm --no-deps nest /bin/bash
4. nest 컨테이너 안에서
   a. apt install libnss3-tools
   b. wget -O mkcert https://github.com/FiloSottile/mkcert/releases/download/v1.4.3/mkcert-v1.4.3-linux-amd64
   c. chmod +x mkcert
   d. cp mkcert /usr/local/bin/
   e. mkcert -install
   f. mkcert -key-file key.pem -cert-file cert.pem localhost 127.0.0.1 ::1
5. docker compose run --rm --no-deps react /bin/bash
6. react 컨테이너 안에서
   a. apt install libnss3-tools
   b. wget -O mkcert https://github.com/FiloSottile/mkcert/releases/download/v1.4.3/mkcert-v1.4.3-linux-amd64
   c. chmod +x mkcert
   d. cp mkcert /usr/local/bin/
   e. mkcert -install
   f. mkcert -key-file key.pem -cert-file cert.pem localhost 127.0.0.1 ::1
7. nest, react 폴더안의 .env.example를 복사해서 .env로 이름 변경후 환경변수 값 입력
8. docker compose up -d
