# Nhiệm Vụ Chuẩn Bị Cho Nhóm Dịch Thuật
*Dành cho quy trình Dịch Thuật Triết Học sử dụng LLM + RAG*

---

## 1. 🖋️ Phân Tích Phong Cách Viết (từ tác giả bạn yêu thích)

Mục tiêu là cung cấp đủ ngữ liệu để AI **mô phỏng giọng văn, nhịp điệu và phong cách** của tác giả bạn chọn.

### Nhiệm vụ
- **Thu thập ngữ liệu viết**: Tập hợp 20–50 đoạn trích tiêu biểu từ tác phẩm của tác giả — đa dạng về chủ đề, độ dài và mức độ trang trọng. Càng nhiều càng tốt (mục tiêu 30.000+ từ).
- **Chú thích đặc điểm phong cách**: Với mỗi đoạn trích, ghi chú:
  - Xu hướng độ dài câu (ngắn & súc tích hay dài & nhiều tầng nghĩa)
  - Sử dụng các biện pháp tu từ (câu hỏi tu từ, lặp từ, song hành cú pháp)
  - Mức độ trang trọng và văn phong
  - Cấu trúc đoạn văn thường dùng
  - Các cụm chuyển ý quen thuộc (ví dụ: *"Nói cách khác…"*, *"Hơn thế nữa…"*)
- **Tạo tài liệu Hướng Dẫn Phong Cách**: Tóm tắt giọng văn của tác giả trong 1–2 trang. Bao gồm:
  - "Tác giả này THƯỜNG LÀM: …"
  - "Tác giả này TRÁNH: …"
  - 5–10 ví dụ trước/sau minh hoạ sự chuyển đổi phong cách

---

## 2. 📖 Thống Nhất Bảng Thuật Ngữ Triết Học

Thuật ngữ triết học phải được dịch **nhất quán trong toàn bộ dự án**. Sự không nhất quán là vấn đề chất lượng số một trong dịch thuật triết học.

### Nhiệm vụ
- **Soạn thảo bảng thuật ngữ chính** (bảng tính với các cột):
  - Thuật ngữ tiếng Anh | Bản dịch tiếng Việt | Ghi chú / bối cảnh | Nguồn tham chiếu | Còn tranh cãi? (C/K)
- **Ưu tiên các thuật ngữ tần suất cao trước**: siêu hình học, nhận thức luận, đạo đức học, lôgíc học, hiện tượng học
- **Tra cứu các chuẩn tiếng Việt hiện có**: Tham khảo cách các học giả/dịch giả triết học Việt Nam đã dịch (ví dụ: giáo trình từ ĐHKHXH&NV, ĐHQG Hà Nội)
- **Gắn cờ các thuật ngữ còn tranh cãi**: Một số thuật ngữ có nhiều bản dịch cạnh tranh — ghi lại tất cả và chọn một dứt khoát
- **Thêm câu ví dụ**: Với mỗi thuật ngữ, kèm một câu ngữ cảnh (cả EN và VI)
- **Phân loại theo lĩnh vực**: thuật ngữ Aristotle, Kant, hiện sinh chủ nghĩa, v.v.
- **Xem xét và bỏ phiếu**: Toàn nhóm phải đồng thuận trước khi chốt bảng thuật ngữ

> [!IMPORTANT]
> Bảng thuật ngữ sẽ được đưa trực tiếp vào lệnh hướng dẫn AI. Hãy giữ định nghĩa ngắn gọn và rõ ràng.

---

## 3. 📚 Xây Dựng Kho Ngữ Liệu Song Ngữ (cho RAG)

RAG hoạt động bằng cách truy xuất **các đoạn tham chiếu liên quan** để làm ví dụ cho AI. Bạn cần một thư viện các cặp dịch EN↔VI chất lượng cao.

### Nhiệm vụ
- **Tìm kiếm các văn bản triết học song ngữ có sẵn**:
  - Các bản dịch tiếng Việt đã xuất bản chính thức
  - Luận văn, luận án có tóm tắt song ngữ
  - Tạp chí song ngữ (ví dụ: *Tạp chí Triết học*)
- **Định dạng mỗi cặp thành một đoạn tài liệu**: Một đoạn tiếng Anh + bản dịch tiếng Việt tương ứng. Cắt tại ranh giới đoạn văn tự nhiên, không cắt giữa câu.
- **Gắn thẻ metadata cho mỗi đoạn**:
  - Tác giả | Tên tác phẩm | Lĩnh vực (đạo đức, siêu hình, v.v.) | Độ khó | Chất lượng dịch (1–3 sao)
