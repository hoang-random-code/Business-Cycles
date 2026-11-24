# 02 · Knowledge base outline + Approach đề xuất (bản nháp chờ Gate 2)

Nhãn: **[Fact]** có nguồn (ID trong `01_evidence_log.md`) · **[Theory]** · **[Assumption]** · **[Unverified]**. Tất cả nguồn mới đọc ở mức abstract.

## Nguyên tắc chung (cách expert đang làm)
1. **Không có phương pháp duy nhất đúng** → dùng nhiều phương pháp rồi so sánh chéo (triangulation). Stylized facts đổi theo filter [Fact: S09; phản biện S10].
2. **Tách 3 câu hỏi**: (a) chu kỳ *đã* xảy ra (dating, ex post) · (b) *hiện tại* đang ở đâu (nowcast, real time) · (c) *sắp tới* đi đâu (leading). Độ tin cậy giảm dần từ a → c [Fact: S07].
3. **Xác suất thay vì nhãn cứng**: báo "xác suất ở pha mở rộng = x%" thay vì "đang ở pha X" [Theory: S03, S17].
4. **Kiểm tra real time**: mô phỏng lại "nếu đứng ở quý t thì mô hình nói gì" và đếm số lần kết luận bị đảo ngược về sau [Fact: S06, S07].

## Kiến trúc approach: 6 tầng

| Tầng | Câu hỏi | Phương pháp | Dữ liệu tối thiểu | Nguồn |
|---|---|---|---|---|
| 0. Nền dữ liệu | Số liệu có dùng được không? | Điều chỉnh mùa vụ X-13 + regressor Tết; ghép chuỗi qua đợt đánh giá lại GDP 2019 (dùng growth, không dùng level); quy về giá so sánh | GDP quý theo ngành, IIP, bán lẻ, XNK, tín dụng, CPI, PMI | S36, S37, S39 |
| 1. Reference cycle (toàn nền KT) | Đỉnh/đáy ở đâu? | (a) Growth-rate cycle: BBQ trên tăng trưởng GDP yoy · (b) Growth cycle: output gap bằng HP + Hamilton + BN + CF → dải ước lượng · (c) Markov-switching → xác suất regime | GDP quý ≥ 2010 | S02, S03, S04, S06, S08, S09 |
| 2. Chỉ báo tổng hợp tháng | Hiện tại ở pha nào? Sắp tới ra sao? | Coincident index (DFM) + Leading index (phương pháp OECD CLI: detrend → smooth → chuẩn hóa → gộp); đọc pha theo mức (trên/dưới 100) × hướng (tăng/giảm) | ~8–15 chuỗi tháng | S11, S12, S13, S14 |
| 3. Phân rã ngành | Ngành nào dẫn / trùng / trễ / phi chu kỳ? Đóng góp bao nhiêu? | Dating từng ngành bằng cùng thuật toán · concordance & synchronization test · cross-correlation lead/lag · contribution to growth (tỷ trọng × tăng trưởng) · factor model chung vs ngành | GDP quý theo ngành; IIP theo ngành | S18, S19 |
| 4. Chu kỳ tài chính | Tín dụng & BĐS đang ở đâu? | Credit-to-GDP gap; turning point của tín dụng + giá BĐS (chu kỳ trung hạn) | Tín dụng tháng (NHNN), giá BĐS | S25, S32, S35 |
| 5. Chứng khoán & đầu tư | Chu kỳ nói gì cho tài sản? | Chứng khoán như leading indicator; lợi suất kỳ vọng theo pha; backtest có chi phí giao dịch | VN-Index, lãi suất, ngành trên sàn | S26, S27, S28, S29, S30 |
| (xuyên suốt) Độ tin cậy | Kết luận chắc đến đâu? | Pseudo-real-time backtest; dải ước lượng giữa các filter; so với output gap của IMF | — | S06, S07, S17, S32 |

## Đặc thù Việt Nam cần đưa vào
- **Định nghĩa chu kỳ**: VN tăng trưởng dương liên tục theo năm (2020 vẫn +2,9% [Fact: S44 — single-source, cần đối chiếu NSO]) → dùng **growth cycle / growth-rate cycle**, không dùng classical cycle (suy thoái = GDP giảm).
- **Tranh luận EM** (S20 vs S21, S22): với VN, S22 cho rằng cú sốc tạm thời chiếm ≈ ½ phương sai output → tách trend–cycle có ý nghĩa, nhưng vẫn phải dùng nhiều filter. Confidence: Med.
- **Kênh bên ngoài**: xuất khẩu (Mỹ ~⅓ xuất khẩu năm 2025 — [Unverified, nguồn Tier 3: S43]), FDI.
- **Chính sách**: NHNN đặt trần tăng trưởng tín dụng [Fact: S33] → chu kỳ tín dụng mang tính hành chính một phần.
- **Các giai đoạn căng thẳng đã ghi nhận**: tín dụng nóng 2008, 2010 → thắt 2011 [S35, single-source]; BĐS & trái phiếu DN 2022–23 [S34].

## Kỳ vọng thực tế cho mục tiêu đầu tư
- Ngay cả khi biết trước chu kỳ một cách hoàn hảo, sector rotation ở Mỹ chỉ thêm ~2,3%/năm; có sai số timing thực tế thì không còn ý nghĩa thống kê [Fact: S29; bản peer-reviewed S30: "chỉ rất nhỏ"]. Chưa có nghiên cứu tương tự cho VN [gap, Low].
- Giá cổ phiếu *dẫn trước* kinh tế 1–2 quý [Fact: S26] → khi dữ liệu vĩ mô xác nhận một pha, thị trường thường đã phản ánh.
- Tín hiệu từ giá tài sản không ổn định theo nước và thời kỳ; kết hợp nhiều tín hiệu thì tốt hơn [Fact: S27].
→ **Đề xuất dùng chu kỳ như khung quản trị rủi ro theo regime**, không dùng như tín hiệu mua/bán đơn lẻ. Confidence: Med–High.

## Gap (đến giờ)
- Không tìm thấy turning point chronology đã công bố cho VN; cũng không tìm thấy CLI kiểu OECD cho VN → đây là phần giá trị gia tăng của dự án. Coverage: ~4 truy vấn → **confidence Low**, sẽ tìm kỹ hơn ở Stage 3.

## Quyết định chờ chốt (Gate 2)
D1 định nghĩa chu kỳ · D2 tần suất dữ liệu nền · D3 core list · D4 cách dùng kết quả cho đầu tư · D5 công cụ. Chi tiết trong chat.
