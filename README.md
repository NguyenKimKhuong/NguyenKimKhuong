KTPM-N05-Nhóm 15
 
 
 Movie Review Website

 Mô tả dự án

Trang web đánh giá phim cho phép người dùng đăng nhập, xem danh sách phim, viết đánh giá và chấm điểm các bộ phim đã xem. Mục tiêu là xây dựng một hệ thống đơn giản, dễ sử dụng, phục vụ cho nhu cầu chia sẻ trải nghiệm xem phim giữa các người dùng.

---

## ✅ Các yêu cầu chức năng (Functional Requirements)

1. **Đăng ký / Đăng nhập người dùng**
   - Người dùng có thể tạo tài khoản và đăng nhập vào hệ thống.

2. **Xem danh sách phim**
   - Giao diện hiển thị danh sách các bộ phim hiện có trong hệ thống.

3. **Tìm kiếm phim**
   - Tìm kiếm phim theo tên, thể loại hoặc năm phát hành.

4. **Xem thông tin chi tiết phim**
   - Gồm tên phim, ảnh, mô tả, năm phát hành, thể loại và điểm đánh giá trung bình.

5. **Viết đánh giá và chấm điểm phim**
   - Người dùng có thể chấm điểm (1–5 sao) và viết nhận xét.

6. **Xem đánh giá từ người khác**
   - Hiển thị danh sách các bình luận, nhận xét từ người dùng khác.

7. **Quản trị viên (Admin)**
   - Quản lý danh sách phim: thêm, sửa, xóa.
   - Xóa đánh giá vi phạm.

---

## ❌ Yêu cầu phi chức năng (Non-functional Requirements)

- **Hiệu năng**: Trang web phản hồi trong vòng 2 giây cho các thao tác cơ bản.
- **Khả năng mở rộng**: Có thể tích hợp thêm API từ bên ngoài (TMDB) trong tương lai.
- **Bảo mật**: Mật khẩu được mã hóa, chỉ có admin mới có thể quản lý phim và kiểm duyệt.
- **Tính khả dụng**: Giao diện đơn giản, dễ sử dụng, hỗ trợ tốt trên desktop và thiết bị di động.

---

## 🧰 Công nghệ sử dụng

### 🔧 Backend
- **Ngôn ngữ**: PHP
- **Framework**: Laravel (hoặc PHP thuần)
- **Cơ sở dữ liệu**: MySQL

### 🎨 Frontend
- **HTML/CSS**: Tailwind CSS hoặc Bootstrap
- **JavaScript**: Vanilla JS (hoặc jQuery nếu cần)
- **Giao diện**: Responsive, dễ sử dụng

### 🌐 Hosting
- Có thể triển khai trên:
  - XAMPP / Laravel Homestead (dev)
  - Hosting nội bộ / Heroku / Vercel (demo)

---

## 🗃️ Cấu trúc cơ sở dữ liệu (tóm tắt)

```sql
Users(id, name, email, password, role)
Movies(id, title, description, release_year, genre, poster_url)
Reviews(id, user_id, movie_id, rating, comment, created_at)
