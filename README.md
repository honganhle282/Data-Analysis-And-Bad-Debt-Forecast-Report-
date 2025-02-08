# **Phân Tích Dữ Liệu Tài Chính & Dự Báo Nợ Xấu**

## **1. Giới thiệu**
Dự án phân tích dữ liệu tài chính của một công ty cho vay tiêu dùng nhằm đánh giá hiệu quả hoạt động, nhận diện rủi ro tín dụng và xây dựng mô hình dự báo nợ xấu.

## **2. Tổng quan dữ liệu**
- **Tổng tiền cho vay**: 30 tỷ VND, tỷ lệ giải ngân 92%.
- **Phân khúc**: Khoản vay trung bình ~12.84 triệu VND, tập trung vào khách hàng cá nhân.
- **Thị trường**: 85% khách hàng tại Hà Nội, các khu vực khác chưa khai thác mạnh.
- **Số khách hàng**: 1.861 khách hàng với 2.374 khoản vay, cho thấy xu hướng vay nhiều lần.
![image](https://github.com/user-attachments/assets/c893493c-2e1e-4bec-a3d6-d8b24eb37a0a)
![image](https://github.com/user-attachments/assets/f8d74014-fc03-4168-bd30-f55c2fe147e0)


## **3. Mô hình dự báo nợ xấu**
Sử dụng **SVM** để phân loại khách hàng có nguy cơ nợ xấu với các kết quả chính:

- **Accuracy**: `92%`
- **Recall (nợ xấu)**: `97%` (mô hình nhận diện tốt các trường hợp nợ xấu).
- **Precision (nợ xấu)**: `58%` (cần cải thiện để giảm dự đoán sai dương).
- **AUC**: `0.99` (khả năng phân biệt nợ xấu rất tốt).
  ![image](https://github.com/user-attachments/assets/f2a07232-2680-4a8d-9d98-d2c3e734a603)


### **Các đặc trưng quan trọng**
- `CreditInfo` (thông tin tín dụng)
- `ReceiveYourIncomeSalary` (thu nhập)
- `Address` (địa chỉ cư trú)

## **4. Chẩn đoán & Đề xuất**
### **Quản lý rủi ro tín dụng**
- Xác định khách hàng có **điểm tín dụng thấp (<500)** và thu nhập thấp để áp dụng xét duyệt chặt chẽ hơn.
- Tăng cường theo dõi khách hàng **thanh toán trễ (13,33%)** bằng **SMS/email nhắc nhở**.
- Tạo **chính sách hỗ trợ** như gia hạn nợ hoặc giảm lãi suất cho khách hàng khó khăn.

### **Mở rộng thị trường & tối ưu danh mục sản phẩm**
- Phát triển **gói vay ưu đãi** cho **nhóm thu nhập thấp nhưng ổn định** *(nhân viên chính thức, tự doanh)*.
- Khai thác **khách hàng nữ** vì có tỷ lệ nợ xấu thấp hơn.
- Đa dạng hóa sản phẩm để giảm rủi ro từ nhóm vay `"cầm cố điện thoại"`, `"vay theo sim"`.

## **5. Hướng phát triển**
- Cải thiện mô hình bằng cách thử nghiệm **Random Forest, XGBoost**.
- Sử dụng thêm **AI/ML** để phân tích hành vi khách hàng và dự đoán sớm rủi ro tín dụng.
- Mở rộng hoạt động sang **TP.HCM** và các tỉnh để giảm phụ thuộc vào Hà Nội.

## **6. Công nghệ sử dụng**
- **Ngôn ngữ**: Python
- **Thư viện chính**: `pandas`, `scikit-learn`, `seaborn`, `matplotlib`, `XGBoost`
- **Môi trường**: Google Colab
