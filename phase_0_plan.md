# Kế Hoạch Chi Tiết — Giai Đoạn 0 (Tháng 1–3)
## Dự án: Từ Điển Triết Học Việt — Nền Tảng Dịch Thuật Thống Nhất

> **Mục tiêu giai đoạn này:** Xây dựng ba trụ cột nền tảng trước khi dịch bất kỳ tác phẩm lớn nào — (1) bộ mẫu văn phong, (2) bảng thuật ngữ cốt lõi, và (3) quy trình dịch có hỗ trợ AI. Kết thúc giai đoạn này, nhóm phải có thể dịch một đoạn triết học nhất quán về giọng văn và thuật ngữ.

---

## Tuần 1–2: Thành Lập Ban Biên Tập & Xác Định Giọng Văn Để Huấn Luyện AI

### Công việc

**1. Thành lập Ban Biên Tập (Editorial Board)**
- Mời 3–5 thành viên sáng lập: ưu tiên triết gia học thuật, nghiên cứu sinh tiến sĩ, hoặc dịch giả có kinh nghiệm với văn bản triết học
- Phân công trách nhiệm theo chuyên ngành:
  - Triết học phương Tây (phân tích & lục địa)
  - Triết học phương Đông & Phật giáo
  - Triết học chính trị & đạo đức
- Xác định người giữ quyết định cuối cùng khi có tranh luận thuật ngữ (Chief Editor)

**2. Chọn "Văn Bản Chuẩn" (Touchstone Text)**

Đây là bước quan trọng nhất của cả giai đoạn. Ban Biên Tập cần chọn **một đoạn văn ngắn** (khoảng 500–1.000 từ tiếng Việt) làm mẫu giọng văn tuyệt đối. Đoạn này sẽ là thước đo cho mọi bản dịch sau này.

Tiêu chí chọn hoặc viết đoạn văn chuẩn:
- Viết bằng tiếng Việt hiện đại, rõ ràng, tránh Hán-Việt nặng nề
- Câu ngắn đến trung bình, không dịch sát theo cú pháp tiếng Anh/Đức
- Có ít nhất 5–10 thuật ngữ triết học xuất hiện tự nhiên trong ngữ cảnh
- Đọc được với sinh viên đại học năm 3, không cần là chuyên gia

> **Gợi ý:** Chief Editor viết lại một đoạn quen thuộc (ví dụ: đoạn mở đầu *Cộng Hòa* của Plato) theo đúng giọng mong muốn. Toàn ban đọc, thảo luận, và chỉnh cho đến khi đồng thuận. Đoạn văn được chấp thuận chính là định nghĩa sống của "giọng văn thống nhất".

---

## Tuần 3–6: Xây Dựng Bảng Thuật Ngữ Cốt Lõi v1.0

### Mục tiêu: 300–500 thuật ngữ được phê duyệt chính thức

### Quy trình

**Bước 1 — AI trích xuất danh sách thuật ngữ ứng viên (~3–5 ngày)**

Thay vì để một nghiên cứu viên đọc thủ công, dùng AI để quét và trích xuất thuật ngữ từ các nguồn sau:

| Nguồn cấp cho AI | Mục đích |
|---|---|
| Stanford Encyclopedia of Philosophy (SEP) | AI trích xuất thuật ngữ kỹ thuật + định nghĩa tiếng Anh chuẩn |
| Wikipedia tiếng Việt (chuyên mục triết học) | AI liệt kê các phiên bản tiếng Việt đang dùng phổ biến |
| *Từ điển Triết học* (NXB Sự Thật) | AI trích baseline lịch sử để so sánh |
| Giáo trình triết học đại học hiện hành | AI xác định từ nào đang được dạy chính thống |

