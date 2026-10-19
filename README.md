# NatureSyn MVP 0.2 – phiên bản sẵn sàng triển khai miễn phí

## Tính năng
Dashboard, 5 AI Agent mô phỏng, hội đồng thảo luận và biểu quyết, Thiên Sinh Kinh, nghi lễ, cố vấn, xuất và nhập dữ liệu JSON.

**Giới hạn**: Các Agent là mô phỏng theo quy tắc, không kết nối model AI thật. Mọi dữ liệu mới nhập được lưu **localStorage** trên chính trình duyệt, **không đồng bộ** qua thiết bị hoặc người dùng. Không có đăng nhập, cơ sở dữ liệu, API hay hệ thống kiểm soát quyền phía server. KHÔNG dùng để lưu bí mật.

## Phương án 1 — GitHub Pages, 0 USD
1. Đăng nhập GitHub, tạo **repository public** có tên `naturesyn` (hoặc tên khác).
2. Tải gói ZIP, giải nén, upload **nội dung thư mục** vào gốc repository, gồm `index.html`, `.nojekyll`, `.github/workflows/deploy.yml`.
3. Trong Settings → Pages → Build and deployment → Source, chọn **GitHub Actions**.
4. Chờ workflow `Deploy NatureSyn to GitHub Pages` hoàn tất tại tab Actions.
5. URL thường có dạng `https://TEN_TAI_KHOAN.github.io/naturesyn/`.
6. Mỗi lần cập nhật commit trên `main`, trang web được triển khai lại.

GitHub Free yêu cầu repo public đối với GitHub Pages; đừng đẩy khóa API, thông tin nhạy cảm hoặc dữ liệu cá nhân vào repo.

## Phương án 2 — Cloudflare Pages, Direct Upload
1. Vào https://dash.cloudflare.com/, đăng nhập và mở Workers & Pages / Pages.
2. Tạo dự án Pages bằng **Direct Upload**.
3. Kéo thả thư mục đã giải nén (hoặc ZIP) từ bản phát hành này.
4. Triển khai; nền tảng cung cấp địa chỉ `*.pages.dev` nếu tên dự án khả dụng.
5. Khi cập nhật, upload bản mới từ trang dự án.

## Kiểm tra
- Mở index.html cục bộ, thử cả 6 tab.
- Thử hội đồng, nghi lễ, thêm cố vấn giả định, sao lưu JSON.
- Tải trang từ GitHub Pages hoặc Cloudflare sau khi xuất bản.
- Trên điện thoại kiểm tra menu và các biểu mẫu.

## Định hướng phiên bản 0.3
- Supabase Free cho dữ liệu nhiều người dùng, xác thực, Row Level Security.
- Backend/edge function trung gian cho LLM API: tuyệt đối không đặt API key vào frontend/public GitHub.
- Giới hạn chi phí API và yêu cầu phê duyệt của con người với tác vụ bên ngoài.

© NatureSyn – bản demo triết học và cộng đồng kỹ thuật, chưa có tư cách pháp lý của tổ chức tôn giáo.
