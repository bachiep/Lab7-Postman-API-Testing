# LAB 7 - KIỂM THỬ REST API VỚI POSTMAN

## Thông tin sinh viên

- **Họ và tên:** Lưu Đức Hiệp
- **Mã sinh viên:** 23010437
- **Môn học:** Đánh giá và kiểm định chất lượng phần mềm
- **Công cụ:** Postman / Newman

## 1. Mục tiêu

Bài thực hành sử dụng Postman để tạo và chạy các kịch bản kiểm thử REST API. Bộ kiểm thử thực hiện các phương thức HTTP phổ biến, kiểm tra mã trạng thái, cấu trúc dữ liệu JSON, dữ liệu phản hồi và thời gian đáp ứng.

API được kiểm thử:

```text
https://jsonplaceholder.typicode.com
```

## 2. Danh sách kịch bản kiểm thử

| Mã | Phương thức | Endpoint | Kết quả mong đợi |
|---|---|---|---|
| TC01 | GET | `/posts` | Trả về 100 bài viết, status 200 |
| TC02 | GET | `/posts/1` | Trả về bài viết có ID bằng 1 |
| TC03 | GET | `/posts?userId=1` | Tất cả bài viết thuộc user 1 |
| TC04 | GET | `/posts/9999` | Trả về status 404 |
| TC05 | POST | `/posts` | Tạo dữ liệu thành công, status 201 |
| TC06 | PUT | `/posts/1` | Cập nhật toàn bộ dữ liệu, status 200 |
| TC07 | PATCH | `/posts/1` | Cập nhật một phần dữ liệu, status 200 |
| TC08 | DELETE | `/posts/1` | Xóa dữ liệu thành công, status 200 |

## 3. Kết quả thực thi

Bộ kiểm thử đã được chạy bằng Postman Collection Runner tương thích qua Newman:

- **Requests:** 8/8 thành công
- **Test scripts:** 8/8 thành công
- **Assertions:** 21/21 đạt
- **Failed:** 0
- **Tỷ lệ thành công:** 100%
- **Thời gian chạy:** khoảng 3 giây

## 4. Kiến thức áp dụng

- Tạo collection và environment trong Postman.
- Sử dụng biến `{{baseUrl}}`.
- Gửi request GET, POST, PUT, PATCH và DELETE.
- Viết test script bằng `pm.test` và `pm.expect`.
- Kiểm tra status code, response time, Content-Type và response body.
- Chạy tự động toàn bộ collection và tổng hợp kết quả.

## 5. Tài liệu tham khảo

- [Video hướng dẫn Postman trong đề bài](https://www.youtube.com/watch?v=MFxk5BZulVU)
- [JSONPlaceholder](https://jsonplaceholder.typicode.com/)

> Minh chứng hình ảnh sẽ được bổ sung trong commit tiếp theo.
