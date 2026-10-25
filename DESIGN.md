# DESIGN.md — Landing page tiệm socola thủ công Đắng Ngọt

> Tài liệu thiết kế chốt cho sprint TEC-383 (task Thiết kế TEC-384). Dev (task Dev của sprint) dựng đúng tài liệu này, không tự thêm màu, font hay khối ngoài danh sách. QA đối chiếu bản dựng với tài liệu này, kèm kiểm tra đa dạng theo OPERATIONS.md mục 16.5.

## 0. Khác biệt so với các project gần nhất (bắt buộc theo mục 16.5 — đã đọc thật ngày 2026-10-25)

Thứ tự project mới nhất lấy từ https://msoft.genalpha.dev/api/office, DESIGN.md đọc trực tiếp qua raw.githubusercontent.com ngày 2026-10-25 (repo tarotlight-app là private nên trả 404 qua đường public; nội dung của nó lấy theo DESIGN.md đã ghi trong hồ sơ Kim Ngọc TEC-371, trong đó app này tự ghi là không có archetype bố cục web):

| Project (mới → cũ) | Archetype | Cặp font | Nhiệt màu |
|---|---|---|---|
| Kim Ngọc (m-software-kim-ngoc, TEC-371) | A2 Split | Noto Serif Display + Manrope | Tối-ấm (nền `#141210`) |
| TarotLight (tarotlight-app, TEC-352) | Không có archetype web (app mobile Flutter, tự ghi "BỎ QUA luật đa dạng archetype") | Cormorant Garamond + (nội dung) | Tối (nền tím đêm `#120E24`) |
| Bánh Lăn (m-software-banh-lan, TEC-347) | A6 Thanh bên cố định | Fraunces + Be Vietnam Pro | Sáng-ấm (nền `#ECEAE4`) |

Lựa chọn cho Đắng Ngọt và lý do không vi phạm luật chống trùng (§16.5):

- **Archetype: A5 Theo chương** — KHÁC A2 của Kim Ngọc (project web liền trước) và KHÁC A6 của Bánh Lăn (project web liền trước nữa); TarotLight không có archetype web nên không tính trùng. Cách A5 thể hiện ở: toàn trang chia thành các chương đánh số ("Chương 1 — Câu chuyện", "Chương 2 — Bộ sưu tập", "Chương 3 — Quy trình", "Chương 4 — Bảng giá", "Chương 5 — Đặt hàng"), mỗi chương mở đầu bằng khối tiêu đề chương + vạch chia hình thanh socola (xem mục "Điểm nhấn đặc sắc"), không phải chia đôi màn hình xen kẽ trái/phải (A2), không phải thanh bên cố định (A6).
- **Cặp font: Fraunces + Be Vietnam Pro** — KHÁC nguyên cặp Noto Serif Display + Manrope của project liền trước (Kim Ngọc): cả font tiêu đề lẫn font nội dung đều khác. Cặp này trùng với Bánh Lăn nhưng luật §16.5 chỉ cấm lặp nguyên cặp của project liền trước, nên không vi phạm; giữ cặp này vì đúng tinh thần công thức gợi ý trong yêu cầu (serif cổ điển cho atelier socola).
- **Nhiệt màu: SÁNG-ẤM — LÝ DO ĐỔI (bắt buộc theo luật chống trùng):** công thức gợi ý trong yêu cầu đặt nền chính tối `#201812`. Nếu giữ nền tối, chuỗi nhiệt màu sẽ là Đắng Ngọt (tối) → Kim Ngọc (tối-ấm) → TarotLight (tối): 3 project liên tiếp cùng họ tối, vi phạm "tránh 3 project liên tiếp cùng một nhiệt màu chủ đạo". Vì vậy ĐẢO VAI TRÒ của 2 màu gợi ý, giữ nguyên bảng màu và không khí: nền chính thành kem sáng `#F3E9D7` (vốn là màu chữ gợi ý), chữ chính thành nâu socola đậm `#201812` (vốn là màu nền gợi ý), nhấn vàng đồng `#D9A441` giữ nguyên. Hero vẫn là ảnh toàn màn hình tối (thợ rót socola lỏng, nền ảnh tối) nên không khí atelier tối-ấm vẫn hiện diện ngay đầu trang; toàn bộ các chương nội dung phía dưới dùng nền kem sáng, vì vậy nhiệt màu chủ đạo của trang là sáng-ấm. Chuỗi sau khi đổi: Đắng Ngọt (sáng-ấm) → Kim Ngọc (tối-ấm) → TarotLight (tối): không có 3 project liên tiếp cùng nhiệt màu.
- **Điểm nhấn riêng** (xem mục "Điểm nhấn đặc sắc"): vạch chia chương hình thanh socola tan chảy + nhãn "nốt vị" trên từng dòng socola — không project nào gần đây có.

