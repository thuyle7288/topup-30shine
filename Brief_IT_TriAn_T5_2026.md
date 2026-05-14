# BRIEF IT — TRIỂN KHAI 2 CHƯƠNG TRÌNH TOPUP TRI ÂN T5/2026

**Người gửi:** Lê Thanh Thuỳ — Giám đốc Khối Thương mại
**Người nhận:** BP IT
**Ngày gửi:** 14/05/2026 · **Deadline hoàn thành setup:** 17:00 ngày 14/05/2026
**Ngày GO-LIVE:** 15/05/2026 · **Áp dụng đến:** 31/05/2026

---

## 1. TÓM TẮT

Khối Thương mại triển khai 2 chương trình kích cầu Topup tháng 5/2026:
- **Camp "Topup CT1"** — KH mua bill cao → tặng máy massage (bill ≥ 3M hoặc ≥ 6M)
- **Camp "Topup CT2"** — Tạo 8 SKU mới (gói nguyên giá × số buổi · KHÔNG có buổi tặng · TẶNG MÁY MASSAGE thay)

**ON cho TẤT CẢ SALON** từ 15/05 đến 31/05/2026 (sau đó ngắt).

Quà = tận dụng tồn máy massage UMOS đang có sẵn ở salon (167 máy, danh sách dưới đây).

---

## 2. KÝ HIỆU CAMP

| Tên Camp trên hệ thống | Tên hiển thị KH | Cơ chế |
|---|---|---|
| **Topup CT1** | "TRI ÂN T5 — Mua nhiều tặng máy" | Bill Topup ≥ 3M / 6M → in voucher quà |
| **Topup CT2** | "TRI ÂN T5 — Buổi nguyên giá + máy" | 8 SKU mới · mỗi SKU map 1 loại máy |

---

## 3. CAMP "TOPUP CT1" — TẶNG QUÀ THEO BILL (không tạo SKU mới)

### 3.1 Quy tắc kích hoạt

- Trong 1 lần thanh toán, **KH mua Topup (bất kỳ SKU gói nào đang ON) có tổng ≥ 3.000.000đ** → kích hoạt Camp CT1 Mức 1 → in voucher quà
- Trong 1 lần thanh toán, **tổng ≥ 6.000.000đ** → kích hoạt Camp CT1 Mức 2 → in voucher quà cao cấp
- Áp dụng cho mọi SKU Topup hiện hành (Entry 3 buổi, Core 6+1, Loyalty 10+2)
- Áp dụng từ 15/05/2026 đến 31/05/2026 (sau đó IT ngắt)
- 1 KH có thể nhận nhiều quà nếu mua nhiều lần đạt ngưỡng

### 3.2 Mapping pool quà CT1

| Mức | Ngưỡng bill | Pool quà |
|---|---:|---|
| **CT1-A** | ≥ 3.000.000đ | Voucher tag **POOL_A** — KH chọn 1 máy trong 8 dòng Pool A (xem §5.1) |
| **CT1-B** | ≥ 6.000.000đ | Voucher tag **POOL_B** — KH chọn 1 máy trong 3 dòng Pool B (xem §5.2) |

### 3.3 Cơ chế xuất voucher
- POS sau khi xác nhận thanh toán đạt ngưỡng → **in voucher mã 6 số** kèm tag pool (vd: TRIAN001234 — POOL_A)
- Voucher ghi rõ: tên KH, salon, ngày mua, pool quà, hạn nhận quà (trong vòng 30 ngày từ ngày mua)
- KH cầm voucher ra quầy → SM cho xem các máy đang có sẵn ở salon → KH chọn 1 máy trong pool → SM scan voucher + nhập Mã Misa máy KH lấy
- Mã voucher đã dùng → POS đánh dấu redeem, không cho tái sử dụng

---

## 4. CAMP "TOPUP CT2" — TẠO 8 SKU MỚI

### 4.1 Tạo 8 IdSPTopup mới (CHƯA có trên hệ thống)

