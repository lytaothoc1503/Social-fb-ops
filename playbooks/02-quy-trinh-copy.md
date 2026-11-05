# Quy trình copy bài Facebook Page A → Page B

## Chuẩn bị
1. Browser (Antigravity / Grok Bot / agent) đã login Facebook.
2. Tài khoản có quyền đăng **Page đích**.
3. (Khuyến nghị) 2 cửa sổ: phải = nguồn, trái = đích.

## Các bước
1. Mở Page nguồn + Page đích (đúng URL trong lệnh lần đó).
2. Lấy N bài mới nhất trên nguồn (bỏ quảng cáo / gợi ý).
3. Mỗi bài: mở đầy đủ caption (Xem thêm) + tải mọi ảnh về thư mục làm việc.
4. Bài chỉ video: ghi chú video-only; đăng **caption chữ** (không bịa video).
5. Đăng lên đích theo thứ tự **cũ → mới**.
6. Mỗi bài: xác nhận composer = tên Page đích → upload ảnh → dán caption → Đăng → xác nhận trên feed.
7. Báo cáo từng bài: OK / lỗi / số ảnh / ghi chú.

## An toàn
- 2FA / captcha / checkpoint → dừng, nhờ người dùng.
- Không đóng browser giữa batch nếu đang giữ session.
