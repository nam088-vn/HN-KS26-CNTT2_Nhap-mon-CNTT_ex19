**Bài 10: Đánh Giá Đa Giải Pháp Xác Thực Đa Yếu Tố (2FA)**

Phần 1: Phân tích 2 Giải pháp Xác thực

1\. Phân tích 3 lớp yếu tố xác thực danh tính số:

- Know : Mật khẩu, mã PIN, câu hỏi bảo mật

- Have : Điện thoại, Token khóa vật lý, thẻ từ  
    
- Are: Vân tay, Face ID, mống mắt  
     
- Mật khẩu đại diện cho yếu tố Know  
    
- Mã OTP đại diện cho yếu tố Have

2\. Nguyên lý hoạt động: App authenticator không cần tải từ internet về. Mà nó hoạt động dựa vào 2 đầu vào đã được chốt từ lúc bạn quét mã QR thiết lập ban đầu:

* Khóa bí mật: Một chuỗi mã được lưu trên điện thoại và máy chủ.

* Thời gian thực: Thời gian trên đồng hồ hệ thống của thiết bị.

Phần 2: Lập bảng So sánh Trade-off và Ra quyết định

3\. Bảng so sánh giữa SMS OTP và TOTP Authenticator:

| Tiêu chí đánh giá | SMS OTP | TOTP Authenticator |
| :---- | :---- | :---- |
| 1\. Khả năng chống tấn công SIM Swapping & Nghe lén viễn thông SS7 | Kém | Tuyệt đối |
| 2\. Tính sẵn sàng khi Offline / Nước ngoài | Phụ thuộc sóng di động, mất sóng hoặc ra nước ngoài không nhận được mã | Hoạt động mọi lúc mọi nơi kể cả trên máy bay và nơi không có mạng |
| 3\. Độ tiện dụng & Chi phí vận hành | Quen thuộc nhưng tốn chi phí | Miễn phí 100% |
| 4\. Rủi ro khi mất điện thoại | Nguy cơ bị kẻ xấu đánh cắp SIM | Cần có Mã Khôi phục |

4\. Quyết định cho Ban Giám đốc PixelForge Studio

Nên chọn TOTP Authenticator để chống rủi ro cướp sim bảo vệ tài sản lớn và đảm bảo khả năng tạo mã offline 100% cho các kỹ sư khi làm việc trên máy bay hoặc công tác quốc tế.

Phần 3: Quản lý Rủi ro và Backup Codes

5\. Mục đích và cách quản lý Backup Codes:

* Mục đích: Nếu kỹ sư làm mất điện thoại, hỏng máy hoặc lỡ tay xóa app authenticator, đây là con đường duy nhất để lách qua lớp 2FA, đăng nhập vào tài khoản và thiết lập lại ứng dụng xác thực sang máy mới.

* 2 vị trí an toàn tuyệt đối để lưu trữ:

  1. Lưu vào một Trình quản lý mật khẩu có mã hóa mạnh   
  2. In ra giấy và cất trong vào chỗ an toàn hoặc ngăn kéo có khóa ở nhà.

* 1 sai lầm nên tránh: Chụp ảnh màn hình chứa Backup Codes và để lưu trong thư viện ảnh hoặc copy vào app ghi chú không đặt mật khẩu trên điện thoại và khi điện thoại vào tay kẻ gian, tài khoản sẽ lập tức bị chiếm đoạt.

