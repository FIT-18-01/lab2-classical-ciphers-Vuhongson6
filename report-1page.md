# Report 1 Page – FIT4012 Lab 2

## 1. Mục tiêu
Bài lab nhằm giúp sinh viên hiểu và cài đặt hai thuật toán mã hóa cổ điển là Caesar Cipher và Rail Fence Cipher, bao gồm cả mã hóa và giải mã. Ngoài ra, bài lab cũng giúp rèn luyện kỹ năng xử lý chuỗi, kiểm tra dữ liệu đầu vào và đọc dữ liệu từ file.

## 2. Cách làm
- Hoàn thiện Caesar Cipher:
    Hỗ trợ chữ thường, chữ hoa và giữ nguyên dấu cách.
    Cài đặt cả mã hóa (encryption) và giải mã (decryption).
- Hoàn thiện Rail Fence Cipher:
    Cài đặt giải mã.
    Giữ nguyên dấu cách trong chuỗi.
    Kiểm tra đầu vào hợp lệ (số rails > 1, chuỗi không rỗng).
    Đọc dữ liệu từ file data/input.txt.
- Chạy thử chương trình với nhiều test case khác nhau để kiểm tra tính đúng đắn.

## 3. Kết quả chính
### 3.1 Caesar Cipher
| Input | Key | Ciphertext / Plaintext | Nhận xét |
|---|---:|---|---|
| I LOVE YOU | 3 | L ORYH BRX  |Mã hóa đúng, giữ khoảng trắng|
| hello world| 5 | mjqqt btwqi |Hoạt động với chữ thường     |
| LORYH BRX  | 3 | I LOVE YOU  |Giải mã chính xác  |

### 3.2 Rail Fence Cipher
| Input | Rails | Ciphertext / Plaintext | Nhận xét |
|---|---:|---|---|
| I LOVE YOU | 2 |ILV OEOU Y  |Giữ khoảng trắng  |
| I LOVE YOU | 4 |IOYV E LOU  |Hoạt động đúng với nhiều rails  |
| IOEOLVYU   | 2 |ILOVEYOU    |Giải mã chính xác  |

### 3.3 Input validation / file input
- Trường hợp đầu vào không hợp lệ:
    Key không phải số nguyên hoặc < 0 (Caesar).
    Rails ≤ 1 (Rail Fence).
    Chuỗi rỗng.
    → Chương trình thông báo lỗi và yêu cầu nhập lại.
- Kết quả đọc từ data/input.txt:
    Đọc thành công dữ liệu từ file.
    Áp dụng đúng thuật toán và in ra kết quả tương ứng.

## 4. Kết luận
Sau khi hoàn thành bài lab, em đã hiểu rõ hơn nguyên lý của các thuật toán mã hóa cổ điển, tiêu biểu là Caesar Cipher (dựa trên dịch chuyển ký tự) và Rail Fence Cipher (dựa trên hoán vị vị trí). Phần khó nhất đối với em là quá trình giải mã Rail Fence, vì cần khôi phục chính xác dạng zig-zag ban đầu của chuỗi. Thông qua việc thử nghiệm với nhiều test case khác nhau, em dần nắm chắc cách hoạt động của thuật toán và cải thiện độ chính xác của chương trình.
