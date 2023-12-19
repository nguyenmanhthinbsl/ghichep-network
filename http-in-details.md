# HTTP IN DETAILS

## 1. What is HTTP/HTTPS? 
- HyperText Transfer Protocol: giao thức truyền tải siêu văn bản. Đây là một giao thức ứng dụng được sử dụng thường xuyên nhất trong bộ các giao thức TCP/IP (gồm một nhóm các giao thức nền tảng cho internet). 

- Http hoạt động dựa trên mô hình Client (máy khách) – Server (máy chủ) trao đổi thông tin webpage data, có thể là HTML, Images, Videos, etc.

-HTTPS? (HyperText Transfer Protocol Secure): Giao thức truyền tải siêu văn bản bảo mật. Là giao thức mà qua đó dữ liệu được gửi giữa trình duyệt và trang web bạn đang kết nối sử dụng để bảo vệ các giao dịch trực tuyến có tính bảo mật cao như giao dịch ngân hàng và đặt hàng mua sắm trực tuyến.

### 1.1 Sử khác nhau giữa HTTP vs HTTPS:
![Alt text](/resources/diffbtwHTTPvsHTTPS.png)


## 2. Request và Response

- Để truy cập web, trình duyệt cần yêu cầu request đến máy chủ web(web server) để yêu cầu tài nguyên(HTML, ảnh, file,...). Thì cần có URL để định danh resources đó ở đâu?

###  2.1 URL - Uniform Resource Locator - Hệ thống  định vị tài nguyên thống nhất.
![Alt text](/resources/urlsample.png)

Trong đó:
- Scheme: định nghĩa phương thức truyền tải nào được sử dụng để truy cập đến tài nguyên này ví dụ như HTTP, HTTPS, FTP...
- User: một số tài nguyên sẽ cần được xác thực người dùng trước để có thể có quyền hạn truy cập vào tài nguyên đó.
- Host: là tên domain hoặc địa chỉ IP mà server bạn muốn truy cập đến.
- Port: là cổng mà server sử dụng để chia sẻ tài nguyên. Với HTTP  là  80, HTTPS thường là 443. Tuy nhiên có thể cấu hình port tuỳ chỉnh từ 1 - 65535.
- Path: Đường dẫn dẫn đến tài nguyên đó trên server mà bạn đang muốn truy cập đến.
- Query String: Thường được thêm vào các thông tin định nghĩa để trích xuất thông tin tài nguyên 1 cách chính xác hơn. Được viết trên chính Request Path.
- Fragment: Đây là tham chiếu đến một vị trí trên trang thực tế được yêu cầu. Thường được sử dụng cho các trang có nội dung dài và có thể có một phần nhất định của trang được liên kết trực tiếp với nó, do đó người dùng có thể xem được ngay khi họ truy cập trang.


## 3. HTTP methods - phương thức HTTP
- Là cách mà client thực hiện mục đích mong muốn với yêu cầu  HTTP mà học  thực hiện:
Bao gồm:
+ HEAD: yêu cầu một GET request nhưng không có Body.
+ GET: yêu cầu trình bày tài nguyên nhất định. Chỉ sử dụng để đọc data.
+ POST: Yêu cầu tài nguyên được chỉnh sửa bởi chính mình. Có thể ghi tài nguyên.
+ PUT: Là phương thức để chỉnh sửa resource khi Client gửi data và muốn update toàn bộ resource đó.
+ DELETE: Là  phương thức để xoá data mong muốn.
+ CONNECT: Xác định một tunel đến máy  chủ  được xác định bởi tài nguyên đích.
+ OPTIONS: Mô tả  các phương thức giao tiếp khác nhau đến tài nguyên đích.
+ TRACE: trình bày thôgn báo loop-back thử nghiệm kết nối đến tài nguyên đích. 
+ PATCH:  sửa đổi một phần cho tài nguyên đích.


