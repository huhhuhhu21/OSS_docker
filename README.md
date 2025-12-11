# Laptop Project (Laravel + React + Docker)

## Yêu cầu
- Đã cài đặt Docker và Docker Desktop.

## Hướng dẫn cài đặt cho Dev (Developer)

### 1. Clone dự án
git clone <link-repo-github-của-bạn>
cd project-laptop

### 2. Khởi chạy Docker
Chạy lệnh sau để dựng toàn bộ môi trường:
docker-compose up -d

### 3. Setup Backend (Laravel)
Truy cập vào container PHP để cài đặt thư viện:
docker-compose exec app composer install
docker-compose exec app cp .env.example .env
docker-compose exec app php artisan key:generate
docker-compose exec app php artisan migrate

### 4. Setup Frontend (React)
Cài đặt thư viện node modules:
docker-compose exec frontend npm install

### 5. Truy cập
- Backend API: http://localhost:8000
- Frontend React: http://localhost:3000 (hoặc 5173 tùy config)
- Database: localhost:3306 (User: user / Pass: userpassword)