## Tổng quan

- Sản phẩm: landing page 1 trang, visual-first, cho tiệm socola thủ công Đắng Ngọt — làm socola từ hạt cacao, bán theo dòng và nhận đặt hàng/tham quan xưởng.
- Archetype: **A5 Theo chương** — trang đọc như một cuốn sách nhỏ về socola: mỗi chương một chủ đề, đánh số chương bằng số La Mã kèm tên chương, chuyển chương bằng vạch chia hình thanh socola.
- Phong cách tham chiếu: **atelier socola Bỉ cổ điển** — quầy gỗ tối, khay đồng, giấy gói kem, chữ serif cổ điển, ánh sáng ấm vàng, chụp cận cảnh macro socola tan chảy.
- Ngôn ngữ: tiếng Việt, hỗ trợ dấu đầy đủ (cả Fraunces và Be Vietnam Pro đều hỗ trợ tiếng Việt).

## Bảng màu (mã hex + vai trò)

| Mã hex | Vai trò |
|---|---|
| `#F3E9D7` | Nền chính toàn trang — kem giấy gói socola, sáng và ấm |
| `#E4D9C6` | Nền khối phụ (chương xen kẽ, thẻ bảng giá) — kem đậm hơn nền chính một nấc |
| `#201812` | Chữ chính + tiêu đề chương — nâu socola đen, đọc rõ trên nền kem |
| `#3B2416` | Nền khối nhấn (chân chương quy trình, chân trang) — nâu socola đậm, dùng ít, không làm nền toàn trang |
| `#6B4E35` | Chữ phụ, mô tả, chú thích ảnh — nâu cacao nhạt, chỉ dùng cho chữ nhỏ, không dùng làm chữ chính |
| `#D9A441` | Nhấn chính — vàng đồng: số chương, vạch chia thanh socola, nút chính, giá nổi bật |
| `#FFFFFF` | Nền thẻ ảnh khi ảnh cần viền sáng (chỉ dùng trong thẻ bộ sưu tập, không dùng làm nền trang) |

Quy tắc dùng màu: tối đa 2 màu nền trong một chương (kem chính + kem đậm xen kẽ); màu `#3B2416` chỉ xuất hiện ở tối đa 2 khối nhấn; nút chính luôn nền `#D9A441` chữ `#201812`; không dùng thêm màu ngoài bảng.

## Typography

- Font tiêu đề: **Fraunces** (serif, nét đậm, có chân cổ điển) — tên tiệm ở hero 64px desktop / 40px mobile; tiêu đề chương 40px desktop / 28px mobile; tên dòng socola 24px.
- Font nội dung: **Be Vietnam Pro** — thân bài 17px, dòng cách 1,6; chú thích ảnh và nhãn "nốt vị" 13px, chữ hoa toàn bộ (uppercase), giãn cách chữ 0,08em.
- Tiêu đề chương luôn gồm 3 dòng theo thứ tự: số chương bằng số La Mã màu `#D9A441` (ví dụ "CHƯƠNG II"), tên chương bằng Fraunces, một câu dẫn ngắn bằng Be Vietnam Pro màu `#6B4E35`.

## Bố cục (A5 Theo chương)

Thứ tự chương, không đổi thứ tự, không thêm khối ngoài danh sách:

