# BÀI LÀM – HACKATHON 02

- **Mã đề:** 06
- **Họ tên:** Nguyễn Tiến Duy
- **Lớp:** Cntt1
- **Link repository:**https://github.com/ngtienduy272008vn-gif/HN-KS26-CNTT1_Nhap-mon-CNTT_Hackathon02
- **Hệ điều hành (Windows/macOS):** MacOS

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
# Ghi lần lượt các lệnh đã chạy, mỗi lệnh một dòng
cd
pwd
ls -la
mv yeu_cau_khach_hang.txt doc/
 mkdir backup
 cp data/don_in_thang_6.xlsx backup/
 rm temp_606.tmp
 cd logs
  ls -la
  cd .. 
  ls -laR
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text

total 0
drwxr-xr-x   7 root     admin   224 Oct 21 17:52 .
drwxr-xr-x  22 root     wheel   704 Jun 25 09:29 ..
-rw-r--r--   1 root     wheel     0 Jun 25 09:29 .localized
drwxrwxrwt   5 root     wheel   160 Aug  5 02:07 Shared
drwxr-x---+ 13 duy      staff   416 Oct 29 19:22 duy
drwxr-x---+ 33 macbook  staff  1056 Nov 11 07:51 macbook
drwxr-xr-x   2 macbook  admin    64 Oct 21 17:52 thư mục không có tiêu đề

./Shared:
total 0
drwxrwxrwt  5 root     wheel  160 Aug  5 02:07 .
drwxr-xr-x  7 root     admin  224 Oct 21 17:52 ..
-rw-r--r--  1 macbook  staff    0 Jul 24 11:04 .betamigrated
-rw-r--r--  1 root     wheel    0 Jun 25 09:29 .localized
drwxrwxrwx@ 2 macbook  wheel   64 Aug  5 02:07 SC Info

./Shared/SC Info:
total 0
drwxrwxrwx@ 2 macbook  wheel   64 Aug  5 02:07 .
drwxrwxrwt  5 root     wheel  160 Aug  5 02:07 ..

./duy:
total 32
drwxr-x---+ 13 duy   staff    416 Oct 29 19:22 .
drwxr-xr-x   7 root  admin    224 Oct 21 17:52 ..
-r--------   1 duy   staff      9 Oct 21 15:13 .CFUserTextEncoding
-rw-r--r--@  1 duy   staff  10244 Nov 10 19:32 .DS_Store
drwx------+  2 duy   staff     64 Oct 21 15:15 .Trash
drwx------+  3 duy   staff     96 Oct 20 21:31 Desktop
drwx------+  3 duy   staff     96 Oct 20 21:31 Documents
drwx------+  3 duy   staff     96 Oct 20 21:31 Downloads
drwx------+ 76 duy   staff   2432 Oct 21 20:06 Library
drwx------   4 duy   staff    128 Oct 26 20:43 Movies
drwx------+  3 duy   staff     96 Oct 20 21:31 Music
drwx------+  4 duy   staff    128 Oct 21 15:13 Pictures
drwxr-xr-x+  4 duy   staff    128 Oct 20 21:31 Public

./duy/.Trash:
total 0
ls: ./duy/.Trash: Operation not permitted

./duy/Desktop:
total 0
ls: ./duy/Desktop: Permission denied

./duy/Documents:
total 0
ls: ./duy/Documents: Permission denied

./duy/Downloads:
total 0
ls: ./duy/Downloads: Permission denied

./duy/Library:
total 0
ls: ./duy/Library: Permission denied

./duy/Movies:
total 0
ls: ./duy/Movies: Permission denied

./duy/Music:
total 0
ls: ./duy/Music: Permission denied

./duy/Pictures:
total 0
ls: ./duy/Pictures: Permission denied

./duy/Public:
total 0
drwxr-xr-x+  4 duy  staff  128 Oct 20 21:31 .
drwxr-x---+ 13 duy  staff  416 Oct 29 19:22 ..
-rw-r--r--   1 duy  staff    0 Oct 20 21:31 .localized
drwx-wx-wx+  3 duy  staff   96 Oct 20 21:31 Drop Box

./duy/Public/Drop Box:
total 0
ls: ./duy/Public/Drop Box: Permission denied

```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng status=500


```shell

grep "status=500" logs/order.log > logs/loi_500.txt
```

### 2 dòng đầu tiên trong logs/loi_500.txt

```text

macbook@38 /Users % head -n 2 logs/loi_500.txt
head: logs/loi_500.txt: No such file or directory
```

### b) Lệnh đếm số dòng status=404 và kết quả

```shell

grep "status=404" logs/ordeer.log | wc -l
```

```text

grep: logs/ordeer.log: No such file or directory
       0
macbook@38 /Use
```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell

chmod +x tong_hop.txt
bash tong_hop.txt
```

### Nội dung file logs/tong_hop.txt
# script: tong_hop.txt
# Tac gia: Nguyễn Tiến Duy
# Ngay tao: 2026-11-11
echo "Dang tao bao cao.."
echo "=== BAO CAO SU CO WEBSITE ===" > logs/tong_hop.sh
cat logs/rental.log | grep "WARNING" >> log.s/tong_hop.sh
cat logs/rental.log | grep "ERROR" | wc -l >> logs/tong_hop.sh
echo "Hoan thanh!"
```text
(Dán nội dung file vào đây – xoá dòng này)

```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] README.md: Heading 1, mô tả có **in đậm** và *in nghiêng*, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | --- | --- | --- |
| 1 |  |  |  |
| 2 |  |  |  |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:** 
- **Expected:** 
- **Actual:** 
- **Log:** 

### Câu tìm kiếm Google

```text
(Ghi câu tìm kiếm vào đây – xoá dòng này)

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/don_in_thang_6.xlsx`, không cần ghi vào đây.
