# social-fb-ops

Playbook + prompt đa Page để agent (Antigravity / Grok Bot / Cursor) **sao chép / đăng bài Facebook Page**.

Không hardcode một Page cố định. Mỗi lệnh ghi rõ **Page nguồn** và **Page đích**.

## Cấu trúc

```
playbooks/     # mục tiêu + quy trình
prompts/       # system prompt & lệnh ngắn
sessions/      # nhật ký batch (tuỳ chọn, không commit secret)
```

## Dùng với Antigravity IDE

1. Mở folder repo này trong Antigravity (`git pull` nếu đã clone).
2. `AGENTS.md` được IDE đọc tự động — không cần dán lại toàn bộ mỗi lần, nhưng nên dán `prompts/03-prompt-da-page.md` vào agent setup **một lần**.
3. Mỗi lần giao việc: copy lệnh trong `prompts/04-cheat-sheet.md` (điền URL + N).

## Không commit

Xem `.gitignore`: cookie, auth JSON, ảnh scrape, `.env`.

## File hay

- `AGENTS.md` — Antigravity / Cursor đọc tự động khi mở repo
- `prompts/04-cheat-sheet.md` — lệnh dán nhanh
- `playbooks/05-meo-toc-do.md` — mẹo thực chiến
- `playbooks/pages-dang-ky.md` — bảng Page (team điền)
- `sessions/NHAT-KY-MAU.md` — nhật ký batch