| STT | IdSPTopup mới (gợi ý) | ServiceId DV gốc | Tên DV gốc | Số buổi | Giá Topup | HSD | Tên hiển thị KH |
|---:|---|---:|---|---:|---:|---:|---|
| 1 | **8001** | 1048 | Combo 4 | 6 | **2.334.000đ** | 365 ngày | Combo 4 — TRI ÂN T5 (Tặng máy massage UMOS) |
| 2 | **8002** | 1047 | Cắt Gội Combo 3 - Chăm da | 6 | **1.794.000đ** | 365 | Cắt Gội C3 Chăm da — TRI ÂN T5 (Tặng máy massage UMOS) |
| 3 | **8003** | 1060 | Gội Combo 4 | 6 | **1.734.000đ** | 365 | Gội Combo 4 — TRI ÂN T5 (Tặng máy massage UMOS) |
| 4 | **8004** | 1059 | Gội Combo 3 - Chăm da | 6 | **1.314.000đ** | 365 | Gội C3 Chăm da — TRI ÂN T5 (Tặng máy massage UMOS) |
| 5 | **8005** | 1058 | Gội Combo 2 | 10 | **1.590.000đ** | 365 | Gội Combo 2 — TRI ÂN T5 (Tặng máy massage UMOS) |
| 6 | **8006** | 1059 | Gội Combo 3 - Chăm da | 10 | **2.190.000đ** | 365 | Gội C3 Chăm da — TRI ÂN T5 (Tặng máy massage UMOS) |
| 7 | **8007** | 1047 | Cắt Gội Combo 3 - Chăm da | 10 | **2.990.000đ** | 365 | Cắt Gội C3 Chăm da — TRI ÂN T5 (Tặng máy massage UMOS) |
| 8 | **8008** | 934 | Gội Combo 3 Dưỡng sinh | 10 | **2.190.000đ** | 365 | Gội Dưỡng sinh — TRI ÂN T5 (Tặng máy massage UMOS) |

**Lưu ý quan trọng cho IT:**
- ⚠️ **CHƯA có concept "tặng buổi"** trong 8 SKU này — KH mua đúng số buổi đã trả tiền (6 hoặc 10), KHÔNG có 1-2 buổi tặng thêm
- Giá Topup = Giá lẻ DV × Số buổi (mua nguyên giá)
- Khi POS bán 1 trong 8 SKU này → **tự động kích hoạt in voucher quà · KH chọn 1 máy trong POOL A** (xem §5.1)
- Tag Camp = `Topup CT2` để báo cáo dễ tổng hợp
- Áp dụng 15/05 - 31/05/2026 (sau đó IT ngắt SKU)
- Số IdSPTopup gợi ý 8001-8008 — IT điều chỉnh theo dải số quản lý nội bộ nếu cần

### 4.2 Cơ chế xuất voucher CT2 — KH CHỌN QUÀ TRONG POOL

- POS bán 1 trong 8 SKU CT2 → in voucher quà tag `Pool A` (xem §5.1)
- **KH cầm voucher ra quầy → chọn 1 máy bất kỳ trong Pool A đang có tại salon** (không map cứng 1 SKU → 1 loại máy)
- Lý do: salon có tồn cục bộ khác nhau, mỗi salon còn các loại máy khác nhau → cho KH linh hoạt chọn = giảm rủi ro "hết đúng loại"
- SM scan voucher + chọn Mã Misa máy KH lấy → ghi nhận xuất kho
- Voucher có thời hạn 30 ngày từ ngày mua
- Mã voucher đã dùng → POS đánh dấu redeem

---

## 5. POOL QUÀ — KH CHỌN TRONG POOL (không map cứng 1-1)

**Lý do thiết kế Pool**: Salon có tồn máy cục bộ khác nhau. Cho KH chọn 1 máy trong Pool → linh hoạt với tồn từng salon, không bị "hết đúng loại đã map".

### 5.1 POOL A — KH chọn 1 máy bất kỳ (CT1 mức Bill 3M-5,99M + Mọi SKU CT2)

