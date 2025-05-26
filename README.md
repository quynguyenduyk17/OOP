# OOP
# Marketplace Transactional System

## 🛒 Giới thiệu

Đây là hệ thống **quản lý giao dịch Marketplace** được xây dựng bằng **Java Swing** và **MySQL**, giúp người dùng quản lý sản phẩm, đơn hàng, người dùng và phân tích doanh thu, hỗ trợ nhiều vai trò như **Admin**, **Seller** và **Customer**.

Hệ thống áp dụng **Lập trình hướng đối tượng (OOP)**, tuân theo mô hình nhiều lớp (`model`, `dao`, `ui`), hỗ trợ giao diện thân thiện và biểu đồ thống kê trực quan bằng **JFreeChart**.

---

## 📌 Tính năng chính

### 1. Đăng nhập & Đăng ký
- Giao diện đăng nhập theo vai trò: Admin, Seller, Customer.
- Đăng ký tài khoản (Customer).
- Phân quyền hiển thị giao diện tương ứng sau khi đăng nhập.

### 2. Admin Dashboard
- Quản lý toàn bộ người dùng, sản phẩm và đơn hàng.
- Xem biểu đồ thống kê: doanh thu, số đơn hàng theo tháng, sản phẩm bán chạy...
- Sử dụng **JFreeChart** để trực quan hóa dữ liệu từ cơ sở dữ liệu.

### 3. Seller Dashboard
- Quản lý sản phẩm của riêng người bán.
- Xem đơn hàng liên quan đến sản phẩm mình cung cấp.

### 4. Customer Dashboard
- Duyệt, tìm kiếm, lọc sản phẩm.
- Thêm sản phẩm vào giỏ hàng.
- Đặt hàng và thanh toán.
- Theo dõi lịch sử đơn hàng.

---

## 🧱 Cấu trúc dự án
do_an/
│
├── model/ # Các lớp mô hình (Product, User, Order, etc.)
├── dao/ # Data Access Object (xử lý kết nối và truy vấn CSDL)
├── ui/ # Giao diện người dùng với Swing
│ ├── login/ # Giao diện đăng nhập, đăng ký
│ ├── dashboard/ # Giao diện AdminDashboard, CustomerDashboard...
│ └── components/ # Các thành phần tái sử dụng
├── utils/ # Tiện ích chung: DBConnection, Validation, ChartHelper
└── Main.java # Điểm khởi chạy ứng dụng

---

## 🧪 Cơ sở dữ liệu

**Tên CSDL**: `marketplace`

### Các bảng chính:

- `users` – chứa thông tin đăng nhập và vai trò
- `customers` – thông tin người mua
- `sellers` – thông tin người bán
- `products` – danh sách sản phẩm
- `orders` – đơn hàng
- `order_items` – chi tiết đơn hàng

> Kết nối qua **SQLyog** hoặc bất kỳ MySQL client nào.

---

## 📊 Công nghệ sử dụng

- **Java Swing** – Xây dựng giao diện desktop
- **MySQL** – Quản lý dữ liệu
- **JDBC** – Kết nối Java và MySQL
- **JFreeChart** – Vẽ biểu đồ thống kê
- **Mô hình MVC / OOP** – Cấu trúc mã rõ ràng

---

## ⚙️ Cách chạy dự án
Tạo database MySQL
Import file marketplaceTransactional.sql
Tạo các bảng users, products, orders, ...
Cấu hình kết nối trong DBConnection.java
private static final String URL = "jdbc:mysql://localhost:3306/marketplace";
private static final String USER = "root";
private static final String PASSWORD = "123456";
Chạy file Trang_chu.java để khởi động hệ thống
📌 Yêu cầu hệ thống
JDK 8 trở lên
MySQL 5.7+
IDE khuyến nghị: Eclipse / IntelliJ IDEA
🎓 Đồ án môn học
Môn học: Lập trình Hướng Đối Tượng với Java
Dạng bài: Dự án nhóm 
Chủ đề: Marketplace Transactional 
📁 Tác giả & đóng góp
Nhóm thực hiện: [Nguyễn Duy Quý]

📝 Giấy phép
Dự án được phát triển cho mục đích học tập. Mọi hành vi sử dụng cho mục đích thương mại cần được sự cho phép của tác giả.