Prompt mẫu gửi AI cho mỗi nguồn:
```
Từ đoạn văn bản sau, hãy liệt kê tất cả thuật ngữ triết học, những từ chưa phổ biến, hoặc những từ chưa có trong tiếng Việt.
Với mỗi thuật ngữ, cho biết: (1) từ tiếng Anh gốc, (2) các phiên bản
tiếng Việt hiện đang dùng, (3) ngữ cảnh xuất hiện.
Kết quả trả về dạng bảng.
[Dán văn bản nguồn vào đây]
```

Kết quả: Một file Excel thô với cột: `Từ tiếng Anh | Các lựa chọn tiếng Việt hiện tại | Nguồn | Ghi chú AI`

**Bước 2 — Ban Biên Tập thẩm định và bỏ phiếu (~1–2 tuần)**

Mỗi chuyên gia phụ trách phân ngành của mình. Với mỗi thuật ngữ AI đề xuất:
1. **Chấp thuận** — dùng đúng như AI đề xuất
2. **Chỉnh sửa** — giữ thuật ngữ nhưng thay đổi phiên bản tiếng Việt
3. **Loại bỏ** — thuật ngữ không đủ quan trọng hoặc AI trích xuất sai
4. **Ghi lý do quyết định** — bắt buộc, dù chỉ một câu — đây là tư liệu quan trọng cho người dùng sau này

> **Lưu ý:** AI sẽ trích ra nhiều hơn cần thiết — đó là điều tốt. Vai trò của Ban Biên Tập là lọc và quyết định, không phải tìm kiếm từ đầu.

**Bước 3 — Ghi lại thành Bảng Thuật Ngữ Chính thức**

Mỗi mục trong bảng gồm:
```
- Thuật ngữ tiếng Anh: epistemology
- Thuật ngữ chính thức: nhận thức luận
- Định nghĩa ngắn (tiếng Việt): Ngành triết học nghiên cứu bản chất, nguồn gốc và giới hạn của tri thức
- Ghi chú dịch: Ưu tiên "nhận thức luận" thay vì "tri thức luận" vì tính phổ biến học thuật cao hơn
- Từ đồng nghĩa/biến thể cần tránh: tri thức học, nhận thức học
```

### Danh mục ưu tiên 10 nhóm thuật ngữ cần có ngay

1. Siêu hình học (metaphysics, ontology, being, substance...)
2. Nhận thức luận (knowledge, belief, truth, justification...)
3. Logic học (inference, deduction, induction, contradiction...)
4. Đạo đức học (virtue, duty, consequentialism, autonomy...)
5. Triết học chính trị (justice, liberty, sovereignty, social contract...)
6. Hiện tượng học (consciousness, intentionality, phenomenology...)
7. Triết học phân tích (proposition, reference, meaning, language...)
8. Triết học Phật giáo (dharma, nirvana, karma, śūnyatā...)
9. Triết học Nho giáo (ren, li, dao, de...)
10. Thuật ngữ lịch sử triết học (Logos, Eidos, Dasein, dialectic...)

---

## Tuần 5–8: Thiết Lập Quy Trình Dịch Bán Tự Động (Semi-Translating)

### Nguyên lý hoạt động

Thay vì dịch toàn bộ thủ công, nhóm áp dụng vòng lặp sau:

```
[Đoạn tiếng Anh] + [Văn bản chuẩn làm mẫu] + [Bảng thuật ngữ]
        ↓
    AI tạo bản nháp
        ↓
  Dịch giả hiệu đính
        ↓
  Bản được phê duyệt → lưu vào kho ngữ liệu
        ↓
  Bản phê duyệt mới được thêm vào mẫu cho lần dịch tiếp theo
```

### Thiết kế Prompt — Hai Lớp (Google Gemini Gems / Claude Projects)

Thay vì dịch giả phải dán lại toàn bộ prompt mỗi lần, prompt được tách thành **hai lớp**:

---

**Lớp 1 — System Prompt (cài đặt một lần bởi Kỹ thuật viên AI)**

