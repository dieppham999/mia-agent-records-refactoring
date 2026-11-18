# M.I.A Agent Records Refactoring

## 1. Giới thiệu dự án

Dự án **Tái thiết Hệ thống Hồ sơ Đặc vụ M.I.A** nhằm chuyển đổi dữ liệu đặc vụ từ các thẻ HTML `<p>` rời rạc thành một bảng HTML có cấu trúc rõ ràng, dễ đọc và dễ so sánh.

**Vai trò:** Frontend Trainee  
**Công nghệ:** HTML5, CSS cơ bản  
**Hình thức:** Bảng dữ liệu tĩnh (Hard Code)

## 2. Mục tiêu

- Sử dụng thành thạo các thẻ `<table>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>`.
- Hiểu và áp dụng `rowspan` để gộp ô theo hàng.
- Sử dụng `colspan` để gộp ô theo cột.
- Xây dựng bảng HTML không bị thừa ô, thiếu ô hoặc vỡ bố cục.

## 3. Yêu cầu chức năng

### 3.1. Cấu trúc bảng

Bảng gồm 4 cột:

| Khu vực | Mã đặc vụ | Tên đặc vụ | Cấp bậc |
|---|---|---|---|
| Châu Á | 007 | James Bond | Senior |
| | 099 | John Doe | Trainee |
| Châu Âu | 006 | Alec Trevelyan | Senior |
| | 102 | Silva | Rogue |

**Yêu cầu:**
- Sử dụng `<thead>` cho tiêu đề bảng.
- Sử dụng `<tbody>` cho dữ liệu đặc vụ.
- Áp dụng `rowspan="2"` cho hai khu vực Châu Á và Châu Âu.
- Sử dụng `colspan="4"` để tạo hàng tổng kết: **Tổng số lượng đặc vụ: 4**.

### 3.2. Quy tắc gộp ô

**rowspan:**
- Gộp nhiều hàng theo chiều dọc.
- Khi sử dụng `rowspan="2"`, hàng tiếp theo không cần khai báo lại ô đã được gộp.
- Hàng đầu tiên của mỗi khu vực có 4 ô `<td>`, hàng thứ hai chỉ có 3 ô `<td>`.

**colspan:**
- Gộp nhiều cột theo chiều ngang.
- Khi sử dụng `colspan="4"`, một ô chiếm toàn bộ chiều rộng của bảng 4 cột.

## 4. Quy trình thực hiện

**Bước 1: Phân tích**
- Đọc Legacy Code.
- Xác định 4 cột dữ liệu.
- Xác định các khu vực cần gộp ô.

**Bước 2: Thiết kế**
- Phác thảo bố cục bảng.
- Tính toán số ô trong mỗi hàng.
- Xác định vị trí sử dụng `rowspan` và `colspan`.

**Bước 3: Triển khai**
- Xây dựng bảng HTML tĩnh.
- Phân chia `<thead>` và `<tbody>`.
- Áp dụng thuộc tính gộp ô.
- Thêm hàng tổng kết.

**Bước 4: Kiểm thử**
- Mở `index.html` trên trình duyệt.
- Kiểm tra bố cục và đường viền các ô.
- Thử thêm hoặc xóa đặc vụ và điều chỉnh `rowspan` phù hợp.

## 5. Cấu trúc thư mục

```text
mia-agent-records-refactoring/
├── index.html          # Bảng hồ sơ đặc vụ
├── ai_prompt_log.md    # Nhật ký trao đổi với AI
└── README.md           # Tài liệu dự án
```

## 6. Kiến thức cần nắm vững

**Câu 1:** Tại sao hàng John Doe có ít hơn hàng James Bond một thẻ `<td>`?

Vì ô khu vực Châu Á đã sử dụng `rowspan="2"`, chiếm vị trí ở cả hai hàng. Do đó, hàng John Doe không cần khai báo lại ô khu vực.

**Câu 2:** Sự khác biệt giữa `<th>` và `<td>`?

- `<th>`: Biểu thị ô tiêu đề, mặc định thường in đậm và căn giữa.
- `<td>`: Biểu thị ô dữ liệu thông thường, mặc định căn trái.

**Câu 3:** Tại sao sử dụng `<thead>` và `<tbody>`?

Giúp phân chia tiêu đề và nội dung bảng theo ngữ nghĩa, thuận tiện cho việc quản lý, định dạng CSS và hỗ trợ công nghệ trợ năng.

## 7. Tiêu chí đánh giá

| Tiêu chí | Tỷ trọng |
|---|---|
| Chất lượng sản phẩm HTML | 40% |
| Bảo vệ mã nguồn và vấn đáp | 40% |
| Kỹ năng tương tác AI và Prompt Log | 20% |

**Lưu ý:** AI chỉ được sử dụng để giải thích kiến thức, phản biện logic gộp ô, hỗ trợ tìm lỗi và sinh dữ liệu giả. Học viên phải tự triển khai bảng HTML.

## 8. Sản phẩm nộp bài

- `index.html`: Bảng HTML hoàn chỉnh, thay thế dữ liệu dạng đoạn văn cũ.
- `ai_prompt_log.md`: Nhật ký các câu hỏi thực tế đã trao đổi với AI trong quá trình thực hiện.

## 9. Kết luận

Dự án giúp củng cố kỹ năng xây dựng bảng dữ liệu HTML, xử lý gộp ô bằng `rowspan` và `colspan`, đồng thời rèn luyện khả năng phân tích cấu trúc, kiểm thử giao diện và giải thích mã nguồn.