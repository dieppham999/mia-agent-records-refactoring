# AI Prompt Log – M.I.A Agent Records Refactoring

### Prompt 01 – Khởi tạo tài liệu dự án

**Câu hỏi:**

> Tạo README và tóm tắt đầu bài vào đó.

**Mục đích:** Nắm rõ mục tiêu, yêu cầu kỹ thuật, cấu trúc bảng và các tiêu chí đánh giá trước khi triển khai.

**Kiến thức tiếp thu:** Xác định bảng gồm 4 cột, 4 đặc vụ, sử dụng `rowspan` để nhóm theo khu vực và `colspan` để tạo hàng tổng kết.

### Prompt 02 – Đặt tên thư mục dự án

**Câu hỏi:**

> Đặt tên folder cho dự án.

**Mục đích:** Đặt tên thư mục dễ hiểu, thể hiện đúng chức năng của dự án.

**Kết quả:** Sử dụng tên `mia-agent-records-refactoring`.

### Prompt 03 – Tìm hiểu CSS cơ bản

**Câu hỏi:**

> Đưa cho mình các CSS cơ bản phải có khi bắt đầu dự án.

**Mục đích:** Tìm hiểu cách chuẩn hóa CSS, tránh sự khác biệt về margin, padding và kích thước phần tử giữa các trình duyệt.

**Kiến thức tiếp thu:** CSS Reset, `box-sizing: border-box`, typography, CSS Variables và các quy tắc định dạng bảng.

### Prompt 04 – Tạo đường viền bằng CSS

**Câu hỏi:**

> CSS tạo border.

**Mục đích:** Tìm hiểu cú pháp khai báo đường viền và các kiểu đường viền trong CSS.

**Kiến thức tiếp thu:** Thuộc tính `border` gồm độ dày, kiểu viền và màu sắc.

### Prompt 05 – Tạo đường viền cho bảng HTML

**Câu hỏi:**

> CSS tạo border cho table.

**Mục đích:** Hiển thị ranh giới giữa các ô trong bảng để dễ kiểm tra bố cục và lỗi gộp ô.

**Kiến thức tiếp thu:** Sử dụng `border` cho `table`, `th`, `td` và `border-collapse: collapse` để tránh viền đôi.

### Prompt 06 – Tìm hiểu giá trị solid

**Câu hỏi:**

> Solid là sao?

**Mục đích:** Hiểu ý nghĩa của `solid` trong khai báo CSS Border.

**Kiến thức tiếp thu:** `solid` tạo đường viền nét liền; phân biệt với `dashed`, `dotted` và `double`.

### Prompt 07 – Điều chỉnh độ dày đường viền

**Câu hỏi:**

> Đường viền bôi đậm thì CSS thế nào?

**Mục đích:** Làm nổi bật đường viền ngoài của bảng so với đường viền giữa các ô.

**Kiến thức tiếp thu:** Tăng độ dày `border` bằng đơn vị `px`, ví dụ `2px` hoặc `3px`.

### Prompt 08 – Điều chỉnh kích thước bảng

**Câu hỏi:**

> Muốn kéo giãn table cho đẹp thì sử dụng CSS như thế nào?

*Câu hỏi được gửi kèm ảnh chụp giao diện bảng đang hiển thị trên trình duyệt.*

**Mục đích:** Khắc phục tình trạng bảng quá nhỏ, các cột sát nhau và nội dung thiếu khoảng cách.

**Kiến thức tiếp thu:**
- `width: 100%` giúp bảng mở rộng theo phần tử cha.
- `max-width` giới hạn chiều rộng tối đa.
- `padding` tạo khoảng cách trong các ô.
- `margin: auto` giúp căn giữa bảng khi có không gian dư.

### Prompt 09 – Kiểm tra cấu trúc Semantic HTML Table

**Câu hỏi:**

> Mình không sử dụng tbody liệu có đúng không?

*Câu hỏi được gửi kèm mã HTML thực tế của bảng M.I.A, sử dụng rowspan và colspan nhưng chưa khai báo thead, tbody.*

**Mục đích:** Kiểm tra tính hợp lệ của HTML và xác định có cần sử dụng các thẻ phân nhóm bảng hay không.

**Kiến thức tiếp thu:**
- HTML Table vẫn có thể hợp lệ khi không khai báo trực tiếp `<tbody>`.
- Trình duyệt có thể tự chèn `<tbody>` vào DOM.
- `<thead>` dùng để nhóm hàng tiêu đề.
- `<tbody>` dùng để nhóm các hàng dữ liệu.
- `<tfoot>` có thể dùng cho hàng tổng kết.
- Theo yêu cầu bài tập, cần khai báo rõ `<thead>` và `<tbody>`.