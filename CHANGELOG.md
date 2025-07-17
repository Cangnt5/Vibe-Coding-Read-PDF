# CHANGELOG

## Ngày 17/07/2025 - Phiên bản 1.0.1

### Sửa lỗi và cải thiện

1. **Xử lý PDF lỗi**
   - Thêm kiểm tra kích thước tệp PDF (giới hạn 50MB)
   - Xử lý phát hiện PDF được bảo vệ bằng mật khẩu
   - Thêm timeout 60 giây khi xử lý PDF phức tạp để tránh treo trình duyệt
   - Giới hạn số trang PDF (tối đa 100 trang)
   - Xử lý lỗi khi trích xuất văn bản từ từng trang riêng biệt
   - Phát hiện và thông báo khi PDF không chứa văn bản có thể trích xuất

2. **Xử lý API key không hợp lệ**
   - Xác thực API key trước khi thực hiện cuộc gọi API
   - Thêm thông báo rõ ràng khi API key chưa được cấu hình hoặc không hợp lệ
   - Ngăn chặn các cuộc gọi API khi không có API key hợp lệ

3. **Xử lý file không được hỗ trợ**
   - Cải thiện phát hiện loại file thông qua phần mở rộng khi MIME type bị thiếu
   - Thêm danh sách các loại file được hỗ trợ rõ ràng
   - Kiểm tra tính hợp lệ của loại file trước khi xử lý

4. **Xử lý hình ảnh quá lớn**
   - Giới hạn kích thước hình ảnh ở mức 10MB
   - Thêm timeout 30 giây khi xử lý hình ảnh lớn
   - Thông báo lỗi khi hình ảnh vượt quá kích thước cho phép

5. **Thiếu xử lý lỗi mạng**
   - Triển khai fetchWithTimeout để xử lý kết nối bị gián đoạn
   - Phân loại và hiển thị thông báo lỗi mạng cụ thể
   - Cải thiện xử lý lỗi khi gọi API Gemini

6. **Xử lý văn bản quá lớn trong knowledgeBase**
   - Giới hạn mỗi tài liệu tối đa 50,000 ký tự
   - Giới hạn tổng số tài liệu xử lý (tối đa 10)
   - Cắt ngắn nội dung quá dài và thông báo cho người dùng

7. **Xử lý ấn nút gửi nhiều lần**
   - Thêm biến theo dõi trạng thái gửi tin nhắn
   - Vô hiệu hóa nút gửi khi đang xử lý yêu cầu
   - Tránh trùng lặp yêu cầu khi người dùng nhấn gửi nhiều lần

8. **Thiếu xác thực MIME type của file**
   - Kiểm tra tính hợp lệ của MIME type
   - So sánh phần mở rộng file với MIME type để đảm bảo tính nhất quán
   - Xử lý các trường hợp MIME type bị thiếu hoặc không chính xác

9. **Xử lý không đồng bộ trong các state update**
   - Tách các cập nhật state để tránh các vấn đề render
   - Sử dụng setTimeout để phân tách các lệnh cập nhật state liên quan
   - Cải thiện logic xử lý khi tải file và gửi tin nhắn

10. **Thiếu kiểm tra và xử lý trùng lặp khi tải lên cùng file nhiều lần**
    - Phát hiện trùng lặp theo tên file
    - Thêm tính năng phát hiện nội dung trùng lặp cho file nhỏ (<1MB)
    - Thông báo rõ ràng khi phát hiện file trùng lặp

### Cải thiện khác

- Thêm giới hạn số lượng file tải lên cùng lúc (tối đa 5 file)
- Giới hạn tổng số file trong tài liệu (tối đa 20 file)
- Thêm thông báo cảnh báo khi API key chưa được cấu hình
- Cập nhật giao diện với thông báo lỗi chi tiết và cụ thể hơn
