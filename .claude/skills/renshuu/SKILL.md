---
name: renshuu
description: Luyện ngữ pháp tiếng Nhật N3→N2 bằng bài tập điền chỗ trống (助詞, chia thể, 自動詞・他動詞, collocation...) có gợi ý, thay vì tự đặt câu từ đầu. Note lại lỗi vào RENSHUU_PROGRESS.md (tách riêng với PROGRESS.md của /kaiwa để dễ theo dõi từng hình thức luyện). Gọi "/renshuu" để bắt đầu, có thể kèm trụ cột muốn luyện (vd "/renshuu 助詞", "/renshuu chia thể"), hoặc "/renshuu progress" để xem lại.
---

# Renshuu — Luyện điền chỗ trống có hướng dẫn

Mục tiêu: khác với `/kaiwa` (hội thoại tự do, phải tự nghĩ câu từ đầu — dễ chán/bí ý với người mới), skill này cho người dùng **câu có sẵn với chỗ trống**, kèm gợi ý, để họ chủ động suy nghĩ và điền vào đúng điểm ngữ pháp đang luyện. Học chủ động nhưng có khung đỡ.

Dùng chung khung **12 trụ cột** với skill `kaiwa` (xem `.claude/skills/kaiwa/SKILL.md` nếu cần đối chiếu bảng đầy đủ), nhưng **log riêng vào `RENSHUU_PROGRESS.md`** (khác với `PROGRESS.md` của `/kaiwa`) — để hai hình thức luyện (hội thoại tự do vs. điền chỗ trống có hướng dẫn) theo dõi tiến độ tách biệt, dễ so sánh mình đang mạnh/yếu ở đâu theo từng cách học.

## 12 trụ cột (rút gọn — tham khảo bảng đầy đủ trong kaiwa/SKILL.md)

1. 助詞 (trợ từ: は/が/を/に/で...) 2. 自動詞・他動詞 3. Chia thể động từ (て/ない/た/可能/受身/使役/使役受身/条件/意向形) 4. Collocation 5. Chunks/mẫu câu cố định 6. 敬語 & mức lịch sự 7. 省略 8. Văn nói/khẩu ngữ 9. 副詞 10. Filler 11. Liên từ nối câu 12. Mức độ chắc chắn

Trụ cột 1-3 (助詞, 自動詞・他動詞, chia thể) là dễ ra bài điền chỗ trống rõ ràng nhất (có đáp án đúng/sai rõ). Trụ cột 4-6, 9, 11-12 cũng làm được nhưng nên cho 2-3 lựa chọn hoặc ngữ cảnh rõ để không quá mơ hồ. Trụ cột 8, 10 phù hợp hơn với `/kaiwa` (cần ngữ cảnh hội thoại thật) — nếu luyện ở đây thì cho dạng "câu trang trọng → viết lại kiểu khẩu ngữ".

## Cách chạy

1. **Chọn trụ cột luyện hôm nay:**
   - Nếu người dùng đã nêu rõ trong args (tên trụ cột hoặc số 1-12), dùng luôn.
   - Nếu không, đọc `RENSHUU_PROGRESS.md` (nếu có) ở gốc project — chỉ file này, không đọc `PROGRESS.md` của `/kaiwa` — xem trụ cột nào xuất hiện nhiều nhất trong các lỗi đã note gần đây → đề xuất ngắn gọn 1-2 trụ cột đó cho người dùng xác nhận (không hỏi dài dòng). Nếu chưa có `RENSHUU_PROGRESS.md` hoặc chưa đủ dữ liệu, hỏi người dùng muốn luyện trụ cột nào (liệt kê ngắn gọn vài lựa chọn tiêu biểu).
   - Có thể luyện 1 trụ cột xuyên suốt buổi, hoặc mix 2-3 trụ cột liên quan (vd 助詞 + chia thể) nếu người dùng muốn.

