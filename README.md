# Bài 5 : Tối ưu quy trình hỗ trợ kỹ thuật nội bộ
## 1. Thiết kế Bug Report Template
**BUG REPORT TEMPLATE**

![BẮT BUỘC ĐIỀN TRƯỚC KHI HỎI](https://img.shields.io/badge/B%E1%BA%AET_BU%E1%BB%98C-%C4%90I%E1%BB%80N_TR%C6%AF%E1%BB%9AC_KHI_H%E1%BB%8EI-1E90FF?style=flat&labelColor=EAF3FF)
### 1. CONTEXT – Bối cảnh
Mô tả môi trường và thao tác xảy ra lỗi.
- Hệ điều hành: Windows 11 / macOS / Linux.
- Công cụ: Docker Desktop, Git, VS Code...
- Phiên bản phần mềm: Ví dụ Docker 4.x.
- Thao tác trước khi xảy ra lỗi: Ví dụ chạy `docker compose up`.
### 2. EXPECTED – Kết quả mong đợi
Bạn muốn hệ thống hoạt động như thế nào?

Ví dụ: Docker khởi chạy thành công các container và ứng dụng truy cập được tại `localhost:3000`.
### 3. ACTUAL – Kết quả thực tế
Điều gì thực sự xảy ra?

Ví dụ: Docker báo lỗi `port is already allocated`, container không thể khởi chạy.
### 4. LOG – Nhật ký lỗi
Cung cấp bằng chứng để người khác xác định nguyên nhân.
- Nội dung lỗi đầy đủ trong Terminal.
- Ảnh chụp màn hình nếu cần.
- Các bước đã thử để khắc phục.
- Lưu ý: Xóa mật khẩu, API Key, Token và thông tin nhạy cảm trước khi chia sẻ.
## 2. Quy trình 3 bước tra cứu bắt buộc
### `Bước 1` GOOGLING – Tìm kiếm Google
**Mục tiêu:** Tìm nguyên nhân và cách khắc phục từ các nguồn tài liệu đáng tin cậy.

Sử dụng các toán tử tìm kiếm nâng cao:
```text
"Docker port is already allocated"
```
Hoặc:
```text
site:stackoverflow.com "port already allocated"
```
- Ưu tiên tài liệu chính thức.
- Tìm lỗi có thông báo giống với lỗi đang gặp.
- Đối chiếu phiên bản phần mềm.
### `Bước 2` COMMUNITY SEARCH – Tra cứu cộng đồng
**Mục tiêu:** Tìm kinh nghiệm xử lý từ những người từng gặp lỗi tương tự.

Các nguồn cần kiểm tra:
- Stack Overflow.
- GitHub Issues.
- GitHub Discussions.
- Reddit (cộng đồng kỹ thuật).

Cách đánh giá:
- Ưu tiên câu trả lời có nhiều lượt đồng tình.
- Kiểm tra thời gian đăng và phiên bản phần mềm.
- Đọc bình luận xác nhận đã khắc phục thành công.
- Không chạy các câu lệnh chưa hiểu rõ chức năng.
### `Bước 3` AI TRANSLATION – Nhờ AI giải thích
**Mục tiêu:** Hiểu tài liệu kỹ thuật tiếng Anh và phân tích hướng xử lý.

Sử dụng AI để:
- Dịch thông báo lỗi sang tiếng Việt.
- Giải thích nguyên nhân lỗi.
- Phân tích các phương án khắc phục.
- Giải thích chức năng và rủi ro của câu lệnh Terminal.

Ví dụ Prompt:
```text
Tôi gặp lỗi Docker:
"port is already allocated".

Hãy giải thích:
1. Nguyên nhân gây ra lỗi.
2. Cách kiểm tra tiến trình đang sử dụng cổng.
3. Các phương án khắc phục an toàn.
4. Rủi ro của từng phương án.

Không đề xuất lệnh xóa dữ liệu
hoặc thay đổi hệ thống khi chưa cần thiết.
```
## 3. Sơ đồ quy trình Troubleshooting tổng thể
```mermaid
flowchart TD
  A["Phát sinh lỗi kỹ thuật"] --> B["Điền Bug Report: 4 mảnh ghép"]
