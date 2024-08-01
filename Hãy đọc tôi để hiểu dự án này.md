# Mục tiêu chính: Thực hiện các chức năng trên app để tương tác với các matrix LED

Vậy app có những chức năng gì, matrix LED là gì, trông như nào?

App có những chức năng:
1. Dịch phải các kí tự
2. Dịch trái các kí tự
3. Nhấp nháy các kí tự
4. Làm toán cơ bản (+-*/)
5. ...
   
Matrix LED là gì?

Matrix LED là tập hợp các đèn LED xếp theo chiều dài và chiều rộng tạo thành ma trận LED, với các chân LED cùng cực được nối tiếp nhau.

Matrix LED trông như nào ?

![image](https://github.com/user-attachments/assets/56b343c2-52f5-443e-a387-0e7a3e53f258)

và đây là "Sơ đồ matrix LED"

![image](https://github.com/user-attachments/assets/6e1c9d3f-e585-49b6-88ac-2184b34eae9c)

Ờm thì, vậy bằng cách nào để các chức năng của app mà điều khiển được các matrix LED 1 cách thần kỳ vậy :D ?

Để từ app chạy ra matrix LED thì cần quãng đường sau:

```mermaid
sequenceDiagram
    participant app
    participant EmberSystem(ardunio & ic & ete..)
		participant matrix LED
    app-->>EmberSystem(ardunio & ic & ete..): Connection
    EmberSystem(ardunio & ic & ete..)-->>matrix LED: Control
```
Vậy chúng hoạt động với nhau như thế nào?

chúng ta sẽ lựa chọn chức năng trong app, thêm tham số(nếu có), rồi bấm chạy. App sẽ truyền chức năng cần thực hiện thông qua kết nối không dây tới EmberSystem(ardunio & ic & ete..). EmberSystem(ardunio & ic & ete..) nhận được sẽ gọi hàm tương ứng với chức năng người dùng yêu cầu, thể hiện kết quả thông qua matrix LED