2. **Ra đề từng câu một** (không dồn nhiều câu một lúc — chờ người dùng trả lời câu này rồi mới ra câu tiếp):
   - Đưa 1 câu tiếng Nhật có 1 (hoặc tối đa 2) chỗ trống `＿＿＿`, kèm:
     - Ngữ cảnh/tình huống ngắn bằng tiếng Việt nếu câu có thể hiểu nhiều nghĩa.
     - Gợi ý cần thiết: với chia thể — cho động từ ở dạng từ điển + tên thể cần chia (vd "書く → điền thể ない"); với trợ từ — có thể cho 2-3 lựa chọn (は/が/を) để người dùng chọn thay vì đoán mù; với collocation — cho nghĩa tiếng Việt của cụm cần ghép.
     - Độ khó tăng dần trong buổi: câu đơn giản trước, câu phức/nhiều trụ cột trộn lẫn sau.
   - Với trụ cột thiên về sắc thái (collocation, mức độ chắc chắn, 敬語...), có thể hỏi dạng "chọn câu tự nhiên hơn giữa A và B" thay vì điền chỗ trống thuần túy.

3. **Sau khi người dùng trả lời:**
   - Nhận xét đúng/sai ngay, giải thích ngắn gọn TẠI SAO (quy tắc/cảm giác đằng sau, không chỉ nói "sai").
   - Cho đáp án đầy đủ + cách đọc (furigana/romaji cho từ khó) + nghĩa tiếng Việt.
   - **Nếu người dùng trả lời sai hoặc phải gợi ý mới ra** — ghi ngay vào `RENSHUU_PROGRESS.md` ở gốc project (Edit/Write ngay lập tức, không đợi cuối buổi; **không** ghi vào `PROGRESS.md` của `/kaiwa`), theo bảng: cột **Trụ cột / Câu gốc / Câu hay hơn / Cách đọc / Nghĩa** — ở đây "Câu gốc" là câu có chỗ trống + câu người dùng điền, "Câu hay hơn" là đáp án đúng:
     - Đọc `RENSHUU_PROGRESS.md` hiện tại nếu đây là lần ghi đầu tiên trong buổi. Nếu file chưa tồn tại, tạo mới theo template ở cuối file này (cấu trúc giống `kaiwa/SKILL.md` nhưng dùng tên file/tiêu đề riêng cho renshuu).
     - Thêm vào mục ngày hôm nay (tạo mới nếu chưa có ở đầu "## Log"), chủ đề ghi là tên trụ cột đang luyện (vd "### 2026-09-10 — 助詞").
   - Nếu người dùng trả lời đúng ngay không cần gợi ý thêm — không cần note lại, chuyển câu tiếp.

4. Tiếp tục ra câu mới, thỉnh thoảng lặp lại (spaced repetition nhẹ) điểm vừa sai ở dạng câu khác để kiểm tra đã hiểu thật chưa. Không giới hạn số câu cứng nhắc — luyện đến khi người dùng muốn dừng.

5. Kết thúc buổi khi người dùng báo dừng — không cần thêm tổng kết/tự đánh giá, chỉ cần bảng note đã ghi trong `RENSHUU_PROGRESS.md`.

## Chế độ xem lại note (khi args chứa "progress" hoặc người dùng muốn xem lại các câu đã note)

1. Đọc toàn bộ `RENSHUU_PROGRESS.md` (chỉ file này — tiến độ luyện hội thoại tự do xem bằng `/kaiwa progress` riêng).
2. Hiển thị lại danh sách các điểm đã note, gom theo **Trụ cột** để thấy rõ đang yếu nhất ở đâu (trụ cột lặp lại nhiều = ưu tiên luyện tiếp buổi sau); trong mỗi trụ cột có thể gom thêm theo mẫu câu/quy tắc lặp lại.
3. Không cần sửa file trong chế độ này, chỉ đọc và hiển thị lại.

## Template RENSHUU_PROGRESS.md (dùng khi tạo file mới)

```markdown
# Renshuu Progress Log (N3 → N2)

Note lại các điểm đã sai/cần gợi ý khi luyện điền chỗ trống. Mục mới nhất ở trên cùng.

## Log

<!-- các mục theo ngày sẽ được thêm vào đây -->
```

Mỗi mục ngày dùng format bảng:

```markdown
### YYYY-MM-DD — <trụ cột>

| Trụ cột | Câu gốc | Câu hay hơn | Cách đọc | Nghĩa |
|---|---|---|---|---|
| ... | ... | ... | ... | ... |
```

Nếu luyện nhiều buổi trong cùng một ngày, thêm dòng mới vào bảng của mục ngày đó (không tạo mục ngày trùng lặp).
