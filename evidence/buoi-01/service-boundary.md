# Service Boundary của nhóm

## 1. Thông tin nhóm

- Tên nhóm: nhóm 11    
- Lớp:cntt 17-09    
- Thành viên: Trần Văn Huy
- Service nhóm phụ trách: IoT Ingestion
- Sản phẩm tổng thể của lớp: Smart Campus Operations Platform

## 2. Actor

Thiết bị IoT: gửi dữ liệu cảm biến lên hệ thống.

Quản trị viên hệ thống: quản lý và giám sát thiết bị, dữ liệu.

Hệ thống Smart Campus: nhận và xử lý dữ liệu từ IoT Ingestion Service.

Ứng dụng giám sát (Dashboard): hiển thị dữ liệu và trạng thái hệ thống.

## 3. System Boundary

Phần nhóm kiểm soát:

Nhận dữ liệu từ các thiết bị IoT

Xử lý và chuẩn hóa dữ liệu

Gửi dữ liệu vào hệ thống Smart Campus

Phần nhóm chỉ tích hợp:

Thiết bị IoT (cảm biến, camera, thiết bị đo)

Hệ thống phân tích dữ liệu và lưu trữ

Dashboard hiển thị dữ liệu cho người dùng
## 4. Service Boundary

Service có trách nhiệm:

Thu thập dữ liệu từ các thiết bị IoT

Xử lý và chuyển dữ liệu vào hệ thống Smart Campus

Service không làm:

Phân tích dữ liệu chi tiết

Lưu trữ dữ liệu lâu dài

Hiển thị dữ liệu trên giao diện người dùng

## 5. Input / Output

### Input

- Dữ liệu từ các thiết bị IoT (nhiệt độ, độ ẩm, ánh sáng, chuyển động)

### Output

- Dữ liệu đã xử lý gửi đến hệ thống Smart Campus hoặc hệ thống phân tích dữ liệu

## 6. API dự kiến

| Method | Endpoint | Mục đích                     |
| ------ | -------- | ---------------------------- |
| GET    | /health  | Kiểm tra trạng thái service  |
| POST   | /data    | Nhận dữ liệu từ thiết bị IoT |
| GET    | /devices | Lấy danh sách thiết bị IoT   |


## 7. Phụ thuộc service khác

Service này gọi đến service nào?

Data Storage Service (lưu trữ dữ liệu IoT)

Analytics Service (phân tích dữ liệu)

Service nào gọi đến service này?

Thiết bị IoT (gửi dữ liệu cảm biến)

Smart Campus Management System

## 8. Sơ đồ minh họa

<img width="1460" height="351" alt="image" src="https://github.com/user-attachments/assets/adf7e570-6166-4373-82ec-81469c09dcd6" />

