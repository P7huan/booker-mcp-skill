# Ohdidi Booker MCP Agent Skill (`booker-mcp`)

Bộ kỹ năng điều phối toàn diện **11 công cụ Ohdidi Booker MCP** (Tìm kiếm Chỗ nghỉ, Xem chi tiết Phòng/Nguyên căn/Villa, Kiểm tra phòng trống & Báo giá chuẩn Server, Quản lý Yêu cầu đặt phòng / Leads, Tạo & Cập nhật Booking, Giao dịch thanh toán `BookingTransaction` & VietQR Khách/Host, Xác nhận đơn, Hủy đơn, Hoàn thành đơn, Áp Voucher & Gửi Email Hợp đồng) dành cho AI Coding Agent & AI Travel Assistant (Antigravity / Claude / Cursor / Gemini CLI).

---

## 🚀 1. Cài đặt lần đầu (cho máy mới hoặc thành viên khác)

Chạy lệnh sau để kéo trực tiếp từ GitHub về thư mục cấu hình Skills của Agent:

```bash
git clone git@github.com:P7huan/booker-mcp-skill.git ~/.gemini/config/skills/booker-mcp
```

*(Hoặc nếu dùng `npx skills` CLI):*
```bash
npx skills add P7huan/booker-mcp-skill -g -y
```

---

## 🔄 2. Tự động cập nhật phiên bản mới nhất

Khi có bản cập nhật mới trên Git, chỉ cần bảo Agent *"Cập nhật skill booker-mcp"* hoặc chạy:

```bash
git -C ~/.gemini/config/skills/booker-mcp pull --ff-only origin main
```

---

## 📦 3. Cấu trúc thư mục

- [`SKILL.md`](./SKILL.md): Quy chuẩn vận hành 11 công cụ Booker MCP, quy tắc tính giá gốc (`total_price_origin`), lợi nhuận (`benefit`), thuế VAT đối tác doanh nghiệp (`tax_rate`, `tax_included`), kiểm tra tài khoản ngân hàng nhận `[DN]` vs `[CN]`, và kỷ luật xác nhận Dry-Run (`confirm: false` $\rightarrow$ `confirm: true`).
