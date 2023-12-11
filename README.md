# GIT và GITHUB
### _1. Khởi tạo_
Lệnh git init được sử dưng để tạo, khởi tạo một kho chứa Git mới (Git Repo) ở local
```sh
git init
```

### _2. Chuẩn bị cho commit (add)_
Lệnh git add sử dụng để __đánh chỉ mục (index)__ các nội dung mới, mới cập nhật trong thư mục làm việc, nó chuẩn bị nội dung sắp xếp cho lần commit tiếp theo.

Khái niệm đánh chỉ mục ở trên có nghĩa là lưu lại ảnh chụp (snapshot) thông tin thay đổi của thư mục làm việc so với lần commit trước (hoặc so với snapshot chưa commit), snapshot lưu ở khu vực gọi là staging (sắp xếp, chuẩn bị)
* __Đưa vào vùng staging file, thư mục cụ thể__
```sh
git add file1 file2 dir1 dir2 ...
```
* __Đưa vào vùng staging toàn bộ thư mục làm việc__
```sh
git add --all
# Hoặc
git add -A
# Hoặc add [thư mục hiện tại]
git add .
```
### _3. Thực hiện commit_
Lệnh git commit thực hiện lưu vào CSDL Git toàn bộ nội dung chứa trong index (vùng staging) và kèm theo nó là một đoạn text thông tin (log) mô tả sự thay đổi của của commit này so với commit trước. Sau khi commit con trỏ HEAD tự động dịch chuyển đến commit này.
* __Thực hiện commit cơ bản__
```sh
git commit -m "Ghi chú về commit"
```
* __Thực hiện commit với tham số -a:__
  Khi cho tham số -a thì nó tương đương thực hiện lệnh git add để đưa các file đang được giám sát có sự thay đổi vào staging rồi tự động chạy git commit
```sh
git commit -a -m "Ghi chú về commit"
```