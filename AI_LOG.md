# NHẬT KÝ SỬ DỤNG TRỢ LÝ AI (AI_LOG)

- **Học phần:** FIT4014 – Thiết kế web và triển khai hệ thống phần mềm
- **Bài tập lớn:** A3 – Thiết kế và triển khai Website
- **Tên dự án:** truongcobooking (Nền tảng chia sẻ và đặt phòng homestay)
- **Sinh viên thực hiện:** Nguyễn Bá Trường
- **Mã sinh viên:** 2071020217
- **Lớp:** CNTT 20-02

---

## 1. Tỷ lệ tự thực hiện & Phạm vi ứng dụng AI

### 1.1. Sinh viên tự thực hiện (~70% khối lượng)
- **Lên ý tưởng & nghiệp vụ:** Đề xuất ý tưởng website kết nối homestay cộng đồng theo khu vực (Sầm Sơn, Sapa, Tam Đảo); xác định các tiện ích thực tế phục vụ khách du lịch (chỗ để xe ô tô, ăn sáng/buffet chiều, chính sách đưa đón tận nơi).
- **Trực tiếp viết mã:** Tự tay viết cấu trúc khung HTML5 Semantic, các phân đoạn nội dung chính, bảng giá niêm yết, thông tin địa chỉ cụ thể từng căn và form đặt phòng.
- **Thiết kế & Tinh chỉnh CSS:** Lựa chọn bảng màu dịu mắt (xanh ngọc, kem ấm), thiết lập thẻ giá nổi bật (chữ đỏ trên nhãn trắng), căn chỉnh khoảng cách, padding và bố cục các khối.
- **Nội dung & Hình ảnh:** Tự soạn thảo toàn bộ đánh giá thực tế (đa dạng 4 sao, 5 sao kèm lời nhận xét chân thật); trực tiếp chuẩn bị và gán ảnh từ thư mục cục bộ `image/`.
- **Triển khai & Kiểm thử:** Tự khởi tạo kho Git, xử lý quyền truy cập Personal Access Token trên macOS, commit theo từng mốc tiến độ và kích hoạt GitHub Pages; tự kiểm thử hiển thị trên trình duyệt Safari, Chrome và chế độ F12 Responsive.

### 1.2. Trợ lý AI hỗ trợ (~30% khối lượng)
- Đóng vai trò như tài liệu tra cứu kỹ thuật, hỗ trợ gợi ý cú pháp CSS Grid/Flexbox và Media Queries để chống vỡ giao diện trên thiết bị di động.
- Gợi ý đoạn logic JavaScript cơ bản để đóng/mở popup (modal) hiển thị nhận xét cho từng căn phòng mà không cần chuyển hướng trang.
- Hỗ trợ chẩn đoán và khắc phục lỗi từ chối mật khẩu (`Authentication failed`) khi đẩy mã nguồn Git qua Terminal trên macOS.

---

## 2. Nhật ký chi tiết các lần tham vấn và triển khai

### Giai đoạn 1: Định hình cấu trúc và bố cục thẻ phòng
- **Vấn đề cần giải quyết:** Cần sắp xếp danh sách 4 căn phòng nghỉ theo các khu vực địa lý khác nhau sao cho gọn gàng, tự co giãn linh hoạt trên cả màn hình rộng và hẹp.
- **Nội dung tham vấn AI:** Tra cứu cú pháp `grid-template-columns: repeat(auto-fit, minmax(...))` và cách căn lề các khối thông tin.
- **Sinh viên triển khai thực tế:** Tự tạo cấu trúc thẻ phòng `.room-card`, viết CSS viền bo tròn, bóng đổ, đưa thông tin địa chỉ cụ thể từng căn vào vị trí trực quan và liên kết ảnh từ thư mục nội bộ `image/`.

### Giai đoạn 2: Khắc phục lỗi xác thực Git trên macOS
- **Vấn đề gặp phải:** Khi chạy lệnh `git push -u origin main` trên Terminal VS Code, hệ thống báo lỗi `Password authentication is not supported for Git operations` do chính sách bảo mật mới của GitHub.
- **Nội dung tham vấn AI:** Tìm hiểu nguyên nhân lỗi và hướng dẫn các bước tạo mã Personal Access Token (classic) với quyền `repo` trên trang Developer Settings của GitHub.
- **Sinh viên triển khai thực tế:** Tự truy cập tài khoản cá nhân, sinh mã Token bí mật, nhập xác thực qua Terminal và đẩy mã nguồn thành công lên repository `BookingHomestayBTLthietkeweb`.

### Giai đoạn 3: Tính năng xem đánh giá dạng popup (Modal)
- **Vấn đề cần giải quyết:** Muốn đặt nút "Xem nhận xét thực tế" ngay dưới ảnh từng căn phòng để người dùng tiện theo dõi mà không làm rối mắt hay kéo dài trang.
- **Nội dung tham vấn AI:** Gợi ý cấu trúc HTML Modal dạng hộp thoại ẩn/hiện và logic JS đơn giản để đổ dữ liệu theo từng mã phòng (`samson1`, `samson2`, `sapa`, `tamdao`).
- **Sinh viên triển khai thực tế:** Tự viết chi tiết nội dung từng lời nhận xét của khách du lịch (phân bổ số lượng tự nhiên từ 2 đến 5 đánh giá), tự gán sự kiện `onclick` và tinh chỉnh CSS cho giao diện modal sắc nét.

### Giai đoạn 4: Tối ưu Responsive và hoàn thiện Form
- **Vấn đề cần giải quyết:** Kiểm tra trên màn hình điện thoại thấy khung form đặt phòng và thanh menu bị chật chội, cần chỉnh lại theo dạng cột dọc.
- **Nội dung tham vấn AI:** Tra cứu các mốc `@media (max-width: 820px)` và `@media (max-width: 640px)`.
- **Sinh viên triển khai thực tế:** Bổ sung trường chọn "Hỗ trợ đưa đón tận nơi" vào form, cập nhật thông tin tác giả và địa chỉ Nhị Khê, Thường Tín ở chân trang footer; tự kiểm tra lại toàn bộ nút bấm trên trình duyệt.

---

## 3. Cam đoan trách nhiệm học tập

- Toàn bộ ý tưởng, nội dung hiển thị, hình ảnh, thông tin liên hệ và mã nguồn dự án đều do sinh viên trực tiếp quản lý, hiểu rõ từng thành phần và chịu trách nhiệm bảo vệ trước giảng viên.
- Công cụ AI chỉ được sử dụng với mục đích học hỏi cú pháp và hỗ trợ gỡ lỗi kỹ thuật trong phạm vi cho phép của môn học.