# F4 Delivery - Backend

Dự án backend cho nền tảng vận chuyển **người** và **hàng hóa**, lấy cảm hứng từ Grab.  
Phát triển bởi nhóm 4 người, sử dụng **Java Spring Boot**, triển khai các chức năng như:

- Đăng ký / xác thực tài xế và người dùng
- Quản lý đặt chuyến, phương tiện, CCCD, giấy phép lái xe
- Hệ thống ví điện tử, giao dịch nạp/rút tiền
- Upload ảnh (Cloudinary), định vị tài xế thời gian thực
- Phân quyền admin, xử lý trạng thái tài xế/người dùng

> 📌 Repo này chỉ chứa phần **backend**, cung cấp RESTful API cho mobile/frontend.

---

## 🔗 API Tiêu biểu

| Nhóm chức năng | Endpoint | Mô tả |
|----------------|----------|-------|
| Auth | `POST /auth/driver` | Đăng ký tài xế |
| Auth | `POST /auth/introspect` | Xác thực token |
| Admin | `PUT /admin/block/{driverId}/{isBlocked}` | Khóa / mở tài xế |
| Admin | `GET /admin/drivers` | Lấy danh sách tài xế |
| Booking | `POST /booking/create` | Tạo đơn chuyến |
| Booking | `POST /booking/complete` | Hoàn tất đơn |
| Driver | `GET /driver/info` | Lấy thông tin tài xế |
| Driver | `POST /driver/{id}/vehicle-detail` | Gửi thông tin phương tiện |
| Transaction | `POST /transactions/deposit` | Nạp tiền |
| Transaction | `POST /transactions/withdraw` | Rút tiền |
| Wallet | `GET /wallet/getWallet/{driverId}` | Lấy số dư ví |
| Bank | `GET /bank/getList/{driverId}` | Tài khoản ngân hàng |
| Location | `POST /location/update` | Cập nhật vị trí GPS |
| Image | `POST /images/upload` | Upload ảnh CCCD/xe |

---

## 🛠 Công nghệ sử dụng
- Java Spring Boot
- RESTful API
- MySQL
- Cloudinary
- WebSocket (giao tiếp thời gian thực)
- JWT Authentication
- Maven

---

📁 *Dự án đang được phát triển và mở rộng thêm nhiều chức năng.*

