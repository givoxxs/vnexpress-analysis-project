# Dự án Phân tích Dữ liệu Báo VnExpress

Dự án này thực hiện phân tích bài báo từ VnExpress, tập trung vào hai lĩnh vực chính: **Công nghệ** và **Khoa học**. Mục tiêu là phân loại các bài báo dựa trên nội dung và đặc điểm của chúng.

## Giới thiệu

Dự án sử dụng kỹ thuật khai phá dữ liệu và học máy để:
- Phân tích đặc điểm của bài viết thuộc hai nhóm Công nghệ và Khoa học
- Xây dựng các đặc trưng để phân biệt giữa hai nhóm
- Áp dụng các mô hình phân loại để tự động nhận dạng chủ đề của bài viết

## Cấu trúc dự án

```
vnexpress-analysis-project/
├── clean_data/                 # Dữ liệu sau khi đã xử lý
│   ├── vnexpress_clean_data.csv
│   ├── vnexpress_encoded_data.csv
│   └── vnexpress_featured_data.csv
├── notebooks/                  # Jupyter notebooks phân tích
│   ├── 01_data_overview.ipynb  # Tổng quan dữ liệu
│   ├── 02_data_visualization.ipynb  # Khám phá dữ liệu
│   ├── 03_data_cleaning.ipynb  # Làm sạch dữ liệu
│   ├── 04_data_encoding.ipynb  # Mã hóa dữ liệu
│   ├── 05_feature_engineering.ipynb  # Xây dựng đặc trưng
│   ├── 06_multivariate_analysis.ipynb  # Phân tích đa biến
│   └── 07_conclusion_feasibility.ipynb  # Kết luận và đánh giá
├── raw_data/                   # Dữ liệu thô ban đầu
│   └── vnexpress_raw_data.csv
└── README.md                   # Tài liệu hướng dẫn
```

## Dữ liệu

Dữ liệu gốc gồm các bài báo được thu thập từ VnExpress có các trường:
- `title`: Tiêu đề bài viết
- `description`: Mô tả ngắn gọn về nội dung
- `content`: Nội dung bài viết
- `group`: Danh mục bài viết (Công nghệ, Khoa học)
- `category`: Thể loại bài viết chi tiết
- `date`: Ngày xuất bản bài viết
- `author`: Tác giả bài viết
- `url`: Đường dẫn đến bài viết
- `thumbnail`: Đường dẫn đến hình ảnh đại diện bài viết
- `nums_of_comments`: Số lượng bình luận

## Các bước phân tích dữ liệu

### 1. Tổng quan dữ liệu
Hiểu cấu trúc dữ liệu, phân bố các nhóm bài viết và khám phá đặc điểm dữ liệu.

### 2. Khám phá dữ liệu 

### 3. Làm sạch dữ liệu
Tiền xử lý dữ liệu: xử lý giá trị thiếu, chuẩn hóa văn bản và chuyển đổi định dạng ngày tháng.

### 4. Mã hóa dữ liệu
Chuyển đổi dữ liệu văn bản thành các đặc trưng số sử dụng TF-IDF, mã hóa các biến danh mục.

### 5. Xây dựng đặc trưng
Tạo các đặc trưng mới từ dữ liệu hiện có, như tỷ lệ tiêu đề/nội dung, thời gian đăng bài, độ phức tạp văn bản.

### 6. Phân tích đa biến
Phân tích mối quan hệ giữa các đặc trưng, trực quan hóa phân bố dữ liệu.

### 7. Đánh giá khả thi và kết luận
Tổng hợp kết quả phân tích, đánh giá khả năng phân loại bài viết.

## Hướng dẫn chạy chương trình

### Yêu cầu cài đặt
```
Python 3.8+
Jupyter Notebook
pandas
numpy
matplotlib
seaborn
scikit-learn
nltk
```

### Trình tự thực hiện

1. **Thiết lập môi trường**:
   ```bash
   # Tạo môi trường ảo (khuyến nghị)
   python -m venv venv
   
   # Kích hoạt môi trường ảo
   # Windows
   venv\Scripts\activate
   # Linux/Mac
   source venv/bin/activate
   
   # Cài đặt các thư viện cần thiết
   pip install pandas numpy matplotlib seaborn scikit-learn nltk jupyter
   ```

2. **Chạy các notebook theo thứ tự**:
   - Đầu tiên, khởi động Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
   - Mở và thực thi các notebook theo trình tự:
     1. `01_data_overview.ipynb`: Hiểu về dữ liệu
     2. `02_data_visualization.ipynb`: Khám phá dữ liệu (tạo file `vnexpress_raw_data.csv`)
     3. `03_data_cleaning.ipynb`: Làm sạch dữ liệu (tạo file `vnexpress_clean_data.csv`)
     4. `04_data_encoding.ipynb`: Mã hóa dữ liệu (tạo file `vnexpress_encoded_data.csv`)
     5. `05_feature_engineering.ipynb`: Xây dựng đặc trưng (tạo file `vnexpress_featured_data.csv`)
     6. `06_multivariate_analysis.ipynb`: Phân tích đa biến
     7. `07_conclusion_feasibility.ipynb`: Kết luận và đánh giá khả thi

3. **Lưu ý khi chạy**:
   - Đảm bảo các notebook được chạy theo đúng thứ tự từ 1 đến 7
   - Mỗi notebook sẽ tạo ra các file dữ liệu trung gian trong thư mục `clean_data/`
   - Kiểm tra kết quả đầu ra của mỗi bước trước khi tiến hành bước tiếp theo

## Kết quả chính

- Xác định được các đặc trưng quan trọng giúp phân biệt bài viết Công nghệ và Khoa học
- Phân tích tương quan giữa các đặc trưng và nhóm bài viết
- Giảm chiều dữ liệu để trực quan hóa và cải thiện hiệu suất mô hình
- Đánh giá khả năng phân loại dựa trên các đặc trưng đã được xây dựng

## Tác giả

- **Phan Văn Toàn** 
- **Trương Xuân Phúc**
- **Ngô Thị Kim Ly**

## Tài liệu tham khảo
- [Scikit-learn documentation](https://scikit-learn.org/stable/documentation.html)
- [Natural Language Processing with Python](https://www.nltk.org/book/)
- [Pandas documentation](https://pandas.pydata.org/docs/)
- [VnExpress](https://vnexpress.net/)
- [Vietnamese Stopword](https://github.com/stopwords/vietnamese-stopwords/tree/master)
