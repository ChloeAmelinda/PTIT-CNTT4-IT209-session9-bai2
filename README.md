\# Bài 2: Khởi chạy Web Server Nginx với Port Mapping



\## 1. Mục tiêu

Khởi chạy Nginx bằng Docker, ánh xạ cổng 8080:80, kiểm tra Web Server và dọn dẹp container.



\## 2. Các bước thực hiện



\### Bước 1: Khởi chạy Nginx

```bash

docker run -d -p 8080:80 --name my-web nginx:alpine

```



Docker sử dụng image `nginx:alpine` và tạo container tên `my-web`.



\### Bước 2: Kiểm tra container

```bash

docker ps

```



Kết quả:

\- IMAGE: nginx:alpine

\- STATUS: Up

\- PORTS: 0.0.0.0:8080->80/tcp

\- NAMES: my-web



\### Bước 3: Kiểm tra Web Server

```bash

curl.exe http://localhost:8080

```



Kết quả trả về:

```html

<h1>Welcome to nginx!</h1>

```



Nginx hoạt động thành công.



\### Bước 4: Dừng và xóa container

```bash

docker stop my-web

docker rm my-web

```



\### Bước 5: Kiểm tra sau khi dọn dẹp

```bash

docker ps -a

```



Kết quả: Không còn container `my-web` trong danh sách.



\## 3. Kết luận



Đã hoàn thành các yêu cầu:

\- Chạy Nginx bằng Docker ở chế độ ngầm.

\- Ánh xạ cổng 8080:80 thành công.

\- Truy cập localhost:8080 và nhận HTML mặc định của Nginx.

\- Dừng và xóa container sau khi kiểm tra.

