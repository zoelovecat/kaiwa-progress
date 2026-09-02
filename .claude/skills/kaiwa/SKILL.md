---
name: kaiwa
description: Luyện hội thoại tiếng Nhật trình độ N2 với Claude đóng vai đối tác, tự động note lại từ vựng/câu góp ý vào PROGRESS.md. Gọi "/kaiwa" để bắt đầu buổi luyện, hoặc "/kaiwa progress" để xem lại các từ/câu đã note.
---

# Kaiwa Practice & Vocab Notes

Mục tiêu: giúp người dùng luyện hội thoại tiếng Nhật để nâng trình độ từ N3 lên N2, và note lại các góp ý (từ vựng, câu nói tự nhiên/cao cấp hơn) vào file `PROGRESS.md` ở gốc project để xem lại sau.

File log: `PROGRESS.md` (tạo mới nếu chưa có, dùng template ở cuối file này).

## Chế độ 1 — Luyện hội thoại (mặc định, khi args rỗng hoặc là chủ đề)

1. Nếu người dùng chưa nói chủ đề, hỏi ngắn gọn họ muốn luyện chủ đề gì (công việc, tin tức, phỏng vấn, du lịch, đời sống hàng ngày...). Nếu họ đã nêu chủ đề trong args, dùng luôn, không hỏi lại.
2. Đóng vai đối tác hội thoại người Nhật, trò chuyện hoàn toàn bằng tiếng Nhật ở độ khó N2 (ngữ pháp, từ vựng, kanji tương ứng N2, tốc độ tự nhiên hơn N3).
3. Trong lúc hội thoại, ngay sau **mỗi lần người dùng trả lời/viết một câu** mà có điểm đáng góp ý — dùng sai, hoặc dùng được nhưng có từ/mẫu câu tự nhiên hơn/cao cấp hơn (N2) — làm ngay, không đợi người dùng yêu cầu và không đợi đến cuối buổi:
   a. Chỉ ra ngay trong hội thoại (ngắn gọn, không phá mạch hội thoại quá nhiều).
   b. **Ghi ngay vào `PROGRESS.md`** (dùng Edit/Write ngay lập tức, không gộp lại chờ cuối buổi):
      - Đọc file `PROGRESS.md` hiện tại nếu đây là lần ghi đầu tiên trong buổi (nếu file chưa có thì tạo theo template bên dưới).
      - Nếu mục ngày hôm nay đã tồn tại ở đầu "## Log", thêm dòng mới vào bảng của mục đó. Nếu chưa có, tạo mục ngày mới ở đầu "## Log".
      - Mỗi điểm góp ý là một dòng trong bảng gồm đủ: **Câu gốc** (câu người dùng đã viết), **Câu hay hơn** (câu/từ thay thế tự nhiên/cao cấp hơn), **Cách đọc** (furigana/romaji cho từ khó đọc), **Nghĩa** (bằng tiếng Việt).
   Nếu một câu trả lời có nhiều điểm đáng góp ý, ghi mỗi điểm một dòng riêng, vẫn ghi ngay lập tức chứ không đợi gộp.
4. Chủ động gài vào hội thoại 1-2 từ vựng/mẫu ngữ pháp N2 mới mỗi buổi; nếu người dùng dùng thử và dùng đúng thì không cần note lại (chỉ note các điểm cần sửa/nâng cấp).
5. Không cần đợi người dùng báo kết thúc buổi mới ghi file — việc ghi đã xảy ra ngay sau mỗi câu trả lời có điểm góp ý (bước 3b). Khi người dùng kết thúc buổi, không cần thêm hành động ghi file nào khác; không thêm phần tự đánh giá độ trôi chảy hay gợi ý buổi sau — chỉ có bảng từ vựng/câu góp ý.

## Chế độ 2 — Xem lại note (khi args chứa "progress" hoặc người dùng muốn xem lại các từ/câu đã note)

1. Đọc toàn bộ `PROGRESS.md`.
2. Hiển thị lại danh sách các điểm đã note, có thể gom theo từ/mẫu câu lặp lại nhiều lần (dấu hiệu đây là lỗi/điểm yếu cần chú ý) để người dùng dễ ôn tập.
3. Không cần sửa file trong chế độ này, chỉ đọc và hiển thị lại.

## Template PROGRESS.md (dùng khi tạo file mới)

```markdown
# Kaiwa Vocab Notes (N3 → N2)

Note lại từ vựng/câu được góp ý khi luyện kaiwa. Mục mới nhất ở trên cùng.

## Log

<!-- các mục theo ngày sẽ được thêm vào đây -->
```

Mỗi mục ngày dùng format bảng:

```markdown
### YYYY-MM-DD — <chủ đề>

| Câu gốc | Câu hay hơn | Cách đọc | Nghĩa |
|---|---|---|---|
| ... | ... | ... | ... |
```

Nếu luyện nhiều buổi trong cùng một ngày, thêm dòng mới vào bảng của mục ngày đó (không tạo mục ngày trùng lặp).
