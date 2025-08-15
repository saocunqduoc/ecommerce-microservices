
# Quy tắc Đặt Tên Branch trong Microservices

## Mục tiêu
- Giúp mọi người trong dự án dễ hiểu, thống nhất và quản lý branch hiệu quả.
- Tránh trùng lặp và giúp dễ dàng tìm kiếm lịch sử phát triển.

## 1. Cấu trúc chung
```
<type>/<service-name>/<task-id>-<short-description>
```
### 1.1. Giải thích
- **`<type>`**: Loại thay đổi hoặc mục đích của branch
- **`<service-name>`**: Tên service/module mà branch này ảnh hưởng (viết thường, dùng `-` để nối từ)
- **`<task-id>`**: ID của task/ticket trong hệ thống quản lý công việc (Jira, Trello, GitHub Issues...)
- **`<short-description>`**: Mô tả ngắn gọn nội dung công việc nếu cần (viết thường, dùng `-` để nối từ)

---

## 2. Danh sách type hợp lệ
| Type         | Ý nghĩa                                                                 |
|--------------|------------------------------------------------------------------------|
| `feat`       | Thêm chức năng mới                                                     |
| `fix`        | Sửa lỗi                                                                |
| `hotfix`     | Sửa lỗi khẩn cấp trên môi trường production                            |
| `refactor`   | Tái cấu trúc mã nguồn, không thay đổi hành vi                          |
| `chore`      | Công việc linh tinh (update config, thư viện, script...)               |
| `test`       | Thêm hoặc sửa test                                                     |
| `docs`       | Thêm hoặc sửa tài liệu                                                 |
| `perf`       | Cải thiện hiệu năng                                                    |
| `style`      | Thay đổi về format/code style, không ảnh hưởng logic                   |

---

## 3. Ví dụ minh họa
| Branch name                                             | Ý nghĩa                                                         |
|--------------------------------------------------------|----------------------------------------------------------------|
| `feat/order-service/1234-add-cancel-order`             | Thêm chức năng hủy đơn hàng cho `order-service`, task #1234    |
| `fix/user-service/5678-fix-email-validation`           | Sửa lỗi validate email trong `user-service`, task #5678        |
| `hotfix/payment-service/9876-fix-payment-callback`     | Sửa gấp lỗi callback thanh toán trong `payment-service`        |
| `refactor/product-service/1122-cleanup-unused-methods` | Xóa hàm không dùng trong `product-service`, task #1122         |
| `docs/auth-service/3344-update-api-docs`               | Cập nhật tài liệu API cho `auth-service`, task #3344           |

---

## 4. Quy tắc bổ sung
1. **Tất cả chữ đều viết thường** (lowercase).
2. **Dùng dấu gạch ngang `-`** để nối các từ trong `service-name` và `short-description`.
3. **Không dùng khoảng trắng hoặc ký tự đặc biệt**.
4. Mỗi branch chỉ nên giải quyết **1 mục tiêu rõ ràng** (liên quan 1 task cụ thể).
5. Sau khi merge, **xóa branch** để tránh rác trong repository.
