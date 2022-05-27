<div align="center">

**TỔNG LIÊN ĐOÀN LAO ĐỘNG VIỆT NAM**<br>
**TRƯỜNG ĐẠI HỌC TÔN ĐỨC THẮNG**<br>
**KHOA CÔNG NGHỆ THÔNG TIN**

<img src="https://upload.wikimedia.org/wikipedia/vi/1/1b/TĐT_logo.png"  alt="TDT-Logo" width="100">

#### BÀI TẬP TIỂU LUẬN GIỮA KỲ MÔN

#### MẪU THIẾT KẾ


</div>

<div align="right" style="margin-top: 150px">

_Người hướng dẫn:_ **Thầy Đặng Huỳnh Trung Tín** <br>
_Người thực hiện:_ **Nguyễn Phú Cường - 51800356** <br>
**Viên Quốc Chuyên - 51800353** <br>
_Khóa:_ **22**

</div>

<div align="center" style="margin-top: 50px">

**THÀNH PHỐ HỒ CHÍ MINH, NĂM 2022**

</div>

---

### 1. GIỚI THIỆU VỀ BÀI TOÁN ỨNG DỤNG

#### 1.1. Bài toán ứng dụng 1

Giả sử trong một hệ thống của công ty nọ có các tài liệu công việc. Mọi người dùng trong hệ thống không phải ai cũng có quyền mở, xem, ghi, đóng file. Một vài người có thể có toàn quyền, cũng có một số người chỉ giới hạn ở mức xem và đóng file. Làm thế nào để khi thêm người mới vào hệ thống thì bằng 1 cách nào đó đơn giản nhất có thể giới hạn quyền của người dùng đó ngay lập tức. Ở đây chúng em áp dụng proxy pattern, về lí do sẽ được nêu rõ ở những phần bên dưới. 

#### 1.2. Bài toán ứng dụng 2

Giả sử chúng ta muốn xây dựng một chương trình mô phỏng lại hành động của các con vật nuôi trong nhà và ban đầu chúng ta mới chỉ nghĩ ra được một hành động của các con vật là tạo ra âm thanh.


### 2. YÊU CẦU

#### 2.1 Visual studio code
#### 2.Java Development Kit (JDK)

### 3. CÁCH THỰC THI ỨNG DỤNG

#### 3.1. Đối với Proxy Pattern

1.Mở thư mục project bằng Visual Studio Code

2.Truy cập Main.java
Đường dẫn : /ProxyPattern/Main.java

3.Chọn Run java

#### 3.2. Đối với Visitor Pattern

 - 1.Mở thư mục project bằng Visual Studio Code

 - 2.Truy cập Test.java
  Đường dẫn : /VisitorPattern/Main.java

 - 3.Chọn Run java

### 4. TÌM HIỂU VÀ TRIỂN KHAI PATTERN

#### 4.1. Proxy Pattern

##### 4.1.1. Giới thiệu chung về Proxy Pattern

###### 4.1.1.1. Giới thiệu 

  Như chúng ta đã biết, mẫu thiết kế được chia làm 3 nhóm chính: Nhóm khởi tạo (creational pattern), nhóm cấu trúc (structural pattern) và nhóm hành vi (behavioral pattern). Mỗi nhóm sẽ có những chức năng khác nhau. Nhóm Khởi tạo cung cấp giải pháp liên quan đến khởi tạo đối tượng, che giấu logic của việc tạo nó, thay vì khởi tạo trực tiếp đối tượng bằng phương thức new. Nhóm Cấu trúc liên quan tới lớp và các thành phần đối tượng. Nhưng mẫu thiết kế thuộc nhóm này nhằm định nghĩa, thiết lập quan hệ giữa các đối tượng. Nhóm Hành vi được dùng trong thực hiện hành vi của các đối tượng. Áp dụng mẫu thiết kế góp phần giúp cho code dễ dàng đọc, hiểu, bảo trì hơn. Mẫu thiết kế cũng giúp các nhà phát triển tạo ra hệ thống phần mềm đảm bảo cho code của họ tuân thủ nguyên tắc thiết kế phần mềm. Ở phần này, chúng ta sẽ đi tìm hiểu một mẫu thiết kế thuộc nhóm Cấu trúc, đó là Proxy.

  Proxy trong tiếng Anh có nghĩa là “Ủy quyền” hoặc “Người đại diện”, là một mẫu thiết kế thuộc nhóm Cấu trúc (Structural pattern). Proxy cho phép cung cấp một đối tượng, lớp thay thế sẽ được ủy quyền, đại diện cho đối tượng, lớp khác. Nó kiểm soát quyền truy cập đối với đối tượng ban đầu, tất cả các truy cập trực tiếp đến một đối tượng gốc ban đầu sẽ được chuyển vào lớp trung gian (lớp Proxy). Lớp này cho phép thêm điều kiện, thực hiện một điều gì đó trước khi yêu cầu được chuyển đến đối tượng gốc.

###### 4.1.1.2. Phân loại Proxy Pattern


###### 4.1.1.2.1. Virtual Proxy

Khi có một đối tượng dịch vụ có cấu trúc phức tạp, chứa dữ liệu lớn luôn luôn chạy làm lãng phí tài nguyên hệ thống, mặc dù chỉ cần gọi nó trong một vài trường hợp. Thay vì khởi tạo đối tượng khi ứng dụng chạy, proxy sẽ tạo đối tượng ở lần truy xuất đầu tiên, những lần gọi kế tiếp chỉ cần tái sử dụng lại mà không cần khởi tạo, nhằm tiết kiệm tài nguyên hệ thống. 


- 1. aaaaaaaaaaaaaaaaaaaaaaaa


<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170718007-2afa0add-f912-420b-ab91-2168191521ca.png" alt="Proxy Pattern Diagram">

</div>