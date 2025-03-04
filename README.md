# README: cmi-pciat-feature
Cuộc thi: Child Mind Institute — Problematic Internet Use
Relating Physical Activity to Problematic Internet Use

## Thành viên nhóm 4 lớp 2425I_INT3405E_55
- Trần Ngọc Huy     (ID: 22028049)
- Nguyễn Duy Khánh  (ID: 22028030)
- Nguyễn Duy Hưng   (ID: 22028264)

## Mục tiêu
Mục tiêu là phát triển một mô hình dự đoán để ước tính mức độ sử dụng Internet có vấn đề ở trẻ em và thanh thiếu niên dựa trên dữ liệu về hoạt động thể chất và thể lực của chúng. Điều này nhằm mục đích phát hiện sớm các dấu hiệu của việc sử dụng Internet không lành mạnh và cho phép can thiệp kịp thời để thúc đẩy thói quen kỹ thuật số lành mạnh hơn.

## Dữ liệu huấn luyện
1. **Dữ liệu bảng (tabular)**: Gồm 3.960 bản ghi của trẻ em và thanh thiếu niên với 81 cột (không bao gồm cột ID).
2. **Dữ liệu chuỗi thời gian (time series)**: Bao gồm 996 tệp định dạng Parquet.

## Các công cụ và thư viện sử dụng
- **Python Libraries**: pandas, numpy, sklearn, matplotlib, seaborn, plotly, lightgbm, xgboost, catboost, keras, torch, eli5, và nhiều thư viện khác.
- **Mục tiêu chính**:
  - Chuẩn hóa và tiền xử lý dữ liệu.
  - Xây dựng mô hình học máy (LightGBM, XGBoost, CatBoost) và học sâu.
  - Đánh giá và tối ưu hóa các mô hình thông qua các kỹ thuật như Cross-Validation và StratifiedKFold.

## Nội dung chính
### 1. **Nhập các thư viện và thiết lập ban đầu**
- Import các thư viện cần thiết cho việc xử lý dữ liệu, trực quan hóa, và xây dựng mô hình.
- Tắt các cảnh báo không cần thiết để tăng tính rõ ràng cho Notebook.

### 2. **Khám phá và tiền xử lý dữ liệu**
- Tải và phân tích cấu trúc dữ liệu.
- Xử lý thiếu dữ liệu bằng các kĩ thuật học máy.
- Chuẩn hóa các đặc trưng.

### 3. **Xây dựng và huấn luyện mô hình**
- Mô hình được triển khai bao gồm:
  - **Regressors**: LightGBM, XGBoost, CatBoost, Random Forest, Gradient Boosting.
  - **Voting Regressor** để kết hợp các mô hình mạnh nhất.
  - **Autoencoder** và **Torch Neural Networks** cho phân tích học sâu.
- Sử dụng các công cụ đánh giá hiệu năng:
  - **Cohen Kappa Score**.
  - Cross-Validation.
  - Permutation Importance. 

### 4. **Trực quan hóa**
- Sử dụng Plotly, Matplotlib, và Seaborn để tạo biểu đồ trực quan về dữ liệu và hiệu suất mô hình.

### 5. **Tối ưu hóa**
- Sử dụng các kỹ thuật học máy để tối ưu hóa các thông số.
- Triển khai các phương pháp ensemble để cải thiện dự đoán.

## Hướng dẫn sử dụng
1. Cài đặt các thư viện phụ thuộc.
2. Chạy lần lượt từng ô (cell) trong Notebook.
3. Điều chỉnh tham số mô hình hoặc thử nghiệm các mô hình khác trong các bước huấn luyện.

## Đầu ra
- Kết quả dự đoán SII cho các bộ dữ liệu thử nghiệm.
- Kết quả cuối cùng: QWK = 0,438.
