<div align="center">
  <img src="https://media.giphy.com/media/3o6gDWq2GkM3R94D0I/giphy.gif" width="100px">
  
  # 🛍️ 36FULLZ Fashion E-Commerce
  
  *Website thương mại điện tử thời trang tích hợp thanh toán trực tuyến toàn diện.*
</div>

---

## 🚀 Giới thiệu

**36FULLZ Fashion** là một dự án website thương mại điện tử được xây dựng bằng PHP, tập trung vào trải nghiệm mua sắm mượt mà cho người dùng và cung cấp bộ công cụ quản trị mạnh mẽ, chi tiết cho chủ cửa hàng. Hệ thống hỗ trợ xử lý toàn bộ vòng đời của một đơn hàng từ lúc thêm vào giỏ, chọn phân loại (màu sắc, kích cỡ) cho đến khi thanh toán online qua VNPay/Momo.

---

## 🛠 Công nghệ sử dụng

*   **Frontend:** HTML5, CSS3 (SCSS, chuẩn BEM), Vanilla JavaScript, jQuery, Ajax.
*   **Backend:** PHP thuần.
*   **Cơ sở dữ liệu:** MySQL.
*   **Thư viện & Tiện ích:** 
    *   `Carbon` xử lý datetime.
    *   `PHPMailer` hỗ trợ gửi mã xác nhận (Quên mật khẩu).
    *   `CKEditor` & `CKFinder` soạn thảo nội dung, chi tiết sản phẩm.
*   **Cổng thanh toán:** VNPay, Momo Sandbox.

---

## 🌟 Tính năng nổi bật

### 👤 Giao diện Người dùng (Customer)
*   **Xác thực:** Đăng nhập, Đăng ký, Quên mật khẩu qua mã OTP gửi tới Email.
*   **Mua sắm:** Xem danh mục, loại sản phẩm, chi tiết sản phẩm (kèm hình ảnh mô tả chi tiết, giá giảm).
*   **Lọc & Tìm kiếm:** Lọc theo mức giá, danh mục, tìm kiếm theo tên.
*   **Giỏ hàng (Cart):** Thêm, sửa, xóa sản phẩm trong giỏ, cập nhật số lượng dựa trên tồn kho thực tế. Ajax thêm giỏ hàng không cần reload.
*   **Thanh toán (Checkout):** 
    *   Ship COD (Thanh toán khi nhận hàng).
    *   Tích hợp cổng thanh toán trực tuyến **VNPay** và **Momo**.
    *   Tự động tính phí ship (Freeship cho đơn trên 2 triệu).
*   **Tương tác:** Đánh giá sao (Rating), Bình luận/Hỏi đáp, Lưu sản phẩm yêu thích (Wishlist).
*   **Quản lý cá nhân:** Xem lịch sử đơn hàng, trạng thái xử lý, cập nhật thông tin cá nhân.

### 👑 Trang Quản trị (Admin Dashboard)
*   **Tổng quan (Dashboard):** Thống kê và báo cáo doanh thu trực quan.
*   **Quản lý Sản phẩm:** 
    *   Thêm/Sửa/Xóa phân cấp: Danh mục -> Loại sản phẩm -> Sản phẩm.
    *   Quản lý biến thể: Màu sắc, Kích cỡ (Size S, M, L, XL, XXL).
    *   Quản lý hình ảnh (Ảnh đại diện & thư viện ảnh mô tả).
*   **Quản lý Đơn hàng:** Xác nhận đơn hàng, thay đổi trạng thái (Chưa xử lý, Đang giao, Đã hoàn thành), theo dõi phương thức thanh toán.
*   **Quản lý Tương tác:** Duyệt bình luận, theo dõi đánh giá sản phẩm.
*   **Quản lý Khách hàng:** Theo dõi danh sách tài khoản đã đăng ký trên hệ thống.
*   **Quản lý Giao diện:** Tùy chỉnh Slider trang chủ.

---

## 📂 Cấu trúc thư mục

```text
nv-duymanh-e-commerce-website/
├── index.php             # Trang chủ
├── product.php           # Trang chi tiết sản phẩm
├── cart.php              # Giỏ hàng
├── pay.php               # Giao diện thanh toán
├── Xulypay.php           # Xử lý logic thanh toán (VNPay, Momo)
├── detail.php / detaill.php # Quản lý thông tin user & lịch sử mua hàng
├── news.php / Show.php   # Bài viết, Tin tức
├── admin/                # Khu vực quản trị
│   ├── index.php         # Bảng điều khiển (Dashboard)
│   ├── Sanphamadd.php    # Thêm sản phẩm mới
│   ├── orderlist.php     # Quản lý đơn hàng
│   ├── ajax/             # Xử lý các request bất đồng bộ (Thống kê, thêm SP)
│   └── Carbon/           # Thư viện xử lý thời gian
├── assets/               # CSS, JS, SCSS và Hình ảnh
└── .htaccess             # Cấu hình routing, ẩn đuôi .php
```

---

## ⚙️ Hướng dẫn cài đặt

1. **Clone repository về máy:**
```bash
   git clone [https://github.com/NV-DuyManh/nv-duymanh-e-commerce-website.git](https://github.com/NV-DuyManh/nv-duymanh-e-commerce-website.git)
   ```
2. **Cài đặt môi trường:**
   * Di chuyển thư mục dự án vào thư mục gốc của Local Server (ví dụ: `htdocs` đối với XAMPP).
3. **Import Cơ sở dữ liệu:**
   * Truy cập `http://localhost/phpmyadmin/`.
   * Tạo một cơ sở dữ liệu mới (ví dụ: `db_36fullz`).
   * Import file `.sql` có sẵn trong thư mục dự án vào CSDL vừa tạo.
4. **Cấu hình kết nối:**
   * Mở file class kết nối Database (thường nằm trong `class/` hoặc cấu hình chung).
   * Thay đổi thông tin kết nối `localhost`, `root`, `password` và `database_name` cho phù hợp với máy của bạn.
5. **Chạy ứng dụng:**
   * Giao diện người dùng: `http://localhost/nv-duymanh-e-commerce-website/`
   * Trang quản trị: `http://localhost/nv-duymanh-e-commerce-website/admin/`

---

## 👨‍💻 Tác giả

**Nguyễn Văn Duy Mạnh**
- Vai trò: Full-stack Developer

Nếu bạn thấy dự án này hữu ích, hãy để lại một ⭐️ để ủng hộ tinh thần nhé!
