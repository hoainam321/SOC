##  Tóm tắt mô hình OSI
Mục lục:

- [Mô hình OSI là gì ?](#Model-OSI-là-gì-?)
- [Thuật ngữ  ?](#what-is-the-osi-model)
- [Các lớp mô hình OSI](#what-is-the-osi-model)
  - [Các lớp OSI](#what-is-the-osi-model)
  - [Bảng chi tiết](#what-is-the-osi-model)
  - [Chi tiết từng lớp](#what-is-the-osi-model)
    - [L7 lớp ứng dụng](#what-is-the-osi-model)
    - [L6 lớp trình bày](#what-is-the-osi-model)
    - [L5 lớp phiên](#what-is-the-osi-model)
    - [L4 lớp vận chuyển](#what-is-the-osi-model)
    - [L3 lớp mạng](#what-is-the-osi-model)
    - [L2 lớp liên kết dữ liệu](#what-is-the-osi-model)
    - [L1 lớp vật lý](#what-is-the-osi-model)
  - [Cổng lớp vận chuyển](#what-is-the-osi-model)
  - [Các cổng quan trọng trên lớp vận chuyển](#what-is-the-osi-model)
  - [Các từ viết tắt](#what-is-the-osi-model)



### Mô hình OSI là gì ?

**Mô hình Kết nối Hệ thống Mở (OSI):** là một mô hình khái niệm do Tổ chức Tiêu chuẩn hóa Quốc tế tạo ra, cho phép các hệ thống truyền thông đa dạng giao tiếp bằng các giao thức chuẩn. Nói một cách dễ hiểu, OSI cung cấp một tiêu chuẩn cho các hệ thống máy tính khác nhau có thể giao tiếp với nhau.

Mô hình OSI có thể được coi là ngôn ngữ phổ quát cho mạng máy tính. Nó dựa trên khái niệm chia hệ thống truyền thông thành bảy lớp trừu tượng, mỗi lớp xếp chồng lên nhau.

Nói một cách đơn giản, mô hình này sẽ giúp bạn tìm ra mức độ của sự cố và rất hữu ích để khắc phục sự cố mạng. Cho dù đó là một người không thể kết nối máy tính xách tay của họ với Internet hay một trang web bị ngừng hoạt động đối với hàng nghìn người dùng, mô hình OSI có thể giúp giải quyết vấn đề và cô lập nguồn gốc của sự cố. Nếu vấn đề có thể được thu hẹp lại thành một lớp cụ thể của mô hình thì có thể tránh được rất nhiều công việc không cần thiết.

### Thuật ngữ chính

**Encapsulation:** đang chuẩn bị và chuyển dữ liệu từ bất kỳ lớp trên nào xuống lớp Dưới. Về cơ bản, điều đó có nghĩa là đi từ lớp ứng dụng xuống lớp vật lý.

**Decapsulation:**  là đóng gói ngược lại. Dữ liệu giải mã này đồng thời đi lên từ lớp vật lý cho đến lớp ứng dụng.

**L7-L5** được gọi là Lớp trên hoặc Lớp chủ. Chúng thường làm việc với một ứng dụng chứ không phải với chính phần cứng.

**L4-L1** được gọi là Lớp dưới hoặc Lớp Phương tiện. Họ thường làm việc với phần cứng.

**[Bits]** - L1

**[Tiêu đề khung]** - L2

**[Tiêu đề mạng]** - L3

**[Tiêu đề truyền tải]** - L4

**[Dữ liệu]** - L7 - L5

Điều ngược lại xảy ra khi đơn vị dữ liệu đi từ L1 đến L7 . Tiêu đề dải lớp.

Để thông tin con người có thể đọc được được truyền qua mạng từ thiết bị này sang thiết bị khác, dữ liệu phải di chuyển xuống bảy lớp của mô hình OSI trên thiết bị gửi và sau đó di chuyển lên bảy lớp ở đầu nhận.

## Các  lớp mô hình OSI

### Các lớp  OSI

<div align="center">
<img src="media/osi-model-7-layers.svg">
<p><strong>Figure:</strong> the OSI layers and their usage.</p>
</div>


| Layer | OSI model layer | Protocol Data Unit | Devices                                    | Protocols                                                    |
| ----- | --------------- | ------------------ | ------------------------------------------ | ------------------------------------------------------------ |
| 7     | Application     | Data               | L7 firewall                                | HTTP, DNS, DHCP, FTP, Telnet, SSH, SMTP, POP, IMAP, NTP, SNMMP, TLS/SSL, GBP, RIP, SIP, etc. |
| 6     | Presentation    | Data               | L7 firewall                                | All the above                                                |
| 5     | Session         | Data               | L7 firewall                                | All the above                                                |
| 4     | Transport       | Segments           | L4 firewall                                | TCP (connection oriented), UDP (connectionless oriented)     |
| 3     | Network         | Packets            | Router, Multiplayer Switch, Router         | IPv4, IPv6, IPSec, OSPF, EIGRP                               |
| 2     | Data Link       | Frames             | Switch, Bridge, NIC, Wireless Access Point | MAC, ARP Ethernet 802.3 (Wired), CDP, LLDP, HDLC, PPP, DSL, L2TP, IEEE 802.11 (Wireless), SONET/SDH |
| 1     | Physical        | Bits               | All the above                              | Electrical signal (copper wire), Light signal (optical fibre), Radio signal (air) |



