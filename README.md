# Phân loại dữ liệu HR — Học liệu tương tác (Chuẩn DAMA)

Trang web học liệu tương tác cho **Buổi 3 — Năng lực & Quản lý dữ liệu HR**, thuộc chương trình đào tạo **HR Analytics x Generative AI**.

Nội dung trình bày cách phân loại dữ liệu HR theo 4 trục của chuẩn **DAMA-DMBOK** (Data Management Body of Knowledge), kèm bài tập tương tác.

## Nội dung trang

1. **Bốn trục phân loại DAMA** — bản chất đo lường, mức độ tổ chức, tần suất thay đổi, tần suất truy cập.
2. **So sánh từng nhóm** với ví dụ thực tế từ nhà máy sản xuất:
   - Định lượng vs Định tính
   - Có cấu trúc · Bán cấu trúc · Phi cấu trúc
   - Master Data vs Dữ liệu giao dịch
   - Dữ liệu nóng vs Dữ liệu lạnh
3. **Lab tương tác** — phân loại bằng kéo–thả hoặc chạm-để-chọn (hỗ trợ cả máy tính và thiết bị cảm ứng).
4. **Quiz 8 câu** — các tình huống HR thực tế kèm giải thích.
5. **Đúc kết bài học** — ba nguyên tắc cốt lõi.

## Cấu trúc thư mục

```
.
├── index.html      # Toàn bộ trang web (HTML + CSS + JS trong một file)
├── .nojekyll       # Báo GitHub Pages không xử lý qua Jekyll
├── README.md       # File này
└── LICENSE         # Giấy phép sử dụng
```

Trang là **một file `index.html` duy nhất** — không cần build, không cần cài đặt. Font chữ và bộ icon được nạp từ CDN công cộng nên cần kết nối internet khi mở.

## Cách đưa lên GitHub Pages (web public)

### Cách 1 — Qua giao diện web GitHub (không cần dùng lệnh)

1. Tạo một repository mới, để ở chế độ **Public**.
2. Bấm **Add file → Upload files**, kéo cả 4 file (`index.html`, `.nojekyll`, `README.md`, `LICENSE`) vào, rồi **Commit changes**.
   - Lưu ý: file `.nojekyll` bắt đầu bằng dấu chấm — nếu giao diện ẩn nó, vẫn upload bình thường được.
3. Vào **Settings → Pages**.
4. Mục **Source** chọn **Deploy from a branch**; chọn nhánh `main` và thư mục `/ (root)`; bấm **Save**.
5. Đợi 1–2 phút, GitHub sẽ hiện đường dẫn dạng:
   `https://<tên-tài-khoản>.github.io/<tên-repo>/`

### Cách 2 — Qua dòng lệnh Git

```bash
git init
git add .
git commit -m "HR data classification interactive page"
git branch -M main
git remote add origin https://github.com/<tên-tài-khoản>/<tên-repo>.git
git push -u origin main
```

Sau đó vào **Settings → Pages** và làm theo bước 3–5 ở Cách 1.

## Tuỳ chỉnh

- Toàn bộ nội dung, ví dụ, câu quiz nằm ngay trong `index.html`.
- Dữ liệu Lab nằm trong biến `AXES`; dữ liệu Quiz nằm trong biến `QUIZ` (trong khối `<script>` cuối file).
- Bảng màu nằm trong khối `:root { ... }` ở đầu thẻ `<style>`.

## Ghi chú kỹ thuật

- Không dùng `localStorage`/`sessionStorage` — chạy được trên mọi môi trường.
- Tương thích các trình duyệt hiện đại (Chrome, Edge, Firefox, Safari).
- Lab hỗ trợ cả thao tác kéo–thả (máy tính) và chạm-để-chọn (máy tính bảng, điện thoại).