Phần này được lưu cố định trong Gemini Gem hoặc Claude Project. Dịch giả không bao giờ phải chạm vào nó.

```
BẠN LÀ DỊCH GIẢ TRIẾT HỌC TIẾNG VIỆT.

BẢNG THUẬT NGỮ:
File Excel/PDF đính kèm trong cuộc trò chuyện này là Bảng Thuật Ngữ chính thức.
Hãy đọc file đó trước. Mọi thuật ngữ triết học trong bản dịch PHẢI dùng đúng từ trong file này.
Nếu một thuật ngữ không có trong file, hãy giữ nguyên tiếng Anh và ghi chú "(chưa có trong bảng thuật ngữ)".

QUY TẮC GIỌNG VĂN (bắt buộc tuân theo):
- Tiếng Việt hiện đại, rõ ràng, câu ngắn đến trung bình
- Không dịch sát cú pháp tiếng Anh — ưu tiên ý nghĩa tự nhiên
- Lần xuất hiện đầu tiên của thuật ngữ: thêm nguyên bản tiếng Anh trong ngoặc đơn

VĂN BẢN CHUẨN (Touchstone Text — đây là giọng văn bạn cần đạt được):
[Kỹ thuật viên AI dán Touchstone Text đã được phê duyệt vào đây]
```

---

**Lớp 2 — Input của Dịch Giả (mỗi lần dịch)**

Dịch giả chỉ cần gửi đúng hai thứ sau, không cần thêm gì:

```
MẪU DỊCH ĐÃ DUYỆT GẦN NHẤT (2–3 đoạn):
[Dán 2–3 đoạn đã được phê duyệt gần nhất từ kho ngữ liệu]

ĐOẠN CẦN DỊCH:
[Dán đoạn tiếng Anh cần dịch vào đây]
```

---

**Xử lý Bảng Thuật Ngữ (Glossary):**

Đầu mỗi phiên làm việc, dịch giả đính kèm file Excel/PDF của Bảng Thuật Ngữ mới nhất vào cuộc trò chuyện (Gemini và Claude đều hỗ trợ đính kèm file). Kỹ thuật viên AI export file này định kỳ (hàng tuần hoặc mỗi khi có cập nhật lớn).

> **Lợi ích:** Dịch giả không cần biết prompt hoạt động như thế nào. Họ chỉ cần: (1) mở Gem/Project, (2) đính kèm file glossary mới nhất, (3) dán đoạn cần dịch và gửi.

### Quy mô đoạn dịch khuyến nghị

Kích thước đoạn dịch nên tăng dần theo quy mô kho ngữ liệu đã được phê duyệt — không cố định:

| Kho ngữ liệu đã duyệt | Kích thước đoạn khuyến nghị | Lý do |
|---|---|---|
| **0–20.000 từ** (Phase 0 ban đầu) | 200–400 từ | AI có ít mẫu; đoạn ngắn hạn chế phạm vi lỗi giọng văn |
| **20.000–100.000 từ** | 400–800 từ | AI đủ mẫu để giữ giọng văn ổn định hơn; dịch giả hiệu đính ít hơn |
| **Trên 100.000 từ** | 800–1.500 từ | Có thể dịch trọn một đoạn lập luận trong một lần |
| **Mô hình fine-tuned** (tương lai) | Cả chương | Lỗi giọng văn hiếm; kiểm soát chất lượng ở cấp độ chương |

> **Tín hiệu để tăng kích thước:** Không tăng theo lịch — tăng khi dịch giả xác nhận AI liên tục đạt giọng văn đúng trong 10–15 đoạn liên tiếp gần nhất mà không cần sửa lớn.

**Ngoại lệ — Văn bản đối thoại (như *Cộng Hòa* của Plato):** Chia đoạn theo **lượt thoại của nhân vật**, không theo số từ — dù kho ngữ liệu đã lớn đến đâu. Cắt giữa lượt thoại khiến AI mất mạch lập luận triết học.

