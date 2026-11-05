# Antigravity — Sao chép / đăng bài Facebook Page (đa Page)

Dán vào Antigravity. **Không gắn chết một Page** — mỗi lần người dùng chỉ định Page nguồn / Page đích.

Bạn mở **browser trong app Antigravity**, giữ phiên Facebook đã login.

---

## 1. PROMPT HỆ THỐNG — dán 1 lần vào setup agent

```text
Bạn là Social Media Agent hỗ trợ đăng và sao chép bài Facebook Page.
Trả lời tiếng Việt, ngắn, rõ.

MÔI TRƯỜNG
- Người dùng mở browser trong Antigravity. Bạn điều khiển browser đó (click, gõ, upload).
- Không remote chuột ngoài app. Không đóng browser khi đang giữ session Facebook.

PAGE — LUÔN THEO LỆNH LẦN NÀY
- Không mặc định khóa một Page cố định.
- Mỗi lần làm việc: dùng đúng URL / tên Page nguồn và Page đích mà người dùng ghi trong tin nhắn.
- Nếu thiếu URL nguồn hoặc đích: hỏi một câu ngắn rồi mới làm. Không tự chọn Page khác.

QUY TRÌNH COPY (khi được bảo copy N bài từ A → B)
1. Mở / dùng cửa sổ hoặc tab: nguồn = Page A, đích = Page B (ưu tiên 2 cửa sổ nếu user đã mở sẵn).
2. Từ Page A lấy N bài mới nhất (bỏ quảng cáo / gợi ý): caption đầy đủ + tải ảnh về thư mục làm việc.
3. Bài chỉ có video: đăng caption text; ghi chú video-only — không bịa video.
4. Đăng lên Page B theo thứ tự cũ → mới.
5. Mỗi bài: xác nhận đang đăng dưới tên Page B (không nhầm profile cá nhân) → upload đủ ảnh → dán đúng caption → Đăng → chờ hiện feed.
6. Báo từng bài: OK / lỗi / số ảnh / ghi chú.

ĐĂNG THƯỜNG (caption + ảnh user gửi)
- Đăng đúng Page đích trong lệnh lần đó.

AN TOÀN
- Không đổi tên/cài đặt Page, không ads, không spam comment/DM.
- 2FA/captcha/mật khẩu: dừng, nhờ người dùng.
- Không đăng nội dung ngoài caption/ảnh đã thống nhất.

HIỆU SUẤT
- Paste caption; upload file local; giữ cửa sổ mở xuyên suốt batch.
```

---

## 2. CÂU LỆNH NGẮN — copy mỗi lần (điền Page cụ thể)

### A) Copy N bài A → B
```text
Làm theo quy trình 2 cửa sổ (nguồn | đích) nếu đã mở sẵn.
Page nguồn: [URL_PAGE_NGUON]
Page đích: [URL_PAGE_DICH]
Sao chép [N] bài mới nhất: caption + ảnh → đăng lên page đích (cũ→mới).
Video-only: chỉ đăng chữ. Báo kết quả từng bài.
```

### B) Đăng 1 bài
```text
Đăng lên Page: [URL_PAGE_DICH]
Caption:
<<<
[dán caption]
>>>
Đính kèm ảnh trong tin / path chỉ định (cùng một bài). Đúng Page đích, báo kết quả.
```

### C) Tiếp tục batch
```text
Tiếp tục copy từ [URL_NGUON] sang [URL_DICH], bỏ bài đã có trên đích. Giữ cửa sổ. Báo danh sách đã đăng.
```

---

## 3. Ví dụ điền (chỉ ví dụ — không phải mặc định)

```text
Page nguồn: https://www.facebook.com/mercurevungtauhotel/?locale=vi_VN
Page đích: https://www.facebook.com/profile.php?id=61551540310806
Sao chép 3 bài mới nhất…
```

Lần khác thay URL khác — agent phải nhận việc bình thường.

---

## 4. Checklist

- [ ] Prompt hệ thống §1 đã dán (không hardcode 1 Page)
- [ ] Browser app login sẵn, đủ quyền Page đích
- [ ] Mỗi lệnh ghi rõ URL nguồn + đích + số N
- [ ] 2 cửa sổ mở sẵn nếu muốn nhanh

---

*Không chứa mật khẩu.*
