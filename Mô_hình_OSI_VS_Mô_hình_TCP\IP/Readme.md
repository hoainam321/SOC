##  Tóm tắt mô hình OSI
Mục lục:

- [Mô hình OSI là gì ?](#mô-hình-osi-là-gì-)
- [Thuật ngữ  ?](#thuật-ngữ)
- [Các lớp mô hình OSI](#các-lớp-mô-hình-osi)
  - [Các lớp OSI](#các-lớp-osi)
  - [Bảng chi tiết](#bảng-chi-tiết)
  - [Chi tiết từng lớp](#chi-tiết-từng-lớp)
    - [L7 lớp ứng dụng](#l7-lớp-ứng-dụng-application)
    - [L6 lớp trình bày](#l6-lớp-trình-bầy-presentation)
    - [L5 lớp phiên](#l5-lớp-phiên-(session))
    - [L4 lớp vận chuyển](#l4-lớp-vận-chuyển-(transport))
    - [L3 lớp mạng](#l3-lớp-mạng-(network))
    - [L2 lớp liên kết dữ liệu](#l2-lớp-liên-kết-dữ-liệu-data-link)
    - [L1 lớp vật lý](#l1-lớp-vật-lý-physical)
  - [Cổng lớp vận chuyển](#cổng-lớp-vận-chuyển)
  - [Các cổng quan trọng trên lớp vận chuyển](#các-cổng-quan-trọng-trên-lớp-vận-chuyển)
  - [Các từ viết tắt](#what-is-the-osi-model)



### Mô hình OSI là gì ?

**Mô hình Kết nối Hệ thống Mở (OSI):** là một mô hình khái niệm do Tổ chức Tiêu chuẩn hóa Quốc tế tạo ra, cho phép các hệ thống truyền thông đa dạng giao tiếp bằng các giao thức chuẩn. Nói một cách dễ hiểu, OSI cung cấp một tiêu chuẩn cho các hệ thống máy tính khác nhau có thể giao tiếp với nhau.

Mô hình OSI có thể được coi là ngôn ngữ phổ quát cho mạng máy tính. Nó dựa trên khái niệm chia hệ thống truyền thông thành bảy lớp trừu tượng, mỗi lớp xếp chồng lên nhau.

Nói một cách đơn giản, mô hình này sẽ giúp bạn tìm ra mức độ của sự cố và rất hữu ích để khắc phục sự cố mạng. Cho dù đó là một người không thể kết nối máy tính xách tay của họ với Internet hay một trang web bị ngừng hoạt động đối với hàng nghìn người dùng, mô hình OSI có thể giúp giải quyết vấn đề và cô lập nguồn gốc của sự cố. Nếu vấn đề có thể được thu hẹp lại thành một lớp cụ thể của mô hình thì có thể tránh được rất nhiều công việc không cần thiết.

### Thuật ngữ

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

## Các lớp mô hình OSI

### Các lớp OSI

<div align="center">
<img src="media/osi-model-7-layers.svg">
<p><strong>Figure:</strong> the OSI layers and their usage.</p>
</div>


### Bảng chi tiết
| Layer | OSI model layer | Protocol Data Unit | Devices                                    | Protocols                                                    |
| ----- | --------------- | ------------------ | ------------------------------------------ | ------------------------------------------------------------ |
| 7     | Application     | Data               | L7 firewall                                | HTTP, DNS, DHCP, FTP, Telnet, SSH, SMTP, POP, IMAP, NTP, SNMMP, TLS/SSL, GBP, RIP, SIP, etc. |
| 6     | Presentation    | Data               | L7 firewall                                | All the above                                                |
| 5     | Session         | Data               | L7 firewall                                | All the above                                                |
| 4     | Transport       | Segments           | L4 firewall                                | TCP (connection oriented), UDP (connectionless oriented)     |
| 3     | Network         | Packets            | Router, Multiplayer Switch, Router         | IPv4, IPv6, IPSec, OSPF, EIGRP                               |
| 2     | Data Link       | Frames             | Switch, Bridge, NIC, Wireless Access Point | MAC, ARP Ethernet 802.3 (Wired), CDP, LLDP, HDLC, PPP, DSL, L2TP, IEEE 802.11 (Wireless), SONET/SDH |
| 1     | Physical        | Bits               | All the above                              | Electrical signal (copper wire), Light signal (optical fibre), Radio signal (air) |

### Chi tiết từng lớp
#### L7 Lớp ứng dụng (Application)

<div align="center">
<img src="media/7-application-layer.svg">
<p><strong>Figure:</strong> L7 the application layer</p>
</div>

Đây là lớp duy nhất tương tác trực tiếp với dữ liệu từ người dùng. Các ứng dụng phần mềm như trình duyệt web và ứng dụng email đều dựa vào lớp ứng dụng để bắt đầu liên lạc. Nhưng cần phải làm rõ rằng *các ứng dụng phần mềm máy khách không phải là một phần của lớp ứng dụng*; thay vào đó, lớp ứng dụng chịu trách nhiệm về các giao thức và thao tác dữ liệu mà phần mềm dựa vào để trình bày dữ liệu có ý nghĩa cho người dùng. Các giao thức lớp ứng dụng bao gồm HTTP , HTTPS, FTP, SFTP, DNS cũng như SMTP (Giao thức truyền thư đơn giản là một trong những giao thức cho phép liên lạc qua email), v.v.

#### L6 Lớp trình bầy (Presentation)

<div align="center">
<img src="media/6-presentation-layer.svg">
<p><strong>Figure:</strong> L6 the presentation layer.</p>
</div>

Lớp này chịu trách nhiệm chính trong việc chuẩn bị dữ liệu để lớp ứng dụng có thể sử dụng nó; nói cách khác, lớp 6 làm cho dữ liệu có thể hiển thị được để các ứng dụng sử dụng. Lớp trình bày chịu trách nhiệm dịch, mã hóa và nén dữ liệu.

Hai thiết bị giao tiếp đang giao tiếp có thể sử dụng các phương thức mã hóa khác nhau, do đó lớp 6 chịu trách nhiệm dịch dữ liệu đến thành cú pháp mà lớp ứng dụng của thiết bị nhận có thể hiểu được (UTF8 -> ASCII hoặc ASCII -> EBCDIC).

Nếu các thiết bị đang liên lạc qua kết nối được mã hóa, lớp 6 chịu trách nhiệm thêm mã hóa ở đầu người gửi cũng như giải mã mã hóa ở đầu người nhận để nó có thể hiển thị cho lớp ứng dụng dữ liệu có thể đọc được, không được mã hóa (thường thông qua SSL/ TL).

Cuối cùng, lớp trình bày còn chịu trách nhiệm nén dữ liệu mà nó nhận được từ lớp ứng dụng trước khi chuyển sang lớp 5. Điều này giúp cải thiện tốc độ và hiệu quả truyền thông bằng cách giảm thiểu lượng dữ liệu sẽ được truyền đi, hơn nữa, việc nén dữ liệu có thể bị ảnh hưởng. có hai loại: mất dữ liệu (không đảm bảo tính toàn vẹn dữ liệu) hoặc không mất dữ liệu (đảm bảo tính toàn vẹn dữ liệu).

#### L5 Lớp phiên (Session)

<div align="center">
<img src="media/5-session-layer.svg">
<p><strong>Figure:</strong> L5 the session layer.</p>
</div>

Đây là lớp chịu trách nhiệm mở và đóng giao tiếp giữa hai thiết bị. Khoảng thời gian giữa lúc mở và đóng giao tiếp được gọi là phiên. Lớp phiên đảm bảo rằng phiên vẫn mở đủ lâu để truyền tất cả dữ liệu được trao đổi và sau đó đóng phiên ngay lập tức để tránh lãng phí tài nguyên.

Lớp phiên cũng đồng bộ hóa việc truyền dữ liệu với các điểm kiểm tra. Ví dụ: nếu một tệp 100 megabyte đang được truyền, lớp phiên có thể đặt điểm kiểm tra cứ sau 5 megabyte. Trong trường hợp mất kết nối hoặc gặp sự cố sau khi truyền 52 megabyte, phiên có thể được tiếp tục từ điểm kiểm tra cuối cùng, nghĩa là chỉ cần truyền thêm 50 megabyte dữ liệu. Nếu không có các trạm kiểm soát, toàn bộ quá trình chuyển giao sẽ phải bắt đầu lại từ đầu.

Thông thường, nhiệm vụ chính của L5 là xác thực và ủy quyền, tải xuống các tệp dưới dạng gói dữ liệu, quản lý phiên.

#### L4 Lớp vận chuyển (Transport)

<div align="center">
<img src="media/4-transport-layer.svg">
<p><strong>Figure:</strong> L4 the transport layer.</p>
</div>

Lớp này được phân tách bằng hai giao thức như Giao thức điều khiển vận chuyển và Giao thức gói dữ liệu người dùng. TCP đang theo truyền dẫn hướng kết nối. Nó chậm hơn nhưng cung cấp phản hồi (HTTP, FTP, v.v.). UDP đang theo truyền dẫn không kết nối. Nó nhanh hơn nhưng không cung cấp phản hồi và được sử dụng khi chúng ta không quan tâm đến tính đầy đủ của dữ liệu (trò chơi điện tử, âm nhạc, phim, v.v.).

Lớp 4 chịu trách nhiệm liên lạc từ đầu đến cuối giữa hai thiết bị. Điều này bao gồm lấy dữ liệu từ lớp phiên và chia nó thành các phần được gọi là phân đoạn (hoặc datagram trong trường hợp UDP) trước khi gửi đến lớp 3. Lớp vận chuyển trên thiết bị nhận chịu trách nhiệm tập hợp lại các phân đoạn thành dữ liệu mà lớp phiên có thể tiêu thụ.

Lớp vận chuyển cũng chịu trách nhiệm kiểm soát luồng và kiểm soát lỗi. Kiểm soát luồng xác định tốc độ truyền tối ưu để đảm bảo rằng người gửi có kết nối nhanh không làm quá tải người nhận có kết nối chậm. Lớp vận chuyển thực hiện kiểm soát lỗi ở đầu nhận bằng cách đảm bảo rằng dữ liệu nhận được là hoàn chỉnh và kiểm tra tổng kiểm tra các đơn vị dữ liệu và sử dụng yêu cầu lặp lại tự động nếu không.

#### L3 Lớp mạng (Network)

<div align="center">
<img src="media/3-network-layer.svg">
<p><strong>Figure:</strong> L3 the network layer.</p>
</div>

Lớp mạng chịu trách nhiệm tạo điều kiện thuận lợi cho việc truyền dữ liệu giữa hai mạng khác nhau. Nếu hai thiết bị giao tiếp nằm trên cùng một mạng thì lớp mạng là không cần thiết. Lớp mạng chia các phân đoạn từ lớp vận chuyển thành các đơn vị nhỏ hơn, được gọi là các gói, trên thiết bị của người gửi và tập hợp lại các gói này trên thiết bị nhận. Lớp mạng cũng tìm đường dẫn vật lý tốt nhất để dữ liệu đến đích; điều này được gọi là định tuyến.

Nhiệm vụ chính của lớp này thường là đánh địa chỉ logic (IPv4, IPv6, mặt nạ, IP), định tuyến (gửi gói tin đến ai), xác định đường dẫn (Mở đường dẫn ngắn nhất trước, Giao thức cổng biên, hệ thống trung gian-hệ thống trung gian).

####  L2 Lớp liên kết dữ liệu (Data link)

<div align="center">
<img src="media/2-data-link-layer.svg">
<p><strong>Figure:</strong> L2 the data link layer.</p>
</div>

Lớp liên kết dữ liệu rất giống với lớp mạng, ngoại trừ lớp liên kết dữ liệu tạo điều kiện truyền dữ liệu giữa hai thiết bị trên CÙNG một mạng. Lớp liên kết dữ liệu lấy các gói từ lớp mạng và chia chúng thành các phần nhỏ hơn gọi là khung. Giống như lớp mạng, lớp liên kết dữ liệu cũng chịu trách nhiệm kiểm soát luồng và kiểm soát lỗi trong giao tiếp nội mạng (Lớp vận chuyển chỉ thực hiện kiểm soát luồng và kiểm soát lỗi đối với giao tiếp giữa các mạng).

Nhiệm vụ thường là địa chỉ logic (lớp mạng), địa chỉ vật lý (lớp liên kết dữ liệu thông qua địa chỉ MAC của Thẻ giao diện mạng, Bộ chuyển mạch), truy cập phương tiện, kiểm soát cách đặt và nhận dữ liệu từ phương tiện (kiểm soát truy cập phương tiện, phát hiện lỗi).

#### L1 Lớp vật lý (physical)

<div align="center">
<img src="media/1-physical-layer.svg">
<p><strong>Figure:</strong> L1 the physical layer.</p>
</div>

Lớp này bao gồm các thiết bị vật lý liên quan đến việc truyền dữ liệu, chẳng hạn như cáp và bộ chuyển mạch. Đây cũng là lớp nơi dữ liệu được chuyển đổi thành luồng bit, là chuỗi 1 và 0. Lớp vật lý của cả hai thiết bị cũng phải thống nhất về quy ước tín hiệu để có thể phân biệt được số 1 với số 0 trên cả hai thiết bị.

#### Cổng lớp vận chuyển

| Category         | Range       | Comments                                                     |
| ---------------- | ----------- | ------------------------------------------------------------ |
| Các cổng nổi tiếng | 0 - 1023    | Được sử dụng bởi các quy trình hệ thống, ví dụ SSH(22), DNS(53), FTP(21), v.v.. |
| Cổng đã đăng ký | 1024-49151  | Đối với các dịch vụ cụ thể, ví dụ PostgreSQL(5432), Redis(6379), v.v.. |
| Cổng riêng    | 49152-65535 | Cho mục đích riêng tư, ví dụ như để chạy một ứng dụng.              |

#### Các cổng quan trọng trên lớp vận chuyển

| Port Number | Protocol | Application                     |
| ----------- | -------- | ------------------------------- |
| 20          | TCP      | FTP data                        |
| 21          | TCP      | FTP control                     |
| 22          | TCP      | SSH                             |
| 23          | TCP      | Telnet                          |
| 25          | TCP      | SMTP                            |
| 53          | UDP, TCP | DNS                             |
| 67, 68      | UDP      | DHCP                            |
| 69          | UDP      | TFTP                            |
| 80          | TCP      | HTTP                            |
| 110         | TCP      | POP3                            |
| 161         | UDP      | SNMP                            |
| 443         | TCP      | SSL                             |
| 16384-32767 | UDP      | TRP-base Voice (VoIP) and Video |