| Mã Misa | Tên sản phẩm | Tồn | BQGQ có VAT (đ/máy) |
|---|---|---:|---:|
| **MAYMS_001** | Máy Massage CVG UMOS N11 (6 điểm) | 19 | 372.718 |
| **MAYMS_002** | Máy Massage CVG UMOS N9 (6 điểm) | 2 | 198.000 |
| **MAYMS_010** | Máy Massage CVG UMOS AVS-S7 N12 | 19 | 445.255 |
| **MAYMS_011** | Máy Massage CVG VLT UMOS 202W | 2 | 305.806 |
| **MAYMS_015** | Máy Massage CVG UMOS N12.2 (6 điểm) | 12 | 286.447 |
| **MAYMS_006** | Máy Massage Mắt UMOS AR-216D | 7 | 336.808 |
| **MAYMS_013** | Máy Massage Mắt UMOS M810 (16 điểm) | 10 | 394.281 |
| **MASM_001** | Máy Massage Mắt UMOS YK810 (16 điểm) | 52 | 399.398 |
| | **Tổng Pool A** | **123 máy** | |

→ Voucher tag **POOL_A** — SM quẩn quanh quầy, KH thấy máy nào còn ở salon thì chọn

### 5.2 POOL B — KH chọn 1 máy cao cấp (CT1 mức Bill ≥ 6M)

| Mã Misa | Tên sản phẩm | Tồn | BQGQ có VAT (đ/máy) |
|---|---|---:|---:|
| **MAYMS_003** | Máy Massage Cơ Bắp UMOS MG1S00E | 5 | 552.842 |
| **MAYMS_004** | Máy Massage Cơ Bắp UMOS MG2230 (6 đầu) | 29 | 615.036 |
| **MAYMS_007** | Máy Massage Mắt UMOS AS-EM05 (cao cấp) | 10 | 615.870 |
| | **Tổng Pool B** | **44 máy** | |

→ Voucher tag **POOL_B** — KH chọn 1 trong 3 dòng máy cao cấp

### 5.3 Cơ chế chọn quà tại quầy

1. KH nhận voucher từ POS (tag POOL_A hoặc POOL_B)
2. KH ra quầy lễ tân → xem máy thật đang trưng bày tại salon đó
3. KH chọn 1 máy bất kỳ trong cùng pool còn tồn tại salon
4. SM scan voucher + nhập Mã Misa máy KH lấy → POS trừ tồn realtime
5. Voucher đánh dấu redeem

### 5.4 Tổng tồn: **167 máy** — IT cần báo cáo trừ tồn realtime theo từng Mã Misa & từng salon

---

## 6. HOA HỒNG NV (rule mới áp dụng từ 01/05/2026)

| Giá Topup | HH NV |
|---|---:|
| < 1.800.000đ | 50.000đ |
| ≥ 1.800.000đ | 100.000đ |

Áp dụng cho cả SKU CT1 (gói cũ) và SKU CT2 (8 SKU mới).

---

## 7. TRACKING & BÁO CÁO

IT setup dashboard / báo cáo daily gửi Khối Thương mại lúc 9h sáng:

1. **Số voucher CT1 in / ngày / salon** (chia theo mức 3M, 6M)
2. **Số deal CT2 / ngày / salon** (chia theo 8 SKU 8001-8008)
3. **Tồn máy UMOS realtime** (theo Mã Misa) — cảnh báo khi tồn < 5 máy/loại
4. **Doanh thu Topup CT1 + CT2 / ngày / salon**
5. **Số voucher đã redeem / chưa redeem**

---

## 8. DEADLINE

| Việc | Deadline |
|---|---|
| IT setup 8 SKU mới (8001-8008) | **17:00 ngày 14/05/2026** |
| IT setup flag CT1 + cơ chế in voucher | **17:00 ngày 14/05/2026** |
| Test 1 deal mẫu (1 KH bill 3M CT1 + 1 KH PA4-01 CT2) | **17:00 ngày 14/05/2026** |
| GO-LIVE chính thức tại 58 salon | **15/05/2026** |
| Ngắt 2 chương trình | **23:59 ngày 31/05/2026** |

---

## 9. LIÊN HỆ

- **Owner chiến dịch**: Lê Thanh Thuỳ — Giám đốc Khối Thương mại
- **Vướng mắc IT**: liên hệ trực tiếp chị Thuỳ qua Zalo
- **File phương án đầy đủ**: https://thuyle7288.github.io/topup-30shine/TriAn_T5_PhuongAn_TrinhBGD.html

---

**Cảm ơn anh/chị IT — Khối Thương mại 30Shine**