- **Đánh dấu các đoạn thể hiện phong cách viết mục tiêu**: Đây là ưu tiên truy xuất hàng đầu — gắn cờ rõ ràng.
- **Mục tiêu tối thiểu**: 500–1.000 cặp đoạn văn chất lượng cao trước khi ra mắt

---

## 4. 📝 Soạn Thảo Prompt Hệ Thống & Hướng Dẫn

Một thành viên (không cần kỹ thuật) cần viết **hướng dẫn bằng ngôn ngữ tự nhiên** để định hướng AI.

### Nhiệm vụ
- **Viết prompt hệ thống cơ bản** bao gồm:
  - Định nghĩa vai trò ("Bạn là dịch giả triết học chuyên về...")
  - Hướng dẫn giọng văn & phong cách (tham chiếu Hướng Dẫn Phong Cách)
  - Quy tắc xử lý thuật ngữ không thể dịch
  - Quy tắc chú thích các khái niệm khó
  - Sở thích về cấu trúc câu
- **Soạn hướng dẫn cho các trường hợp ngoại lệ**:
  - Khi thuật ngữ có trong bảng thuật ngữ (luôn dùng bản dịch đã chốt)
  - Khi thuật ngữ KHÔNG có trong bảng (phiên âm + ghi chú)
  - Cách xử lý trích dẫn lồng nhau
  - Cách xử lý ngôn ngữ giới tính (tiếng Anh ít hơn, tiếng Việt phức tạp hơn)
- **Tự kiểm tra hướng dẫn**: Đọc lại prompt và hỏi "Liệu một dịch giả người thật có hiểu rõ các quy tắc này không?"

---

## 5. 🔍 Xây Dựng Tiêu Chí Kiểm Soát Chất Lượng (QA)

Nhóm của bạn sẽ đánh giá kết quả đầu ra của AI. Họ cần một **tiêu chí rõ ràng** để đánh giá nhất quán.

### Nhiệm vụ
- **Xác định các chiều đánh giá** (chấm điểm 1–5 cho mỗi chiều):
  | Chiều đánh giá | Cần kiểm tra |
  |----------------|-------------|
  | Độ chính xác | Nghĩa có được truyền đạt trung thực không? |
  | Thuật ngữ | Các thuật ngữ trong bảng có được dùng đúng không? |
  | Phù hợp phong cách | Có nghe giống giọng văn mục tiêu không? |
  | Tính lưu loát | Tiếng Việt có tự nhiên và dễ đọc không? |
  | Chú thích | Các khái niệm khó có được chú thích phù hợp không? |
- **Tạo các bản dịch mẫu "tiêu chuẩn vàng"**: 10–20 đoạn được dịch bởi dịch giả giỏi nhất của bạn. Đây sẽ là thước đo chuẩn.
- **Viết danh sách kiểm tra cho người đánh giá** (1 trang): Danh sách đạt/không đạt nhanh mà mỗi người đánh giá dùng trước khi phê duyệt kết quả.

---

## 6. 🗂️ Tài Liệu Quy Trình Làm Việc

### Nhiệm vụ
- **Xác định quy trình dịch thuật** (ai làm gì):
  ```
  Văn bản gốc → AI tạo bản nháp → Người đánh giá chỉnh sửa → Biên tập viên cấp cao duyệt → Xuất bản
  ```
- **Tạo vòng phản hồi**: Người đánh giá phải ghi lại mọi chỉnh sửa họ thực hiện, kèm phân loại lỗi. Dữ liệu này giúp cải thiện prompt và bảng thuật ngữ trong tương lai.
- **Quản lý phiên bản bảng thuật ngữ**: Mỗi khi một thuật ngữ thay đổi, ghi lại ai thay đổi, khi nào và lý do.
- **Thiết lập quy trình phân xử phong cách**: Ai có tiếng nói cuối cùng khi nhóm không đồng ý về một lựa chọn dịch thuật?

---

## 📅 Thứ Tự Ưu Tiên Đề Xuất

| Ưu tiên | Nhiệm vụ | Người phụ trách |
|---------|---------|----------------|
| 🔴 Trước tiên | Bảng thuật ngữ chính (200 thuật ngữ đầu tiên) | Dịch giả cấp cao |
| 🔴 Trước tiên | Hướng dẫn phong cách từ ngữ liệu tác giả | Biên tập viên |
| 🟠 Tiếp theo | Kho ngữ liệu song ngữ (500+ cặp) | Toàn nhóm |
| 🟠 Tiếp theo | Soạn thảo prompt hệ thống | Biên tập viên + Trưởng dự án |
| 🟡 Sau đó | Tiêu chí QA + bản dịch tiêu chuẩn vàng | Dịch giả cấp cao |
| 🟡 Sau đó | Tài liệu hoá quy trình làm việc | Trưởng dự án |
