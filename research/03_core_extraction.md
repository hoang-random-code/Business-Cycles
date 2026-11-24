# 03 · Stage 3 — Đọc sâu core list (24/11/2026)

Mức đọc của từng nguồn được ghi rõ. "FT" = đã đọc full text (các phần liên quan: abstract, phương pháp, kết quả chính, kết luận). Bản đã đọc có thể là working paper; khác biệt so với bản journal được ghi chú.

| ID | Bản đã đọc | Mức đọc |
|---|---|---|
| S02 Harding & Pagan | Melbourne Inst. WP 13/99 (05/1999), tiền thân của JME 2002 | FT |
| S03 Hamilton 1989 | Chỉ abstract (JSTOR có phí) | Abstract |
| S04 Hamilton 2018 | Bản tác giả, sửa 13/05/2017 | FT |
| S06 Kamber-Morley-Wong | CAMA WP 3/2017 | FT |
| S07 Orphanides & van Norden | Bản WP 07/1999 (tiền thân REStat 2002) | FT |
| S09 Canova 1998 | Chỉ "User's guide" (JME 41:533–540); bài chính không tải được (503) | FT bài phụ |
| S11, S12 OECD | Bản chính thức 2012, 2020 | FT |
| S13 Stock & Watson 1989 | Chương NBER | FT (phần cấu trúc chỉ số) |
| S19 Foerster-Sarte-Watson | WP 09/2008 (tiền thân JPE 2011) | FT |
| S20 Aguiar & Gopinath | NBER WP 10734 (2004) | FT |
| S21 García-Cicco et al. | NBER WP 12629 | FT (abstract, intro, data) |
| S22 Pham-Sala-Silva | MPRA 90297 (11/2018), tiền thân Economic Systems 2020 | FT |
| S25 Drehmann-Borio-Tsatsaronis | BIS WP 380 | FT |
| S27 Stock & Watson 2003 | NBER WP 8180 | FT (tổng quan + kết luận) |
| S30 Molchanov & Stangl | Bản journal IJFE, DOI 10.1002/ijfe.2882 | FT |
| S32 IMF Art. IV 2025 | Bản text (~80% verbatim, ~20% cuối chỉ là tóm tắt) | Gần FT |

## Trích xuất theo khối

### D · Turning point
- **S02 BBQ (dữ liệu quý)**: đỉnh tại t nếu y(t) lớn hơn 2 quý trước và 2 quý sau (K=2). Censoring: mỗi pha ≥ 2 quý, cả chu kỳ ≥ 5 quý (Anh phải dùng 4 quý để không bỏ sót chu kỳ 1974). Áp dụng trên log GDP. Chu kỳ trung bình: Mỹ ~62 tháng, Anh ~60 tháng.
- **S02 Concordance index**: I = tỷ lệ số kỳ hai chuỗi ở cùng pha. **Luôn phải so với mức kỳ vọng khi hai chuỗi độc lập.** Ví dụ: Anh–Mỹ 0,82 so với 0,72 nếu độc lập; Úc–Mỹ 0,86 so với 0,76. → Concordance trông cao chưa chắc là đồng bộ thật.
- **S03 Markov-switching** (chỉ abstract): tăng trưởng trung bình nhảy giữa các regime; một cuộc suy thoái điển hình ở Mỹ ứng với mức GNP mất vĩnh viễn ~3%.

