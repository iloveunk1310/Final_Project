# Ứng dụng BERTopic trong Phân tích Chủ đề Tài liệu tiếng Việt
(NLP Final Project)

## Giới thiệu
Đồ án này tập trung vào việc tái hiện và áp dụng mô hình **BERTopic** để trích xuất và phân tích các chủ đề ẩn trong tập dữ liệu lịch sử chuyên biệt: **"Lịch sử Việt Nam"**. 

Thay vì sử dụng thư viện `bertopic` có sẵn một cách thụ động, nhóm thực hiện đã xây dựng một class tùy chỉnh `SimpleBERTopic` để tái hiện luồng xử lý (pipeline) của thuật toán gốc, bao gồm các bước: Embedding, Dimensionality Reduction (UMAP), Clustering (HDBSCAN), và Class-based TF-IDF (c-TF-IDF).

Mời thầy sử dụng link https://www.kaggle.com/code/minhnewbi/bertopic-full để chạy code (Vì chạy local sẽ không đảm bảo thư viện phù hợp)
## Thành viên nhóm
| STT | Họ và Tên | MSSV |
|:---:|:---|:---|
| 1 | Lê Hải Đăng | 23122005 |
| 2 | Nguyễn Nhật Minh | 23122010 |
| 3 | Nguyễn Văn Khoa | 23122016 |
| 3 | Bùi Anh Quân | 23122017 |

## Các thư viện cần thiết
pip install bertopic sentence-transformers underthesea langchain transformers scikit-learn gensim umap-learn hdbscan

## Cách kiểm tra mô hình
Chạy hết tất cả cell để đảm bảo code chạy đầy đủ.

Để test với mô hình bất kỳ, thay thế tên mô hình vào biến embedding_model: v_bert = SimpleBERTopic(embedding_model = "dangvantuan/vietnamese-embedding", verbose = False)

Để test với data bất kỳ, đọc data (gồm list các ngữ liệu thô) và thay thế vào biến documents: v_bert.fit_transform(documents_ = data_ans)

Các hàm chức năng có hướng dẫn trong class.
