# Vibe-Coding-Read-PDF

Ứng dụng đọc và phân tích tài liệu PDF, hình ảnh và văn bản.

## Tính năng

- Tải lên và xử lý file PDF, hình ảnh (JPG, PNG) và file văn bản (TXT)
- Trích xuất nội dung văn bản từ PDF sử dụng PDF.js
- Trích xuất văn bản từ hình ảnh bằng Google Gemini Vision API
- Trả lời câu hỏi dựa trên nội dung tài liệu với trợ lý AI

## Cách sử dụng

1. Mở file `index.html` trong trình duyệt hoặc chạy local server:
   ```
   python3 -m http.server 8080
   ```
   Sau đó truy cập: http://localhost:8080

2. Tải lên tài liệu bằng cách nhấn vào nút "Tải lên File"
3. Đặt câu hỏi liên quan đến nội dung trong tài liệu

## Yêu cầu

- Cần API key của Google Gemini để phân tích hình ảnh và trả lời câu hỏi
- Thay thế chuỗi "YOUR_GEMINI_API_KEY" trong file `index.html` bằng API key thực của bạn

## Lưu ý

- API key cần được bảo mật và không nên chia sẻ công khai
- Ứng dụng sử dụng các thư viện từ CDN nên cần kết nối internet để hoạt động
