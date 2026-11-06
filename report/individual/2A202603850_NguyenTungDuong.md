# Báo cáo cá nhân — Day 01: Lọc tin nhắn rác bằng ML, DL, Embedding và LLM

> Đổi tên file này thành `MSSV_HoTen.md` của bạn, ví dụ `2A20260000_NguyenVanAn.md`, rồi điền từng mục. Xoá các dòng hướng dẫn in nghiêng khi xong.

- **MSSV:**
- **Họ và tên:**
- **SEED** (in ở ô đầu notebook):

## 1. Bằng chứng

| Tệp | Có? |
| --- | --- |
| [`day01_lab.ipynb`](day01_lab.ipynb) — notebook đã chạy, còn output | ☐ |
| [`lab1_report.json`](lab1_report.json) — do ô "Báo cáo cuối" sinh ra | ☐ |
| [`hand_calc.jpg`](hand_calc.jpg) — ảnh tính tay có các bước | ☐ |

## 2. Kết quả chính

*Chép bảng so sánh cuối Phần 5 (F1 test, F1 SUB 40, p95 ms/tin, USD/1k tin) của chính bạn.*

## 3. Dự đoán và thực tế

Chạy lại với lr = 0.001 và lr = 50. Dự đoán trước hình dạng đường loss,dự đoán 0.001 kết quả 0.007 vì ở lr=50 loss không bị phân kỳ hay bùng nổ mà lại giảm cực kỳ nhanh và đạt giá trị loss cuối rất nhỏ 
## 4. Phân tích 50 case khó

Model tụt nhiều nhất: Mô hình Bag-of-Words (BoW) hoặc mô hình truyền thống (logistic regression/embedding đơn thuần) là nhóm sụt giảm độ chính xác (accuracy) nghiêm trọng nhất trên tập 50 case khó này, trong khi các LLM (như Gemini/OpenAI) duy trì tỷ lệ chính xác tốt hơn nhờ khả năng hiểu ngữ nghĩa ngữ cảnh sâu.

Nhóm case tụt mạnh nhất:Nhóm obfuscation (tin nhắn cố tình viết biến đổi ký tự, chèn khoảng trắng hoặc dùng từ lóng để né bộ lọc) và nhóm ham_looks_spam (tin nhắn thông thường nhưng chứa các từ khóa nhạy cảm dễ gây hiểu lầm).
Đối với các mô hình truyền thống dựa vào tần suất từ, các nhóm này gây ra sai sót hàng loạt vì chúng chỉ đếm từ khóa mà không đọc được ngữ cảnh bẻ lái của câu.

## 5. Thử thách cá nhân



## 6. Phương án cho sản phẩm thật

sử dụng kết hợp cả 2 LM(p<0.3 p>0.7) và 
LLM(p [0.3,0.7]),đánh đổi lại thì hệ thống phức tạp hơn và độ chính xác tối đa giảm nhỏ

## 7. AI log và điều đã học