### C · Tách trend – cycle
- **S04 Hamilton filter**: hồi quy y(t+h) trên p=4 giá trị gần nhất tại t. **h = 8 với dữ liệu quý, h = 24 với dữ liệu tháng, h = 2 với dữ liệu năm.** HP với λ=1600 tạo dynamics giả; λ ước lượng chính thức thấp hơn 1600 rất nhiều.
- **S06 BN filter**: BN thông thường cho signal-to-noise δ̂=2,22 (GDP Mỹ), khiến gap nhỏ và sai dấu. Áp δ thấp: chọn tự động được δ̄=0,24 (trend shock chiếm 24% phương sai sai số dự báo). Mô hình AR(12) Bayesian với shrinkage prior. Real time: ít bị revise hơn, dự báo tăng trưởng và lạm phát tốt hơn HP, band-pass, detrend tất định.
- **S09 Canova (user's guide)**: các filter khác nhau cho kết quả khác nhau; nhà nghiên cứu phải biết điều đó và kiểm tra xem khác biệt có ảnh hưởng đến kết luận hay không. Phản biện: S10 Burnside.

### G · Độ tin cậy real time
- **S07**: Độ tin cậy output gap real time "khá thấp". Các phương pháp **thường không thống nhất cả về dấu** của gap. **Sai số chuẩn của phần revision cùng bậc độ lớn với chính output gap.** Revision dai dẳng và lệch có hệ thống quanh turning point. Phương pháp trend tăng trưởng cố định (linear trend) revise nhiều nhất → nên dùng trend thay đổi theo thời gian. Nguồn chính của sai số là cuối mẫu, không phải data revision.

### A, E · Pha và chỉ báo tổng hợp
- **S12 OECD, 4 pha (đã xác minh)**:

  | | CLI tăng | CLI giảm |
  |---|---|---|
  | **CLI > 100** (trên trend) | **Expansion**: gap dương, đang rộng ra | **Downturn**: gap dương, đang hẹp lại |
  | **CLI < 100** (dưới trend) | **Recovery**: gap âm, đang hẹp lại | **Slowdown**: gap âm, đang rộng ra |

  Thông tin định tính: CLI không đo tốc độ tăng trưởng; chỉ so được mức trong cùng một pha.
- **S11 OECD, quy trình CLI**:
  1. Chọn thành phần: có lý do kinh tế, phạm vi rộng, theo tháng, ít bị revise, kịp thời, chuỗi dài không gãy. Gồm 4 nhóm lý do: early stage (đơn hàng mới, giấy phép xây dựng), rapidly responsive (giờ làm, lợi nhuận, tồn kho), expectation-sensitive (giá cổ phiếu, giá nguyên liệu, khảo sát niềm tin), prime movers (cung tiền, terms of trade).
  2. Lọc outlier bằng TRAMO.
  3. Dùng HP làm band-pass, giữ chu kỳ 12–120 tháng (thay PAT/MCD từ 11/2008 vì revision ổn định hơn).
  4. Xác định turning point bằng Bry-Boschan rút gọn.
  5. Chuẩn hóa: (x − mean)/MAD + 100.
  6. Gộp các thành phần.
  - Mục tiêu dẫn trước 6–9 tháng.
- **S13 Stock-Watson coincident index**: dựng từ 4 chuỗi tháng của Mỹ: IP, thu nhập cá nhân thực trừ trợ cấp, doanh số sản xuất và thương mại thực, giờ công. Leading index dự báo 6 tháng; spread lãi suất là predictor tốt.

### H · Ngành
- **S19 (bản WP 2008)**: aggregate shocks giải thích phần lớn biến động IP Mỹ. Tỷ trọng của cú sốc riêng ngành tăng từ ~12% (trước 1984) lên ~30% (sau 1984). **Lưu ý:** tóm tắt bản JPE 2011 ghi "khoảng một nửa", khác số trong WP → cần kiểm tra bản journal trước khi trích.

### F · Đặc thù EM và Việt Nam
- **S20 (EM 1980–2003)**: tiêu dùng biến động hơn thu nhập 40% (nước phát triển < 1). Tỷ lệ σg/σz (cú sốc trend so với cú sốc tạm thời): Mexico 2,5–5,4, Canada 0,25–0,61, tức hơn kém một bậc độ lớn.
- **S21 (Argentina, Mexico 1900–2005)**: mẫu ngắn làm sai lệch kết luận. Mô hình có financial frictions và cú sốc country premium gán cho cú sốc năng suất không dừng vai trò **không đáng kể**.
- **S22 Việt Nam 1986–2015**:
  - Dùng **dữ liệu năm của UNSD vì dữ liệu quý chỉ có từ sau 2000 và không đủ các biến tổng hợp** → xác nhận rủi ro dữ liệu của dự án.
  - Cú sốc năng suất tạm thời ≈ ½ phương sai output; country risk và cú sốc năng suất không dừng mỗi loại ≈ ⅕.
  - Trend chỉ chiếm 12% phương sai Solow residual (Thái Lan 6%).
  - Độ lệch chuẩn tăng trưởng GDP giai đoạn 2001–2015 giảm ⅓ so với 1986–2000.
  - Tăng trưởng chủ yếu nhờ tích lũy vốn.

### I · Tài chính và đầu tư
- **S25 Financial cycle**:
  - Đo bằng credit, credit/GDP, giá nhà; giá cổ phiếu không khớp.
  - Dữ liệu quý của 7 nước, 1960–2011.
  - Chu kỳ ngắn hạn 5–32 quý; chu kỳ trung hạn 32–120 quý (8–30 năm).
  - Turning point: chu kỳ ngắn ≥ 5 quý, mỗi pha ≥ 2 quý; chu kỳ trung hạn dùng cửa sổ 9 quý, ≥ 40 quý.
  - Chu kỳ tài chính dài trung bình **~16 năm** (các chu kỳ có đỉnh sau 1998: ~20 năm).
  - Mọi khủng hoảng ngân hàng có nguồn gốc trong nước đều xảy ra gần đỉnh chu kỳ tài chính.
- **S27 (7 nước OECD, 1959–99)**:
  - Giá tài sản chỉ có "khả năng dự báo biên nhỏ" cho output ở chân trời 2, 4, 8 quý. Không có biến nào hoạt động tốt qua nhiều nước và nhiều thập kỷ; term spread gần nhất nhưng không ổn định.
  - **Stock returns nhìn chung không có khả năng dự báo đáng kể cho output.**
  - Biến nào thắng ở giai đoạn 1 không liên quan đến việc nó có thắng ở giai đoạn 2 hay không.
- **S30 (Mỹ 1948–2022, 14–15 chu kỳ, bản journal)**:
  - Biết trước chu kỳ hoàn hảo: sector rotation đạt **0,16%/tháng** risk-adjusted (≈1,9%/năm) trước chi phí; rủi ro cao hơn (độ lệch chuẩn và beta cao hơn thị trường).
  - **Một chiến lược market-timing đơn giản (ở trong thị trường, chỉ rút ra trong giai đoạn đầu suy thoái) đạt 0,18%/tháng**, cao hơn sector rotation.
  - Sau chi phí giao dịch (spread ~0,75%, 75 giao dịch khứ hồi) và sai số timing thì lợi thế gần như mất hết.
  - Khả năng dự báo chéo giữa các ngành không khác gì ngẫu nhiên.
- **S32 IMF Art. IV 2025 (bảng Key Statistics and Projections)**:
  - GDP thực: 2021 2,6% · 2022 8,5% · 2023 5,1% · 2024 7,1% · 2025p 6,5% · 2026p 5,6%.
  - CPI bình quân: 2024 3,6%, 2025p 3,4%. Lạm phát lõi 2024 2,7%, 2025p 3,2%.
  - Tín dụng tăng 15% (2024) và 19% yoy (6/2025). Dư nợ tín dụng = 136% GDP. **Credit-to-GDP gap dương năm 2024.**
  - Văn bản: "the output gap turned positive". Dự kiến "negative output gap" mở ra năm 2026.
  - **Không tìm thấy hàng output gap định lượng trong bản text** → các con số output gap từ snippet ở Stage 2 bị hạ xuống [Unverified].
  - Chất lượng dữ liệu: "rapid economic transformation is outpacing development of robust economic statistics"; sai số và bỏ sót trong BOP = 6,9% GDP (2024); **"rebasing of the national accounts is scheduled for completion in 2026"**.
  - Rủi ro: bất động sản, trái phiếu doanh nghiệp, ngân hàng yếu (likelihood: High). Thuế Mỹ cơ sở 20% từ 8/2025; kịch bản xấu (40%): tăng trưởng giảm thêm 0,2–0,6 điểm % trong 2025–26.

## Xung đột mới
4. **Chứng khoán có dự báo kinh tế không?** S26 Estrella-Mishkin: giá cổ phiếu có ích ở chân trời 1–2 quý ⟷ S27: stock returns nhìn chung không dự báo đáng kể output. Lý do khả dĩ: S26 dự báo *xác suất suy thoái* (biến nhị phân, chỉ Mỹ); S27 dự báo *tốc độ tăng trưởng output* (biến liên tục, 7 nước, kiểm tra tính ổn định ngoài mẫu). → Với VN: dùng VN-Index làm một thành phần của CLI (theo S11), không dùng làm tín hiệu đơn lẻ.
5. **Tăng trưởng 2025**: IMF dự báo 6,5% (giữa 2025) ⟷ NSO ước tính 8,02% (01/2026). Đây là dự báo so với số ước tính, không cùng thời điểm; cần lấy số NSO đã chính thức hóa.
6. **S19 bản WP và bản JPE** cho tỷ trọng cú sốc ngành khác nhau (30% so với "khoảng một nửa").

## Hệ quả cho approach (đề xuất cập nhật)
1. **Báo cáo dạng "đồng thuận"**: vì các phương pháp có thể khác nhau cả về dấu (S07), kết quả output gap báo dưới dạng "k/4 filter cho gap dương" kèm dải giá trị, không báo một con số.
2. **Ưu tiên filter có trend thay đổi theo thời gian** (S07): Hamilton (h=8), BN filter (δ̄≈0,24), HP chỉ để đối chiếu. Không dùng linear trend, vì tăng trưởng tiềm năng của VN thay đổi (S22: biến động giảm ⅓ sau 2000).
3. **Chu kỳ tài chính chỉ ở mức mô tả**: chu kỳ dài ~16–20 năm (S25), trong khi dữ liệu tín dụng VN chỉ đủ cho tối đa 1–2 chu kỳ → không ước lượng thống kê được. Dùng credit-to-GDP gap như chỉ báo rủi ro (IMF: gap dương 2024, tín dụng 136% GDP).
4. **Vintage dữ liệu**: NSO đổi năm gốc vào 2026 (S32) → lưu từng phiên bản dữ liệu, chỉ dùng tốc độ tăng trưởng để ghép chuỗi, chạy lại khi có số mới.
5. **Coincident index VN thiếu chuỗi việc làm theo tháng** (S13 dùng giờ công) → dùng IIP, bán lẻ thực, nhập khẩu, PMI; ghi nhận đây là giới hạn.
6. **Đầu tư (củng cố D4)**: theo S30, điều chỉnh mức phơi nhiễm tổng thể theo regime đạt kết quả ít nhất bằng sector rotation và đơn giản hơn; mọi backtest phải tính chi phí giao dịch và sai số timing.
