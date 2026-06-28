# Tiệm Truyện Chữ Desktop App

Bộ công cụ phần mềm Desktop chuyên dụng để đọc, đăng truyện, tìm kiếm, lưu tiến độ và đồng bộ truyện từ hệ thống Tiệm Truyện Chữ với giao diện tối ưu trải nghiệm và bảo mật cao.

> [!IMPORTANT]
> **Yêu cầu mã kích hoạt (Key):** Phần mềm yêu cầu mã kích hoạt theo thiết bị (HWID) để sử dụng. Vui lòng liên hệ qua email **bqthang28122003@gmail.com** để được cấp mã kích hoạt thiết bị của bạn.

---

## 📋 Yêu cầu hệ thống
- **Hệ điều hành:** Windows 10 / 11
- **Node.js:** Phiên bản `>= 18` (dành cho chế độ phát triển và đóng gói)

---

## 🚀 Quick Start (Khởi chạy nhanh)

### Bước 1: Tải mã nguồn và Cài đặt thư viện
Mở Terminal (Command Prompt / PowerShell) tại thư mục chứa mã nguồn và chạy lệnh:
```bash
npm install
```

### Bước 2: Chạy ứng dụng (Chế độ Developer)
Chạy thử ứng dụng trực tiếp trong môi trường phát triển:
```bash
npm start
```

### Bước 3: Đóng gói thành file cài đặt độc lập (.exe)

- **Đóng gói thông thường:**
  ```bash
  npm run build
  ```

- **Đóng gói Bảo Mật (Tự động xáo trộn code chống dịch ngược):**
  *Yêu cầu mở Terminal dưới quyền quản trị viên (**Run as Administrator**)*
  ```bash
  npm run build:secure
  ```
  *File cài đặt `.exe` duy nhất sau khi đóng gói sẽ tự động được tạo ra trong thư mục `dist/`.*

---

## 📂 Cấu trúc Project
```text
tiemtruyenchu-proxy/
├── package.json          # Khai báo thông tin dự án, thư viện & các script build
├── main.js               # Backend Electron chính (quản lý vòng đời app, cửa sổ đăng nhập Google)
├── preload.js            # Cầu nối bảo mật (Bridge) giữa Electron và giao diện web
├── server.js             # Local Proxy Server (điều hướng API, xử lý ảnh & xác thực bản quyền)
├── build-secure.js       # Script tự động xáo trộn mã nguồn trước khi đóng gói thành file exe
├── ui/                   # Giao diện ứng dụng (Frontend SPA)
│   ├── index.html        # Giao diện HTML chính (thiết kế responsive)
│   ├── styles.css        # Giao diện CSS phong cách Premium Dark Mode
│   └── app.js            # Logic frontend xử lý sự kiện, API đọc truyện, lịch sử tiến độ...
└── README.md             # Tài liệu hướng dẫn sử dụng dự án
```

---

## ✨ Các tính năng nổi bật

| Tính năng | Mô tả chi tiết |
| :--- | :--- |
| **Đăng & Quản Lý Truyện** | Hỗ trợ tính năng đăng truyện mới, thêm chương trực quan như trên trang web chính thức. |
| **Đăng Nhập Linh Hoạt** | Hỗ trợ đăng nhập nhanh qua Google hoặc đăng nhập truyền thống bằng Tài khoản & Mật khẩu. |
| **Thống Kê & Lịch Sử Giao Dịch** | Hỗ trợ xem thống kê ngân quỹ, số chương đã đọc/đã mua, tủ truyện và biến động số dư hoa trực quan sinh động. |
| **Tìm Kiếm Gợi Ý Thông Minh** | Hỗ trợ tìm kiếm đa chiều theo **Truyện**, **Tác giả**, và **Người đăng** với cơ chế Fuzzy Search (tìm kiếm gần đúng) cực kỳ linh hoạt. |
| **Đọc Tiếp Tiện Lợi** | Tự động ghi nhớ tiến độ đọc của từng chương và hiển thị nút "Đọc tiếp" nổi bật ngay tại đầu trang chi tiết truyện. |
| **Khóa Bản Quyền Theo Thiết Bị** | Tự động quét mã phần cứng Mainboard/CPU (HWID) để khóa bản quyền, kiểm tra và cập nhật trạng thái kích hoạt trực tiếp thông qua Google Sheets. |
| **Bảo Mật Xáo Trộn Code** | Tích hợp thư viện xáo trộn (obfuscator) tự động mã hóa chuỗi ký tự, chặn dịch ngược file `.exe` để bảo vệ mã nguồn. |

---

## ✉️ Hỗ trợ & Liên hệ
Mọi thắc mắc về kỹ thuật, báo lỗi hoặc yêu cầu cấp mã kích hoạt thiết bị, vui lòng gửi email về:
📩 **bqthang28122003@gmail.com**
