### 1. Lakehouse Anti-Pattern
Trong 5 Anti-patterns, tôi thấy ấn tượng nhất là "Tách rời Vector DB khỏi Lakehouse mà không có cơ chế quản lý vòng đời dữ liệu" (như Notebook 7). Việc đồng bộ dữ liệu một chiều (Upsert) mà quên đi sự kiện xóa (Deletes) tạo ra những lỗ hổng nguy hiểm về tính tuân thủ. Nếu người dùng yêu cầu gỡ bỏ dữ liệu của họ (GDPR), dữ liệu Lakehouse biến mất nhưng các bản sao embeddings ngoài hệ thống cũ vẫn tồn tại vô thời hạn, khiến AI tiếp tục sinh câu trả lời từ dữ liệu trái phép.

### 2. Khai báo sử dụng AI
Trong bài lab này, tôi dùng Claude và Google Antigravity để: giải thích khái niệm; hướng dẫn các lệnh PowerShell cho việc cài đặt môi trường, chạy smoke test, pytest và run_all (tôi tự gõ và chạy các lệnh này); gỡ lỗi UnicodeEncodeError và PermissionError; đối chiếu kết quả với RUBRIC. Tôi tự chạy toàn bộ notebook, thu thập output và kiểm tra các số liệu trong bài.
