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

| Mức | Ngưỡng bill | Pool quà (KH chọn 1) |
|---|---:|---|
| **CT1-A** | ≥ 3.000.000đ | Pool A (Quà thường) — xem §5 |
| **CT1-B** | ≥ 6.000.000đ | Pool B (Quà cao cấp) — xem §5 |

### 3.3 Cơ chế xuất voucher
- POS sau khi xác nhận thanh toán đạt ngưỡng → **in voucher mã 6 số** (vd: TRIAN001234)
- Voucher ghi rõ: tên KH, salon, ngày mua, pool quà được chọn (A hoặc B), hạn nhận quà (trong vòng 30 ngày từ ngày mua)
- KH cầm voucher ra quầy lễ tân → SM scan mã → trao máy + ghi nhận xuất kho
- Mã voucher đã dùng → POS đánh dấu redeem, không cho tái sử dụng

---

## 4. CAMP "TOPUP CT2" — TẠO 8 SKU MỚI

### 4.1 Tạo 8 IdSPTopup mới (CHƯA có trên hệ thống)

| STT | IdSPTopup mới (gợi ý) | ServiceId DV gốc | Tên DV gốc | Số buổi | Giá Topup | HSD | Tên hiển thị KH | Map quà (Mã Misa) |
|---:|---|---:|---|---:|---:|---:|---|---|
| 1 | **8001** | 1048 | Combo 4 | 6 | **2.334.000đ** | 365 ngày | Combo 4 — TRI ÂN T5 (Tặng máy massage CVG UMOS) | **MAYMS_010** |
| 2 | **8002** | 1047 | Cắt Gội Combo 3 - Chăm da | 6 | **1.794.000đ** | 365 | Cắt Gội C3 Chăm da — TRI ÂN T5 (Tặng máy massage CVG UMOS) | **MAYMS_015** |
| 3 | **8003** | 1060 | Gội Combo 4 | 6 | **1.734.000đ** | 365 | Gội Combo 4 — TRI ÂN T5 (Tặng máy massage CVG UMOS) | **MAYMS_001** |
| 4 | **8004** | 1059 | Gội Combo 3 - Chăm da | 6 | **1.314.000đ** | 365 | Gội C3 Chăm da — TRI ÂN T5 (Tặng máy massage UMOS) | **MAYMS_006** |
| 5 | **8005** | 1058 | Gội Combo 2 | 10 | **1.590.000đ** | 365 | Gội Combo 2 — TRI ÂN T5 (Tặng máy massage CVG UMOS) | **MAYMS_015** |
| 6 | **8006** | 1059 | Gội Combo 3 - Chăm da | 10 | **2.190.000đ** | 365 | Gội C3 Chăm da — TRI ÂN T5 (Tặng máy massage CVG UMOS) | **MAYMS_001** |
| 7 | **8007** | 1047 | Cắt Gội Combo 3 - Chăm da | 10 | **2.990.000đ** | 365 | Cắt Gội C3 Chăm da — TRI ÂN T5 (Tặng máy massage CVG UMOS) | **MAYMS_010** |
| 8 | **8008** | 934 | Gội Combo 3 Dưỡng sinh | 10 | **2.190.000đ** | 365 | Gội Dưỡng sinh — TRI ÂN T5 (Tặng máy massage CVG UMOS) | **MAYMS_001** |

**Lưu ý quan trọng cho IT:**
- ⚠️ **CHƯA có concept "tặng buổi"** trong 8 SKU này — KH mua đúng số buổi đã trả tiền (6 hoặc 10), KHÔNG có 1-2 buổi tặng thêm
- Giá Topup = Giá lẻ DV × Số buổi (mua nguyên giá)
- Khi POS bán 1 trong 8 SKU này → **tự động kích hoạt in voucher quà** với Mã Misa quà tương ứng (xem cột cuối)
- Tag Camp = `Topup CT2` để báo cáo dễ tổng hợp
- Áp dụng 15/05 - 31/05/2026 (sau đó IT ngắt SKU)
- Số IdSPTopup gợi ý 8001-8008 — IT điều chỉnh theo dải số quản lý nội bộ nếu cần

### 4.2 Cơ chế xuất voucher CT2

- POS bán 1 trong 8 SKU CT2 → **tự động in voucher gắn liền** với Mã Misa quà đã map
- Voucher quy đổi 1 máy massage UMOS cụ thể tại quầy (KHÔNG cho KH chọn loại khác)
- Voucher có thời hạn 30 ngày từ ngày mua
- Mã voucher đã dùng → POS đánh dấu redeem

---

## 5. POOL QUÀ — DANH SÁCH MÁY MASSAGE UMOS

### 5.1 Pool A — Quà thường (CT1 mức 1: Bill 3M-5,99M · CT2 các SKU 6 buổi)

| Mã Misa | Tên sản phẩm | Tồn | BQGQ có VAT (đ/máy) | Phân nhóm dùng |
|---|---|---:|---:|---|
| **MAYMS_015** | Máy Massage CVG UMOS N12.2 (6 điểm) | 12 | 286.447 | CT2-8002, 8005 |
| **MAYMS_001** | Máy Massage CVG UMOS N11 (6 điểm) | 19 | 372.718 | CT2-8003, 8006, 8008 |
| **MAYMS_002** | Máy Massage CVG UMOS N9 (6 điểm) | 2 | 198.000 | CT1 Pool A |
| **MAYMS_010** | Máy Massage CVG UMOS AVS-S7 N12 | 19 | 445.255 | CT2-8001, 8007 |
| **MAYMS_011** | Máy Massage CVG VLT UMOS 202W | 2 | 305.806 | CT1 Pool A |
| **MAYMS_013** | Máy Massage Mắt UMOS M810 (16 điểm) | 10 | 394.281 | CT1 Pool A |
| **MASM_001** | Máy Massage Mắt UMOS YK810 (16 điểm) | 52 | 399.398 | CT1 Pool A |
| **MAYMS_006** | Máy Massage Mắt UMOS AR-216D | 7 | 336.808 | CT2-8004 |
| | **Tổng Pool A** | **123 máy** | | |

### 5.2 Pool B — Quà cao cấp (CT1 mức 2: Bill ≥ 6M)

| Mã Misa | Tên sản phẩm | Tồn | BQGQ có VAT (đ/máy) | Phân nhóm dùng |
|---|---|---:|---:|---|
| **MAYMS_004** | Máy Massage Cơ Bắp UMOS MG2230 (6 đầu) | 29 | 615.036 | CT1 Pool B chính |
| **MAYMS_003** | Máy Massage Cơ Bắp UMOS MG1S00E | 5 | 552.842 | CT1 Pool B |
| **MAYMS_007** | Máy Massage Mắt UMOS AS-EM05 (cao cấp) | 10 | 615.870 | CT1 Pool B |
| | **Tổng Pool B** | **44 máy** | | |

### 5.3 Tổng tồn: **167 máy** — IT cần báo cáo trừ tồn realtime sau mỗi deal

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