1. **Hero (không đánh số chương)** — ảnh toàn màn hình thợ rót socola lỏng; tên tiệm "Đắng Ngọt" + câu định vị một dòng + 1 nút chính "Xem bộ sưu tập" (cuộn xuống Chương 2).
2. **Chương I — Câu chuyện** — chữ kể chuyện hạt cacao và người thợ, kèm 1 ảnh lớn người thợ làm socola; chữ chiếm tối đa 60% chiều rộng khối, không dàn 2 cột.
3. **Chương II — Bộ sưu tập** — mỗi dòng socola một thẻ ảnh lớn, xếp dọc từng thẻ (không xếp lưới nhiều cột kiểu tạp chí, không chia đôi trái/phải cố định); mỗi thẻ gồm ảnh, tên dòng, nhãn "nốt vị", giá mẫu.
4. **Chương III — Quy trình** — đúng 4 bước từ hạt cacao tới thanh socola, xếp ngang 4 ô trên desktop, xếp dọc trên mobile; mỗi ô gồm số bước, tên bước, mô tả 1–2 câu.
5. **Chương IV — Bảng giá** — bảng giá mẫu, mỗi dòng gồm tên dòng socola + trọng lượng + giá; giá là giá mẫu, ghi chú rõ "Giá mẫu" ngay dưới tiêu đề chương.
6. **Chương V — Đặt hàng / Tham quan** — form chỉ giao diện (không gửi thật): họ tên, số điện thoại, chọn loại yêu cầu (đặt hàng / tham quan xưởng), ghi chú; nút "Gửi yêu cầu" chỉ hiển thị, không có xử lý gửi.
7. **Chân trang** — tên tiệm, câu slogan một dòng, ghi chú "Trang demo — giá và form chỉ là mẫu".

Chuyển chương: giữa hai chương đặt vạch chia hình thanh socola (xem mục "Điểm nhấn đặc sắc"); không dùng thanh bên cố định, không dùng lưới bento.

## Điểm nhấn đặc sắc

1. **Vạch chia chương hình thanh socola tan chảy** — một hàng ngang gồm 4 ô vuông bo góc nhẹ màu `#D9A441` viền `#201812` (mô phỏng 4 miếng của một thanh socola), ô cuối cùng có mép dưới chảy giọt (hình giọt socola lỏng rủ xuống 12px). Vạch này xuất hiện ở đầu mỗi chương, ngay trên số chương; không dùng ở nơi khác.
2. **Nhãn "nốt vị"** — trên mỗi thẻ bộ sưu tập, dưới tên dòng socola, một hàng nhãn nhỏ chữ hoa (ví dụ "70% ĐẮNG · CAM KHÔ · MUỐI BIỂN") mô tả vị của dòng đó; nhãn có viền mảnh `#D9A441`, chữ `#6B4E35`, không dùng màu khác.

## Quy tắc hình ảnh

- Tông ảnh: ấm, ánh sáng vàng, nền tối hoặc gỗ tối trong ảnh; tuyệt đối không dùng ảnh ánh sáng trắng lạnh, không dùng ảnh nền trắng studio.
- Tỉ lệ khung: hero toàn màn hình 16:9 trên desktop, cắt giữa thành 4:5 trên mobile (giữ nhân vật thợ ở giữa khung); ảnh câu chuyện 3:2 ngang; ảnh từng dòng socola 4:5 dọc (ảnh lớn, chiếm gần hết chiều rộng thẻ); ảnh quy trình 1:1 vuông cho cả 4 bước.
- Nội dung ảnh: hero bắt buộc là thợ đang rót socola lỏng (dòng socola chảy nhìn thấy rõ); ảnh bộ sưu tập là cận cảnh macro từng thanh socola/viên socola, thấy rõ bề mặt và kết cấu; ảnh quy trình theo đúng bước (hạt cacao → rang/xay → rót khuôn → thành phẩm).
- Ảnh mẫu: dùng ảnh mẫu chất lượng cao, đồng tông theo quy tắc trên ngay từ bản đầu tiên; ghi rõ là ảnh mẫu trong kết quả của Dev.
- Không dùng ảnh người thật nổi tiếng, không dùng logo thương hiệu thật.

## Quy tắc responsive

- Desktop (≥1024px): nội dung chính rộng tối đa 1080px, căn giữa; quy trình 4 ô ngang.
- Mobile (<768px): một cột duy nhất; hero cắt 4:5; quy trình xếp dọc; bảng giá giữ dạng dòng (tên + giá), không ép thành bảng nhiều cột ngang gây cuộn ngang.
- Không có cuộn ngang ở bất kỳ breakpoint nào.
