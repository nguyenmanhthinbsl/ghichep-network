# ghichep-network

## Mạng truyền thông và công nghệ mạng

### Giới thiệu chung
Truyền thông mạng máy tính ( computer communications ) là quá trình truyền dữ liệu từ thiết bị này sang thiết bị khác, trước đây chúng ta thường hiểu thiết bị là máy tính, nhưng ngày nay thiết bị ( end-system, decive ) không chỉ đơn thuần là máy tính mà bao gồm nhiều chủng loại thiết bị khác.

Networking: chỉ khái niệm kết nối các thiết bị lại với nhau nhằm mục đích chia sẻ thông tin, liên quan đến nhiều vấn đề gồm:
- giao thức truyền thông ( protocol ): mô tả những nguyên tắc mà tất cả các thành phần mạng cần tuân thủ để có thể trao đổi với nhau được
- Topo ( mô hình ghép nối mạng/hình trạng mạng ): mô tả cách thức nối các thiết bị với nhau.
- Địa Chỉ: mô tả các thức định vị 1 đối tượng trên mạng.
- Định tuyến ( routing ): mô tả cách thức dữ liệu truyền từ thiết bị này sang thiết bị khác trên mạng.
- Tính tin cậy ( reliability ): giải quyết tính toàn vẹn của dữ liệu, đảm bảo dữ liệu nhận được chính xác như dữ liệu gửi đi.
- Khả năng liên tác ( interoperability): chỉ mức đọ các sản phẩm phần mềm và phần cứng của các hãng sản xuất khác nhau có thể làm việc được với nhau.
- An ninh (security): đảm bảo an toàn hoặc bảo vệ tất cả các thành phần của mạng.
- Chuẩn (Standard): Thiết lập các quy tắc và luật lệ cụ thể cần phải tuân theo

Mạng truyền thông ra đời sớm nhất và phổ biến nhất là mạng điện thoại( plain old telephone system - POTS, public switched telephone network - PSTN ).

### Mạng máy tính:
Mạng máy tính là tập hớp các máy tính và các thiệt bị phụ trợ khác sử dụng chung 1 nhóm giao thức để chia sẻ tài nguyên thông qua các phương tiện truyền thông mạng:
- Các thiết bị đầu cuối (end system) kết nối với nhau tạo thành mạng có thể là các máy tính (computer) hoặc các thiết bị khác. Ngày càng có nhiều loại thiết bị có khả năng kết nối vào mạng máy tính như điện thoại đi động,( PDA- Thiết bị hỗ trợ kỹ thuật số), Tivi,...
- Môi trường truyền (media) thực hiện việc truyền dẫn các tín hiệu vật lý. Môi trường truyền có thể là các loại dây dẫn ( cáp), sóng (đối với các mạng không dây)
- Giao thức (protolcol) là quy tắc quy định cách thức trao đổi dữ liệu giữa các thực thể.

## Các kiểu mô hình mạng:
### phân loại trên phạm vi:
```
Mạng cục bộ (Local Area Network - LAN);
Mạng diện rộng (Wide Area Network - WAN);
Mạng đô thị (Metropilitan Area Network - MAN);
Mạng cá nhân (Personal Area Network - PAN);
Mạng toàn cầu (Global Area Network - GAN);
Mạng Lưu trữ (Storage Area Network - SAN);
```

###Các kiểu kết nối mạng trong LAN
- Dạng tuyến (BUS Topology): dùng dây cáp ít nhất, dễ lắp đặt nên tiết kiệm được chi phí lắp đặt. Nhưng sẽ có sự ùn tắc khi di chuyển dữ liệu với lưu lượng lớn. Khi có sự hỏng hóc ở đoạn nào đó thì rất khó phát hiện, một sự ngừng trên đường dây để sửa chữa sẽ ngừng toàn bộ hệ thống.

- Dạng Hình Sao(Star topology): Tốc độ cao, dễ bảo trì sửa chữa, dễ mở rộng. Nhưng kả năng mở rộng mạng đều phụ thuộc vào khả năng của trung tâm. Khi trung tâm gặp sự cố thì toàn mạng đều ngưng hoạt động. Mạng yêu cầu nối độc lập riêng rẽ từng thiết bị ở các nút thông tin đến trung tâm. Khoảng cách từ máy đến trung tâm rất hạn chế (100 m).
- Dạng Vòng( Ring topology): có thể nới rộng ra xa, tiết kiệm được dây cable, tốc độ nhanh hơn kiểu BUS. Nhưng tốc độ không nhanh bằng dạng Star, ngưng toàn bộ hệ thống khi lỗi/bảo trì,khó phát hiện lỗi.

## [Mô hình OSI](#https://github.com/nguyenmanhthinbsl/ghichep-network/blob/master/OSI-model.md)
Mô hình OSI là một trong những công cụ quan trọng nhất để giúp ta nắm bắt cách làm việc của các thiết bị mạng như router, switch, PC ... OSI viêt tắt của từ Open System Interconnection


## Mô Hình TCP/IP !

TCP/IP là bộ giao thức cho phép kết nối các hệ thống mạng không đồng nhất với nhau. Ngày nay TCP/IP được sử dụng rộng rãi trong mạng cục bộ cũng như mạng toàn cầu. TCP/IP được xem như giản lược của mô hình tham chiếu OSI với 4 tầng.
