# MÔ HÌNH OSI

## 1. Hiểu về giao thức Host-to-Host:
   - Host là một thức thể mạng có khả năng truyền được các ứng dụng.(theo định nghĩa Quốc Tế) VD: WWW,... 
   - PC là thiết bị mạng có thể thực hiện được các ứng dụng .
   - Để truyền thông từ một Host-to-Host thì phãi xác định các mô hình truyền thông. Có nhiều loại mô hình: Older Model, Standards-based Model (mô hình chuẩn hóa).
 * So sánh Older Model và Standards-based Model:
 
 Older Model: Độc quyền. Tất cả các ứng dụng và phần mềm đều được cung cấp bởi 1 nhà cung cấp.
 
 Standards-based Model: Sử dụng nhiều sản phẩm của nhiều nhà sản xuất phần mềm. Xây dựng bằng phương pháp phân lớp.
 
## 2. Tại sao phải xây dựng mô hình mạng phân lớp:

 - Gỉam thiểu được độ phức tạp của hệ thống truyền dữ liệu.
 - Chuẩn hóa về các giao diện của các dòng sản phẩm.
 - Đảm bảo tính thương thích về mặt công nghệ.
 - Thúc đẩy kĩ thuật modun hóa.
 
 => Thúc đẩy sự phát triển của ngành công nghệ mạng.
 - Đơn giản cho việc dạy và học.
 
## 3. MÔ HÌNH OSI:

  <img src="http://vietjack.com/ipv4/images/osi_layers.jpg">
  
   a. Lớp Physical: có chức năng là truyền một dòng **bit** qua một đường truyền cụ thể nào đó.
   
   b. Lớp Data Link: điều khiển việc truy nhập vào đường truyền vật lí và thực hiện với lớp bên trên của nó (network).
   
   c. Lớp Network: chịu trách nhiệm cho việc phân bố dữ liệu từ điểm này đến điểm khác một cách tối ưu nhất bằng các thực hiện định tuyến các gói dữ liệu, chọn ra một đường đi tối ưu nhất để phân phối dữ liệu.
   
   d. Lớp Transport: quản lí các kết nối đầu cuối-đầu cuối (end-end)
   
   e. Lớp Session: truyền thông liên Host-to-Host bằng cách thiết lập, quản lí và giải phóng các session trong ứng dụng.
   
   f. Lớp Presentation: đảm bảo cho hai tầng lớp app ở 2 đầu có thể nói chuyện được với nhau.
   
   g. Lớp Application: giao tiếp trực tiếp với người dùng, cung cấp ứng dụng mạng, dịch vụ mạng cho tầng lớp ứng dụng, cung cấp cơ chế xá định người dùng.
   
## 4. Cách hoạt động mô hình OSI:

   a. Data Encapsulation:
 
<img src="https://www.routemybrain.com//wp-content/uploads/2010/04/encapsulation.jpg">

   Header: là phần thông tin quản lí của một gói tin.
   
   Sender sẽ truyền một gói dữ liệu người dùng đến lớp **APP** sau đó đóng thêm một lớp HDR cho lớp **PRE**, lớp **PRE** đóng thêm một lớp HDR cho lớp **Ses**, cứ như thế đến lớp **DTL**, ở lớp **DTL** còn được bọc thêm Kiểm tra lỗi *FCS*, đến lớp **PHY** thì tất cả các cấu trúc dữ liệu được chuyển hóa thành 1 dòng Bits nhị phân) và sau đó lại đi ngược lại đến Receive.
   
 b. Truyền thông ngang hàng:
 
  <img src="http://2.bp.blogspot.com/_oI4G5UUCxnU/TRxegRxWZaI/AAAAAAAAAJ4/49EnNEMpPt8/s1600/osi.gif">

     - Segments, Packets, Frames, Bits là đơn vị dữ liệu của lớp Trans, Net, DTL và Phy.
    
## 5. So sánh TCP/IP và OSI
 
  <img src="http://2.bp.blogspot.com/--LdXEFHRLz0/UzQeMLNUyzI/AAAAAAAAADE/YAQAXBPEVqg/s1600/OSI-TCP-IP2.jpg">
  
    - TCP/IP gồm 4 phân lớp trong đó phân lớp App là bao gồm cả 3 lớp **App,Pre và Ses** của OSI.
    
    - Phân lớp Internet <=> lớp Network.
    
    - Phân lớp Network Access bao gồm 2 lớp **DTL và Phy** của OSI.
    
    *TCP/IP ngày nay được sử dụng phổ biến hơn*
