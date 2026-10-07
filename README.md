
# Hướng dẫn chạy bài thực hành xử lý ảnh

## 1. Chuẩn bị

Mở PowerShell tại thư mục dự án:

```powershell
cd "D:\OPENCV\BTTL"
```

Cài các thư viện cần dùng:

```powershell
python -m pip install numpy opencv-python matplotlib pillow
```

Nếu máy dùng lệnh `py` thay cho `python`, có thể thay `python` bằng `py` trong các lệnh bên dưới.

## 2. Bài 1 — Histogram và cân bằng histogram

Các chương trình mặc định xử lý cả `sang.png` và `toi.png` trong thư mục `Input Images`:

```powershell
python Code/histogram.py
python Code/histogram_bins_levels.py
python Code/histogram_equalization.py
```

Kết quả được lưu trong `ket_qua_histogram`. Để chỉ xử lý một ảnh, truyền đường dẫn ảnh, ví dụ:

```powershell
python Code/histogram.py "Input Images/toi.png"
```

Muốn mở cửa sổ xem kết quả của `histogram.py`, thêm `--show`:

```powershell
python Code/histogram.py "Input Images/toi.png" --show
```

## 3. Bài 2 — Lọc Median và Gaussian

```powershell
python Code/median_filter.py
python Code/gaussian_filter.py
```

Median mặc định đọc `Input Images/nhieumuoitieu.jpg`; Gaussian đọc `Input Images/nhieuhat.jpg`. Ảnh kết quả và ảnh so sánh ba ảnh được lưu trong `Code/ket_qua_bai2`.

Hai phép lọc được tính bằng vòng lặp nên ảnh lớn có thể mất một lúc để xử lý.

## 4. Bài 3 — Tách biên Sobel và Laplace

Truyền ảnh tối `toi.png` vào từng chương trình:

```powershell
python BTTL3/Code/sobel.py "Input Images/toi.png"
python BTTL3/Code/laplace.py "Input Images/toi.png"
```

Có thể điều chỉnh ngưỡng bằng `--threshold`, ví dụ:

```powershell
python BTTL3/Code/sobel.py "Input Images/toi.png" --threshold 40
python BTTL3/Code/laplace.py "Input Images/toi.png" --threshold 1
```

Ảnh kết quả và hình so sánh các mặt nạ được lưu trong `BTTL3/Code/ket_qua_bai3`.

## 5. Ảnh JPG dùng trong báo cáo

Các ảnh JPG đã nén được lưu trong `anh_jpg`. Ảnh PNG gốc vẫn nằm trong các thư mục kết quả của từng bài.
