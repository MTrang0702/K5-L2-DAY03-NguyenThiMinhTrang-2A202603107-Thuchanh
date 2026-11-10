# BÀI THỰC HÀNH CÁ NHÂN: ANNOTATION & SEGMENTATION (DAY 03)

**Họ và tên:** Nguyễn Thị Minh Trang  
**MSSV:** 2A202603107  
**Lớp/Khóa:** Khóa 5 (K5-L2)  
**Chủ đề:** Phân đoạn ảnh đường phố đô thị (Urban Street Scene Segmentation)

---

## 1. PHIẾU THÔNG TIN DATASET

- **Tên chủ đề:** Phân đoạn ảnh đường phố đô thị (Urban Street Scene Segmentation)
- **Tên Dataset:** Cityscapes Dataset
- **Nguồn / Link tải:** Kaggle (Kaggle Cityscapes Dataset)
- **Loại giấy phép (License):** CC BY-NC-SA 4.0 (Nghiên cứu & Học tập phi thương mại)
- **Các nhãn phân đoạn (Labels):**
  - `car`: Xe con
  - `pedestrian`: Người đi bộ
  - `road`: Mặt đường

---

## 2. QUY TRÌNH THỰC HIỆN CVAT

1. **Khởi tạo Task trên CVAT:** Đã tạo Task với 3 nhãn Polygon (`car`, `pedestrian`, `road`).
2. **Gán nhãn:** Hoàn thành gán nhãn 3 ảnh mẫu đường phố bằng công cụ Polygon/Mask.
3. **Export Dữ liệu:** Xuất tập dữ liệu gán nhãn ở định dạng `COCO 1.0 (segmentation)` / `CVAT for images 1.1`.

---

## 3. BẢNG ĐO ĐÁNH GIÁ CHẤT LƯỢNG GÁN NHÃN

| Chỉ số / Tiêu chí | Kết quả đánh giá | Ghi chú / Đánh giá chi tiết |
| :--- | :--- | :--- |
| **Số lượng ảnh gán** | 3 / 3 ảnh | Hoàn thành 100% mục tiêu |
| **Độ ôm sát vùng biên (Border Fit)** | ~85% - 90% | Khung Polygon ôm sát thân xe và người, các đường cong mép gán tương đối mịn |
| **Độ chính xác phân loại (Label Accuracy)** | 100% | Phân biệt chuẩn giữa `car`, `pedestrian` và `road` |
| **So với Ground Truth gốc** | Khá tương đồng | Nhãn tự gán ôm sát các chi tiết chính, chỉ lệch nhẹ ở viền bánh xe/gầm |

---

## 4. CẤU TRÚC THƯ MỤC

```text
.
├── README.md              # Báo cáo tổng quan bài thực hành
└── cvat_export/           # Chứa file nhãn export từ CVAT (.zip / .json / .xml)# K5-L2-DAY03-NguyenThiMinhTrang-2A202603107-Thuchanh
Bài thực hành cá nhân: Phân đoạn ảnh đường phố đô thị
