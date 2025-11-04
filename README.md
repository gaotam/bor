# Bor Overview
Bor is the official Golang implementation of the Polygon PoS blockchain. It is a fork of [geth](https://github.com/ethereum/go-ethereum) and is EVM compatible (upto London fork).

## Hướng dẫn build và đẩy lên docker hub
1. chạy lệnh
```make
make bor-static
```

2. Build docker image
```bash
 docker build -f Dockerfile.release -t bor-node:v2.3.4.0 .
```

3. Đăng nhập vào docker hub (làm đúng 1 lần nếu chưa login)
```bash
 docker login
```

4. Đẩy image lên docker hub
```bash
 docker tag bor-node:v2.3.4.0 [your_dockerhub_username]/bor-node:v2.3.4.0
 docker push [your_dockerhub_username]/bor-node:v2.3.4.0
```

Lưu ý: [your_dockerhub_username] đổi thành tài khoản docker hub của bạn.