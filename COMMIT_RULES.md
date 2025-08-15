
# Quy tắc Commit

## 1. Cấu trúc Commit Message
```
<type>(<scope>): <short summary>
```
- **type**: Loại commit
- **scope**: Phạm vi (module, feature, file...)
- **short summary**: Mô tả ngắn gọn, tối đa 50 ký tự

## 2. Các loại type
- **feat**: Thêm tính năng mới
- **fix**: Sửa lỗi
- **docs**: Thay đổi tài liệu
- **style**: Thay đổi định dạng, code style (không ảnh hưởng logic)
- **refactor**: Chỉnh sửa mã nhưng không thay đổi chức năng
- **perf**: Cải thiện hiệu năng
- **test**: Thêm/sửa test
- **chore**: Công việc linh tinh (build, config...)

## 3. Quy tắc viết
- Sử dụng tiếng Anh hoặc tiếng Việt nhất quán
- Viết ở thì hiện tại: "add" không phải "added"
- Không viết hoa chữ cái đầu type
- Không kết thúc summary bằng dấu chấm
- Mỗi commit chỉ nên chứa 1 mục đích thay đổi

## 4. Ví dụ
```
feat(auth): add JWT authentication
fix(ui): button not aligned correctly
docs(readme): update installation guide
```
