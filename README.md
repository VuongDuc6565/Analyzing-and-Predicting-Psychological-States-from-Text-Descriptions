# Phân Tích và Dự Đoán Trạng Thái Tâm Lý Qua Miêu Tả Dạng Văn Bản

## Giới thiệu
Đây là sản phẩm thực nghiệm môn **Học Máy** tại **Trường Đại học Khoa học Tự nhiên – ĐHQGHN**, với mục tiêu xây dựng một hệ thống phân tích và dự đoán trạng thái tâm lý từ văn bản ngắn tiếng Anh.

## Thành viên thực hiện
- **Trần Anh Minh** – Giảm chiều dữ liệu. Mô hình Random Forest  
- **Dương Đức Vương** – Mô hình hồi quy Softmax và MLP (Artificial Neural Network)  
- **Nguyễn Tuấn Kiệt** – Mô hình Multinomial Naive Bayes và K-Means

## Cấu trúc thư mục
```
├── src/Data_Preprocessing_and_Visualization/                  # Giảm chiều, trực quan hóa dữ liệu
├── src/K_Means/                     # Code phân cụm K-Means
├── src/Naive_Bayes_And_Softmax_Regression/                 # Code huấn luyện mô hình Multinomial Naive Bayes và mô hình hồi quy Softmax
├── src/MULTI_LAYER_PERCEPTRON/     # Code huấn luyện mạng neuron nhân tạo (ANN)
├── src/Random_forest_classifier/   # Code mô hình rừng ngẫu nhiên
```

## Dữ liệu
Bộ dữ liệu sử dụng: **Sentiment Analysis for Mental Health** (Kaggle)  
- Link tải: [Google Drive](https://drive.google.com/file/d/12nfzfXYr4v_eEZKk2aZLNxjOcql-35oY/view?usp=sharing)

Gồm các nhãn:
- `Normal`, `Depression`, `Anxiety`, `Stress`, `Bipolar`, `Personality disorder`

## Quy trình thực hiện
1. **Tiền xử lý dữ liệu**: xoá dòng trống, chuẩn hoá chữ thường, loại bỏ ký tự đặc biệt, stemming, resampling.
2. **Vector hoá văn bản**: Bag of Words / TF-IDF.
3. **Giảm chiều dữ liệu**: PCA, LDA.
4. **Phân cụm không giám sát**: K-Means.
5. **Huấn luyện mô hình phân loại**:
   - Multinomial Naive Bayes
   - Hồi quy Softmax
   - Mạng neuron nhân tạo (ANN)
   - Rừng ngẫu nhiên (Random Forest)
6. **Đánh giá mô hình**: Accuracy, F1-Score, Confusion Matrix.

## Kết quả nổi bật
| Mô hình           | F1-Score cao nhất |
|-------------------|------------------|
| Random Forest     | ~0.95            |
| ANN (MLP)         | ~0.94            |
| Softmax           | ~0.93            |
| Naive Bayes       | ~0.85            |

## Hướng dẫn chạy
1. Cài đặt Python ≥ 3.8 và các thư viện: `scikit-learn`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `torch`
2. Chạy file tương ứng trong từng thư mục để huấn luyện mô hình hoặc thử nghiệm.

## Ghi chú
Dự án được thực hiện trong khuôn khổ học phần, do đó có thể còn hạn chế về hiệu suất và tối ưu hoá mô hình.
