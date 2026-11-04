**(Bài tập tổng hợp) Rà Soát An Toàn Thông Tin Trước Khi Bàn Giao Dự Án SmartCampus**

Phần 1: Nhận diện rủi ro và xử lý sự cố

- Tình huống 1:Dấu hiệu giả mạo là tên miền sai lỗi chính tả githuh thay vì github.

- Tình huống 2:Yêu cầu tắt windows defender là để hệ thống không chặn virus chuẩn bị xâm nhập vào máy.

- Quy tắc 5 KHÔNG: Tình huống 1 là KHÔNG click link lạ và KHÔNG điền mật khẩu. Tình huống 2 là KHÔNG tải và dùng phần mềm Crack.

- 4 Bước Cấp cứu: Ngắt mạng ngay. Dùng máy khác đổi mật khẩu các tài khoản quan trọng. Quét virus toàn bộ máy hoặc cài lại Win. Báo cho team biết để phòng ngừa.

Phần 2: Chuyển sang Password Manager

1. Rủi ro dùng chung: Hacker lấy được email sẽ dùng luôn mật khẩu đó đăng nhập GitHub và Vercel. Đây là Credential Stuffing   
     
2. Zero-Knowledge Architecture: Bitwarden chỉ lưu dữ liệu đã mã hóa, nên hacker chiếm được máy chủ cũng chỉ thấy các đoạn ký tự vô nghĩa.

3. Thông số tạo mật khẩu: Độ dài từ 16 ký tự trở lên. Bật tất cả các tùy chọn gồm chữ hoa/thường, số và ký tự đặc biệt.

Phần 3: Kích hoạt 2FA cho tài khoản GitHub

1. Nên dùng TOTP: SMS OTP dễ bị cướp SIM, bị nghe lén hoặc không nhận được mã. App TOTP tạo mã offline 100% an toàn ngay trên thiết bị.

2. Thứ tự bật 2FA: Vào cài đặt bảo mật c → chọn bật 2FA bằng Authenticator App. Mở app Google Authenticator → quét mã QR trên máy tính. Nhập mã 6 số từ điện thoại lên GitHub để xác nhận.

3. Lưu Mã khôi phục: Nên lưu vào phần mềm quản lý mật khẩu hoặc in ra giấy. Không chụp màn hình hoặc app ghi chú.

Phần 4: Bảo vệ Secrets trước khi push code

1. 2 Secrets đang bị lộ: Chuỗi sk-proj-abc123456789 và chuỗi SmartCampus@2026.

2. Sửa lại code [config.js](http://config.js): const API\_KEY \= process.env.API\_KEY; const DB\_PASSWORD \= process.env.DB\_PASSWORD; function connectDatabase() { return connect(DB\_PASSWORD); }

3. Nội dung các file: File .env: Viết API\_KEY=sk-proj-abc123456789 và DB\_PASSWORD=SmartCampus@2026 trên 2 dòng. File .gitignore: Ghi thêm dòng chứa chữ .env để Git bỏ qua.File .env.example: Viết API\_KEY= và DB\_PASSWORD= nhưng để trống giá trị đằng sau.

4. Kiểm tra trước khi Push: Gõ lệnh git status xem có  file .env không. Gõ lệnh git diff kiểm tra code xem còn dính mật khẩu không. Đảm bảo file .gitignore đã được lưu cập nhật.

