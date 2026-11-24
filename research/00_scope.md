# 00 · Scope (Stage 0) — cập nhật 24/11/2026

| Mục | Nội dung | Nguồn |
|---|---|---|
| Câu hỏi | (1) Chu kỳ kinh tế tổng thể VN đang ở pha nào? (2) Từng ngành ở pha nào, đóng góp gì vào chu kỳ chung? | User |
| Quyết định phục vụ | Quyết định đầu tư / tài chính cá nhân của user | User |
| Dữ liệu user có | Báo cáo Cục Thống kê **theo năm** (~10 năm), PDF dài | User |
| Dữ liệu còn thiếu | Chuỗi quý/tháng (GDP theo ngành, IIP, bán lẻ, XNK, tín dụng, CPI, PMI, VN-Index...) — sẽ tìm cùng nhau sau research | User |
| Công cụ | Bất kỳ (đề xuất: Python) | User |
| Thứ tự | Approach research trước → data sau | User |

## Ràng buộc đã biết
- Container không truy cập được gso.gov.vn / nso.gov.vn (502 / connection reset, 24/11/2026) → có thể cần user tải dữ liệu từ máy cá nhân.
- 10 điểm dữ liệu năm không đủ để xác định turning point → bắt buộc bổ sung dữ liệu quý/tháng.

## Quyết định đã chốt — Gate 2 (24/11/2026, user duyệt toàn bộ)
| # | Quyết định | Chốt |
|---|---|---|
| D1 | Định nghĩa chu kỳ | Growth cycle (độ lệch khỏi trend) + growth-rate cycle (tốc độ tăng trưởng); không dùng classical cycle |
| D2 | Dữ liệu xương sống | GDP quý theo ngành từ 2010 + chuỗi tháng từ 2011; PDF năm chỉ dùng cho cơ cấu |
| D3 | Core list | 15 nguồn đánh dấu **Y** trong `01_evidence_log.md` |
| D4 | Dùng cho đầu tư | Khung rủi ro theo regime, không phải tín hiệu timing |
| D5 | Công cụ | Python |
