**Bài 9: Thiết Kế Kiến Trúc Két Sắt Số Bitwarden Và Chính Sách Mật Khẩu Game Studio**

**Phần 1: Báo cáo phân tích kiến trúc an ninh mật khẩu**

- Vì khi chrome lưu mật khẩu, nếu nhiễm mã độc ăn cắp dữ liệu, mã độc sẽ hack  vào để lấy file và giải mã tất cả mật khẩu trong nháy mắt.

- Nếu Bitwarden bị hack, dữ liệu của studio vẫn an toàn tuyệt đối, mật khẩu đã được mã hóa ngay trên máy của bạn trước khi gửi lên mạng. 

**Phần 2: Thiết kế Chính sách và Kịch bản Chuyển đổi**

- Thiết kế: Dùng chữ cái in hoa, thường hoặc dùng như bí danh của bản thân và thêm các chữ số cùng với kí tự đặc biệt dài khoảng hơn 12 kí t .Ví dụ: Meobuhaybuon@20918.

- Cấu hình chuẩn cho Generator: Đặt độ dài 24 ký tự và yêu cầu bắt buộc phải trộn đủ cả chữ hoa, chữ thường, chữ số và ký tự đặc biệt.

- Tính năng tự động điền chống giả mạo: Nó quét mã máy tính, vân tay và chỉ điền mật khẩu khi tên miền khớp chính xác 100% với trang web gốc.

- Lưu trữ Khóa Cấp cứu: Lưu trữ mật khẩu trên đám mây như Icloud của apple hoặc Bitwarden

