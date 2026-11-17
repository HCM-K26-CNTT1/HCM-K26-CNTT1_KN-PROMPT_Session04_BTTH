# **BÀI TẬP THỰC HÀNH TỔNG HỢP – SESSION 04**

**Chủ đề: Ứng dụng Kỹ thuật Prompting Nâng cao (Logic & Chuỗi)**

## **1. Phân tích và thiết kế giải pháp**

**Bối cảnh:** Xây dựng chatbot AI hỗ trợ cửa hàng online tự động tiếp nhận, kiểm tra và xử lý đơn hàng.

**Input:** Họ tên, số điện thoại, địa chỉ, tên sản phẩm, số lượng, đơn giá.

**Output:** Thông tin đơn hàng, tổng tiền, trạng thái và hướng xử lý.

Giải pháp sử dụng Prompt Chaining gồm 3 bước:

- Bước 1: Kiểm tra và chuẩn hóa dữ liệu.
- Bước 2: Tính toán tổng tiền.
- Bước 3: Tổng hợp và phân loại đơn hàng.

## **2. Prompt hệ thống và Prompt thực thi**

```
Bạn là AI quản lý đơn hàng online.

Thực hiện tuần tự 3 bước:
1. Kiểm tra dữ liệu khách hàng và sản phẩm.
2. Tính tổng tiền nếu số lượng và đơn giá hợp lệ.
3. Phân loại đơn hàng và đề xuất hướng xử lý.

Quy tắc:
- Không tự suy đoán dữ liệu bị thiếu.
- Nếu dữ liệu sai định dạng, phải thông báo lỗi.
- Không tính toán khi dữ liệu không hợp lệ.
- Lưu kết quả từng bước để tránh đứt gãy ngữ cảnh.
- Chỉ trả về kết quả cuối cùng theo cấu trúc rõ ràng.
```

## **3. Kết quả chạy thử**

**Input:**

- Khách hàng: Nguyễn Văn An.
- Sản phẩm: Chuột không dây.
- Số lượng: 2.
- Đơn giá: 150.000 đồng.
- Địa chỉ: Để trống.

**Output AI:**

```
KẾT QUẢ XỬ LÝ ĐƠN HÀNG

- Họ tên: Nguyễn Văn An.
- Sản phẩm: Chuột không dây.
- Số lượng: 2.
- Đơn giá: 150.000 đồng.
- Tổng tiền: 300.000 đồng.
- Địa chỉ: Thiếu thông tin.

Trạng thái: CẦN BỔ SUNG.

Hướng xử lý: Yêu cầu khách hàng cung cấp
địa chỉ trước khi xác nhận đơn hàng.
```