## 4. HTTP Status Codes - Mã thông báo trạng thái HTTP
Khi Client gửi HTTP Request đến server sẽ nhận được các output để xác định tín hiệu trả về sẽ như thế nào, được phân chia thành 5 nhánh chính:
- 100 -> 199 Information response: Thông báo thông tin - Cho client biết rằng phần đầu tiên của Request được chấp nhận và server mong muốn client sẽ tiếp tục gửi các phần còn lại của request đến. Các mã này thường không được sử dụng phổ biến.
- 200 -> 299: Success - thông báo thành công: Các code trong khoảng này thường sẽ thông báo cho client biết là request đã được đáp ứng thành công.
- 300 -> 399: Redirection- thông báo chuyển tiếp: Thường sử dụng để chuyển tiếp yêu cầu tài nguyên của client sang một resources khác. Có thể resources URL khác trong 1 server, hoặc có thể resources thuộc server khác.
- 400 -> 499 Client error: Thông báo lỗi phía Client: thường chỉ ra các lỗi có trong Request được gửi từ client.
- 500 -> 599: Server Error: Chỉ xảy ra ở phía Server.

### 4.1 Bảng các HTTP Status code thường gặp:

|STT|Status Code|Ý nghĩa|
|---|-----------|-------|
| 1 |200-OK     |Thành công|
| 2 |201-created|Tạo mới thành công|
| 3 |301-moved permanently|Chuyển tiếp  thành công|
| 4 |302-found  |Tương tự 301 nhưng chỉ mang tính tạm thời|
| 5 |400-bad    |Thiếu gì  đó trong request. Đợi client  gửi tham số cần thiết.|
| 6 |401-not authorised| Không được xem tài nguyên khi chưa xác thực|
| 7 |403-forbidden| Không có quyền hạn xem tài nguyên này|
| 8 |405-method not allowed| Method này không được phép|
| 9 |404-page not found| Tài nguyên này không tồn tại|
|10 |500-Internal service|Server xảy ra lỗi khiến cho hành động không response không thực  hiện được|
|11 |503-service unavailable|Server  không thể handle request client gửi đến do quá tải|


##  5.Header
header - Tiêu đề:  là các bit dữ liệu bổ sung mà bạn có thể gửi đến máy chủ web khi thực hiện yêu cầu Request.
### 5.1 Common request headers:
header được gửi từ trình duyệt của Client đến Server khi Request được gửi đi.

Các khái niệm:
- Host: Một số máy chủ cung cấp 1 loạt nhiều các dịch vụ web khác nhau. Vì  vậy cần có Header để phân biệt được yêu cầu đến tài nguyên dịch vụ web nào. Nếu không có  sẽ chỉ yêu cầu đến trang mặc định.
- User-agent: Là thông tin trình duyệt Client sử dụng và phiên bản kèm theo của nó để gửi Request.
- Content-length: Xác định độ lớn của thông tin được gửi đến web server. Qua đó đảm bảo tính toàn vẹn dữ liệu.
- Accept-encoding: Nén thông tin để rút gọn quá trình truyền tin qua internet.
-  Cookie: Các thông tin của Client mà server lưu trữ để xác định bạn.

### 5.2 Common Response Header:

Các response header thông thường được trả lại khi Client gửi request là:
- Set-cookie: Thông tin được lưu trữ để xác định người dùng mỗi request.
- Cache-control: thời gian mà thông tin response được lưu trữ trong bộ nhớ tạm trước khi nó hết hiệu lực.
- Content-type: Báo cho Client rằng loại data nào sẽ được trả về cho họ. Để trình duyệt có cách xử lý thông tin phù hợp.
- Content-encoding: Nén thông tin để rút gọn quá trình truyền tin qua internet.
## 6. Cookies
Là thông tin được lưu trữ trên trình duyệt để xác định bạn là ai khi truy cập vào một webserver. 

![Alt text](/resources/cookies.png)

Cookie thường được sử dụng với vai trò xác thực trong website( website authentication)

### Xác định cookie trên trang web bạn đang truy cập:
View site -> network tab -> cookies.
