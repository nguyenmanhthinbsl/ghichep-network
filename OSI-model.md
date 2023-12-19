# Mô hình OSI - Open Systems Interconnection
![Alt text](/resources/osi.png)
![Alt text](/resources/osi2.png)

`Gồm 7 tầng`
## 1. Physical - vật lý - gói tin dạng bit
> chuyển đổi tín hiệu mã bit 0 1 sang dạng sóng để truyền trên dây mạng theo 1 đường truyền cụ thể nào đó(cab xoắn, cab đồng, cab quang, wireless)
Bao gồm các thành phần như: Coax, Fiber, Wireless, Hubs, Repeaters:

### 1.1 Coax
### 1.2 Fiber
### 1.3 Wireless
### 1.4 Hubs
### 1.5 Repeaters

## 2. Datalinks - liên kết dữ liệu  - gói tin dạng frames
> Sau khi có đường truyền vật lý ở lớp `physical`, thì làm cách nào để các lớp ở bên trên có thể truy cập vào đường truyền vật lý và chia sẻ đường truyền vật lý trên mạng thì đó là lớp `Data Link`.

> Thực hiện chức năng điều khiển truy nhập vào đường truyền `vật lý` và giao tiếp với lớp `network`. `Datalink` định dạng các thông điệp vào một khung dữ liệu (Frame) và thêm vào đó một header chứa các địa chỉ phần cứng nơi nhận và địa chỉ nguồn. Tiêu đề này chịu trách nhiệm cho việc tìm kiếm các thiết bị đích tiếp theo trên một mạng nội bộ.

> Lớp `Network` là chịu trách nhiệm cho việc tìm kiếm con đường đến đích cuối cùng nhưng không quan tâm về việc ai sẽ là người nhận tiếp theo. `Vì vậy lớp datalink  giúp cho dữ liệu truyền được điểm đến tiếp theo.`

Gồm 2 lớp con: LLC và MAC
### 2.1 Logical links control điều khiển logic liên kết (LLC)

- các giao thức: ethernet, wifi, cdp,...

Chức năng: 
- Quản lý các khung(frame) cho các lớp trên và dưới.
- Kiểm soát lỗi
- Điều khiển lưu  lượng
### 2.2 Media Access Control – Kiểm soát truy cập phương tiện (MAC)


## 3. Network - mạng  - gói tin dạng packet
> Nhiệm vụ định tuyến đường đi cho các gói tin trên mạng.
- router
- Các giao thức: IP, ICMP

## 4. Transport - Vận chuyển - gói tin dạng segment 
> Nhiệm vụ giao tiếp đầu cuối H2H host-to-host. Điều khiển quá trình truyền gói, phân luồng dữ liệu và giảm tắc nghẽn.
- Firewall, gateway.
- Giao thức: TCP, UDP
> Port: xác định dịch vụ mà gói tin sẽ được chuyển đến.

### TCP vs UDP communication diff:
![Alt text](/resources/tcp-udp.png)
## 5. Session - Phiên giao dịch.
> Nhiệm vụ thiết lập, duy trì kết nối,  đồng bộ hoá, chấm dứt kết nối phiên ứng dụng của người dùng cuối.
- Các giao thức: SMB - Server Message Block, SOCKS, netBIOS,Remote Procedure Call - RPC.
## 6. Presentation -trình diễn 
> Nhiệm vụ chuẩn bị dữ liệu phù hợp nhất khi truyền lên tầng 7. 
- Các giao thức: SSL/TLS, JPEG, GIF,...
## 7. Application - Ứng dụng
> Cung cấp giao diện, dịch vụ cho ứng dụng, tương tác trực tiếp với người dùng.
- Các giao thức: DHCP, HTTP, POP3, FTP, SMTP,...

|Protocol|Port Number(s)|Description|
|--------|--------------|-----------|
|Domain Name System (DNS)|	53|	Translates internet names to their globally registered IP addresses. For example, “google.com” is registered in global DNS as IP address 8.8.8.8.|
|Hypertext Transfer Protocol Secure (HTTPS)|443|Sends data to and from web browsers and web servers, but securely with the Secure Socket Layer (SSL) protocol.|
|File Transfer Protocol FTP|20,21|Transfers files from a client to a server and vice versa.|
|Secure Shell (SSH)|22|	Connects to computers remotely and in a secure, encrypted way.|
|Simple Mail Transfer Protocol (SMTP)|	25|	Sends and receives email.|
|Dynamic Host Configuration Protocol (DHCP)	|67|	Automatically assigns IP addresses to devices on a network.|
|Internet Relay Chat (IRC)	|194|	Used in a client/server method. IRC clients communicate through an IRC server.|
|Post Office Protocol 3  (POP3)	|110| (unsecured), 995 (secured)	Used for email where the client receives mail by downloading it locally to a computer from a server mailbox.|