- Không dịch theo câu đơn lẻ — dễ mất mạch lập luận triết học

---

## Tuần 7–12: Dịch Thử Nghiệm — Văn Bản Nền Tảng Đầu Tiên

### Mục tiêu: 3 tác phẩm ngắn hoặc đoạn trích dài, hoàn toàn được phê duyệt

### Danh sách đề xuất cho Phase 0

| Tác phẩm | Lý do ưu tiên |
|---|---|
| Plato — The Republic (Cộng Hoà) | Ngắn (~10.000 từ), văn xuôi đối thoại, dễ đọc, quen thuộc |
| Descartes — *Meditations I & II* | Ngắn, câu văn rõ ràng, kinh điển nhập môn |
| Aristotle — trích đoạn *Nicomachean Ethics* (quyển I) | Đạo đức học — thuật ngữ thực tế, liên quan đời sống |
| Wittgenstein — *Tractatus Logico-Philosophicus* hoặc *Philosophical Investigations* | Có chuyên gia dịch thuật |

### Vai trò của dịch giả trong giai đoạn này

| Nhiệm vụ | Mô tả |
|---|---|
| **Hiệu đính giọng văn** | Đọc bản nháp AI và đảm bảo đọc như văn Việt viết, không phải văn dịch |
| **Kiểm tra thuật ngữ** | Mọi thuật ngữ phải khớp với Bảng Thuật Ngữ chính thức |
| **Ghi chú bất đồng** | Nếu thấy thuật ngữ trong bảng chưa phù hợp → đề xuất sửa bảng, không tự ý dùng từ khác |
| **Phê duyệt & lưu trữ** | Bản được duyệt lưu vào kho ngữ liệu với metadata đầy đủ |

---

## Tiêu Chí Hoàn Thành Giai Đoạn 0

Giai đoạn 0 kết thúc khi **tất cả** các mục sau được đánh dấu hoàn thành:

- [ ] Ban Biên Tập thành lập với ít nhất 3 thành viên chính thức
- [ ] Văn bản chuẩn (Touchstone Text) được toàn ban thống nhất bằng văn bản
- [ ] Bảng Thuật Ngữ v1.0 có ít nhất 300 mục được phê duyệt
- [ ] Prompt chuẩn cho AI được kiểm thử và tinh chỉnh qua ít nhất 50 đoạn thử nghiệm
- [ ] Ít nhất 1 tác phẩm ngắn được dịch hoàn chỉnh và phê duyệt toàn bộ
- [ ] Kho ngữ liệu nền tảng đạt ít nhất 20.000 từ tiếng Việt đã phê duyệt

---

## Phân Công & Nguồn Lực Gợi Ý

| Vai trò | Số lượng | Thời gian cam kết | Công việc chính |
|---|---|---|---|
| Chief Editor | 1 | Toàn thời gian hoặc 50% | Viết Touchstone Text, quyết định thuật ngữ tranh cãi, QC cuối |
| Triết gia chuyên ngành | 2–4 | Bán thời gian (~10h/tuần) | Thẩm định và bỏ phiếu danh sách thuật ngữ do AI đề xuất |
| Dịch giả hiệu đính | 1–2 | Bán thời gian | Hiệu đính bản nháp dịch AI theo đoạn |
| Kỹ thuật viên AI | 1 | Bán thời gian | Vận hành pipeline trích xuất thuật ngữ và pipeline dịch |

> **So với phương án thủ công:** Việc dùng AI trích xuất thuật ngữ thay thế hoàn toàn vai trò nghiên cứu viên toàn thời gian, tiết kiệm ~2–3 tuần nhân công trong Bước 1. Thời gian Ban Biên Tập tập trung vào phán quyết, không phải thu thập.

---

*Tài liệu này là nội bộ dành cho nhóm dịch. Phiên bản: 1.0 — Tháng 3/2026.*
