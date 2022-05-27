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

 - 1.Mở thư mục project bằng Visual Studio Code
 - 2.Truy cập Main.java (Đường dẫn : /ProxyPattern/Main.java)
 - 3.Chọn Run java

#### 3.2. Đối với Visitor Pattern

 - 1.Mở thư mục project bằng Visual Studio Code
 - 2.Truy cập Test.java (Đường dẫn : /VisitorPattern/Main.java)
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

###### 4.1.1.2.2. Protection Proxy

Chúng ta sử dụng Protection Proxy khi muốn chỉ ra những đối tượng cụ thể mới có thể sử dụng dịch vụ, chức năng nào đó bằng các điều kiện ràng buộc bổ sung. Lúc này việc sử dụng protection proxy là cần thiết. Nó chỉ có thể chuyển yêu cầu đến các đối tượng chức năng nếu thông tin người dùng phù hợp với các điều kiện mà người phát triển đã đặt ra. Ví dụ, để có thể thực hiện chức năng quản lý tài khoản thì phải yêu cầu tài khoản đăng nhập có vai trò là Admin, những tài khoản khác thì không cho phép.

###### 4.1.1.2.3. Remote Proxy

Remote proxy cung cấp một đối tượng cục bộ tham chiếu đến một đối tượng khác ở một vị trí khác, thường thông qua kết nối mạng. Proxy thực hiện các hành động cần thiết để mã hóa các yêu cầu chuyển mạng và chấp nhận kết quả từ tài nguyên ở xa trước khi trả lại cho máy khách. 

###### 4.1.1.2.4. Logging Proxy

Khi muốn giữ lịch sử của các yêu cầu đối với đối tượng dịch vụ, lúc này sẽ cần sử dụng logging proxy. Proxy này có thể lưu lại từng yêu cầu trước khi chuyển nó đến dịch vụ.

###### 4.1.1.2.5. Cache Proxy

Cung cấp không gian lưu trữ tạm thời cho các kết quả trả về từ đối tượng nào đó, đặc biệt nếu kết quả trả về lớn. Kết quả này sẽ được tái sử dụng nếu các máy khách có chung một yêu cầu gửi đến. Proxy có thể sử dụng các tham số của yêu cầu làm khóa bộ nhớ cache.

###### 4.1.1.2.6. Smart Reference Proxy

Bổ sung thêm các hành động, phần mở rộng bất cứ khi nào một đối tượng được tham chiếu. Ví dụ: đếm số lượng tham chiếu đến một đối tượng. Ngoài ra, còn một số loại proxy khác như: Monitor Proxy, Firewall Proxy, Synchronization Proxy, Copy-On-Write Proxy,…

###### 4.1.1.3. Cấu trúc của Proxy Pattern

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170717076-1f8d6140-1e36-4dc6-9911-02649c64fc26.png">

Sơ đồ lớp tổng quát của Proxy Pattern

</div>

Các đối tượng tham gia vào Proxy Pattern:
- Subject: Là một Interface định nghĩa các phương thức giao tiếp với client. Nó xác định giao diện chung cho RealSubject (đối tượng thực) và Proxy.
- RealSubject: Là một lớp dịch vụ sẽ thực hiện các thao tác, chức năng thực sự khi có yêu cầu từ phía client.
- Proxy: Là một lớp đại diện cho RealSubject nhằm thực hiện các xử lý các yêu cầu trước và sau khi nó được gửi đến RealSubject. Proxy duy trì một tham chiếu đến đối tượng của RealSubject nhằm truy cập/truy xuất dữ liệu của lớp này.
- Client: Đối tượng sử dụng RealSubject nhưng phải thông qua Proxy.

##### 4.1.2. Đặt vấn đề

Theo như những gì chúng ta đã tìm hiểu, Proxy Pattern được sử dụng để kiểm tra các điều kiện nhất định. Một số đối tượng hoặc tài nguyên cần ủy quyền thích hợp để truy cập chúng, do đó, sử dụng Proxy Pattern là một trong những cách để kiểm tra các điều kiện này. Với Proxy Pattern, chúng ta sẽ kiểm soát quyền truy cập đến các đối tượng linh hoạt hơn.

Ví dụ, chúng ta muốn kiểm soát quyền truy cập vào tài nguyên hệ thống có nhiều loại người dùng. Ở trong hệ thống, chúng ta sẽ có người dùng được phép xem hoặc chỉnh sửa tài nguyên, và một số người khác có thể thực hiện xem, xóa, sửa với tài nguyên.
Giả sử chúng ta có một lớp interface Parent có phương thức là doExam(). Đồng thời ta cũng có một lớp Child implement đến lớp Parent và override phương thức doExam().

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170719007-7b13b3cd-5b98-47bd-90c6-ba3ad4f93245.png">

Cấu trúc đối tượng ban đầu

</div>

Nếu muốn bổ sung các ràng buộc để đối tượng Child phải thỏa mãn thì mới thực hiện hàm doExam(), chúng ta phải thêm các câu lệnh vào trong hàm doExam() hoặc phải viết thêm một phương thức mới checkDoExam(). Sau đó thêm câu lệnh kiểm tra vào hàm doExam().

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170719047-be3606b0-66d5-405d-9e6b-9b26422410d7.png">

Thêm phương thức checkDoExam vào lớp Child

</div>

Vì trường hợp đưa ra ở đây chỉ có một hàm doExam() nên chúng ta thấy đơn giản. Nếu mà lớp Parent có rất nhiều phương thức và lớp Child phải override các phương thức này thì chắc chắn sẽ phải viết rất nhiều câu lệnh kiểm tra hoặc viết thêm các hàm mới. Nhưng nếu làm như vậy, chúng ta sẽ thay đổi cấu trúc của những lớp, hàm, phương thức đã viết trước đó. Điều này là một điều tối kỵ trong lập trình. Bởi vì nếu làm như vậy, chúng ta đã vi phạm nguyên tắc đóng mở trong lập trình. Mặt khác, nếu sửa đổi source code của module hoặc lớp có sẵn, nếu không may ta sẽ làm ảnh hưởng đến tính đúng đắn của chương trình. Hơn nữa, nếu tiến hành sửa trực tiếp trên các lớp có sẵn, nếu bị lỗi thì chương trình sẽ không thực thi được như ý muốn.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170719520-128ec638-77ef-4c1c-aa7e-6f946cb3fe3f.png">

Mỗi phương thức được override từ lớp cha phải thêm các phương thức kiểm tra

</div>

Vì vậy chúng ta cần tạo lớp mới, ta nên kế thừa và mở rộng các module/class có sẵn. Ở trong ví dụ này, cần tạo một lớp Protection Proxy và implement lớp Parent. Các sửa đổi về điều kiện sẽ được thêm vào các hàm override từ lớp Parent.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170719539-9f5e127b-cd08-4344-9143-8bab34c78360.png">

Áp dụng Protection Proxy để giải quyết vấn đề của cấu trúc đối tượng trên

</div>

##### 4.1.3. Áp dụng Proxy Pattern vào ví dụ cụ thể

Khi chúng ta áp dụng Protection Proxy, có nghĩa là chúng ta sẽ không thay đổi trong các lớp đã được tạo trước đó mà ta sẽ tạo thêm lớp Proxy mới. nhằm thực hiện các xử lý các yêu cầu trước khi nó được gửi đến lớp Person. Proxy duy trì một tham chiếu đến đối tượng của lớp Person nhằm truy cập/truy xuất dữ liệu của lớp này. Chúng ta sẽ đặt tên cho lớp Proxy này là PersonProtectProxy. Lớp này sẽ kế thừa từ interface Action và nó sẽ có 3 thuộc tính là name, role và person. 4 chức năng openFile, readFile, writeFile và closeFile sẽ thêm các ràng buộc điều kiện. Chỉ khi người dùng có vai trò là “Admin”, “Manager” mới có thể thực thi 4 chức năng này.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170720841-d9b43a93-7b77-49a0-9cb3-3e8547482ce7.png">

Cấu trúc đối tượng truy xuất file ban đầu

</div>

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170721240-b4c88f16-49ce-4941-8466-66db5ba24757.png">

Sơ đồ lớp của cấu trúc đối tượng sau khi áp dụng Protection Proxy 

</div>

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170728333-071da23f-0600-42f1-81ee-252fe205164b.png">
</div>

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170728344-f8cb6229-cc4b-40da-b1ad-f4ff3dfa0d73.png">

Code của lớp PersonProtectProxy

</div>

Tiếp theo, tiến hành tạo hàm Main để thực thi chương trinh sau khi áp dụng Protection Proxy. Chúng ta cũng sẽ khởi tạo 2 đối tượng person1, person2, thuộc kiểu PersonProtectProxy với tên gọi và vai trò lần lượt là (Cuong, Admin), (Chuyen, Accountant). Sau đó sẽ gọi 4 phương thức openFile, readFile, writeFile, closeFile.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170721259-264cd668-d462-41e9-8704-51a7c9c7fe36.png">

Thực thi chương trình sau khi áp dụng Protection Proxy Pattern

</div>

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170721557-c7dd727e-030c-4b24-afa4-a7b6621500e2.png">

Kết quả thực thi chương trình sau khi áp dụng Protection Proxy Pattern

</div>


##### 4.1.4. Tóm tắt Proxy Pattern

Tên Pattern: Proxy.

Nhóm Pattern: nhóm cấu trúc.

Định nghĩa: Proxy là một mẫu thiết kế cho phép ta cung cấp thêm một đối tượng, lớp thay thế cho lớp gốc ban đầu. Lớp Proxy đại diện cho đối tượng gốc đó, do đó nó sẽ kiểm soát quyền truy cập đối này. Tất cả các truy cập trực tiếp đến một đối tượng gốc ban đầu sẽ được chuyển vào lớp trung gian Proxy. Lớp này cho phép thêm điều kiện, thực hiện một điều gì đó trước khi yêu cầu được chuyển đến đối tượng gốc.

Sơ đồ lớp tổng quát:

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170729192-de4d217b-a4e1-4c7b-861c-ccb0203f586e.png">

Kết quả thực thi chương trình sau khi áp dụng Protection Proxy Pattern

</div>

Các thành phần trong sơ đồ lớp tổng quát:
- Subject: Là một Interface định nghĩa các phương thức giao tiếp với client. Nó xác định phương thức chung cho RealSubject (đối tượng thực) và Proxy.
- RealSubject: Là một lớp sẽ thực hiện các thao tác, chức năng thực sự khi có yêu cầu từ phía client.
- Proxy: Là một lớp đại diện cho RealSubject nhằm thực hiện các xử lý các yêu cầu trước và sau đó nó được gửi đến lớp RealSubject. Proxy duy trì một tham chiếu đến đối tượng của RealSubject nhằm truy cập/truy xuất dữ liệu của lớp này.
- Client: Đối tượng sử dụng RealSubject nhưng phải thông qua Proxy.

Vấn đề áp dụng: Khi muốn bổ sung các điều kiện vào các lớp có sẵn, chúng ta không thể trực tiếp sửa đổi các source code này vì làm như vậy sẽ vi phạm nguyên tắc đóng mở trong lập trình. Vì vậy, cần phải tạo một lớp Proxy mới, lớp này sẽ kiểm tra các điều kiện trước khi gọi đến các đối tượng gốc ban đầu.

Các bài toán nên sử dụng Proxy Pattern: 
- Kiểm soát quyền truy xuất các phương thức của đối tượng.
- Bổ sung thêm các chức năng, ràng buộc điều kiện trước khi thực thi phương thức của đối tượng gốc
- Bổ sung các phương thức, chức năng mới cho đối tượng gốc mà không sửa đổi code của nó.
- Tiết kiệm bộ nhớ, thời gian khi có nhiều truy cập vào các đối tượng có chi phí khởi tạo lớn.
- Khi muốn theo dõi trạng thái và vòng đời đối tượng	
- Khi đối tượng gốc nằm trong hệ thống cũ hoặc thư viện bên thứ 3.

Ưu điểm:
- Proxy góp phần làm tăng tính bảo mật cho chương trình bằng cách thêm các điều kiện trước khi gọi tới lớp có sẵn.
- Proxy khá là dễ áp dụng vào các dự án.
- Proxy có thể giúp cải thiện hiệu suất của ứng dụng bằng cách lưu vào bộ nhớ đệm các đối tượng nặng hoặc các đối tượng được truy cập thường xuyên.
- Lập trình viên có thể kiểm soát được chức năng, dịch vụ mà không cần phía máy khách biết về nó.
- Lập trình viên có thể quản lý của vòng đời của chức năng khi mà phía máy khách không quan tâm đến nó
- Proxy hoạt động ngay cả khi dịch vụ không sẵn sàng hoặc không có sẵn.

Khuyết điểm:
- Code sẽ trở nên phức tạp hơn khi phải tạo ra nhiều lớp proxy mới.
- Phản hồi từ đối tượng dịch vụ của thể bị chậm trễ.


##### 4.1.5. Kết luận

Với sự đa dạng và các ưu điểm của Proxy Pattern, lập trình viên có thể tận dụng pattern này để thiết kế code cũng như là hệ thống trở nên linh hoạt, hoạt động tốt hơn mà vẫn đảm bảo sự toàn vẹn của các lớp đối tượng ban đầu.

#### 4.2. Visitor Pattern

##### 4.2.1. Giới thiệu chung về Visitor Pattern

###### 4.2.1.1. Giới thiệu 

Có rất nhiều pattern thuộc nhóm hành vi mà chúng ta có thể nghiên cứu, tìm hiểu để áp dụng cho các vấn đề mà ta đang gặp phải hay ít nhất là dùng để tránh đi các lỗi tiềm ẩn trong khi lập trình. Mỗi loại pattern ở nhóm này đều có điểm hay, điểm đặc biệt và mức độ kiến thức để chúng ta tiếp thu cũng phân hóa từ dễ đến khó và ở phần này, chúng ta sẽ đi tìm hiểu về Visitor Pattern.

Visitor Pattern là một pattern thuộc nhóm hành vi, cho phép lập trình viên có thể dễ dàng định nghĩa các phương thức mới cho các đối tượng mà không làm thay đổi lớp hiện tại của chúng.

###### 4.2.1.2. Cấu trúc của Visitor Pattern 

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170731011-26730f93-e930-43d0-840a-0e9ca2effd87.png">

Sơ đồ lớp tổng quát của Visitor Pattern

</div>

Các thành phần tham gia Visitor Pattern bao gồm:
- Visitor: Có thể là một lớp interface hoặc là một lớp abstract được sử dụng để khai báo các phương thức cho các ConcreteVisitors. Mỗi phương thức được định nghĩa chấp nhận các ConcreteElement làm tham số - phương thức này thường có tên gọi là visit(). Do đó, mặc dù tên các phương thức này có thể giống nhau nhưng sẽ được thực hiện dựa trên việc tham số được truyền vào là gì.
- ConcreteVisitors: Các lớp sẽ override lại các phương thức được khai báo trong lớp Visitors và định nghĩa lại các hoạt động sẽ được thực thi trong các phương thức dựa vào tham số đối tượng được truyền vào.
- Element: Có thể là một lớp interface hoặc là một lớp abstract có định nghĩa phương thức chấp nhận đối tượng Visitor làm tham số - phương thức này thường có tên gọi là accept().
- ConcreteElement: Các lớp sẽ override lại phương thức accept() từ lớp Element.
- Client: Sử dụng phương thức accept() của Element cho phép đối tượng Visitor làm tham số để thực hiện một phương thức tương ứng.

Như vậy, dựa vào các thành phần tham gia Visitor Pattern ta có thể trình bày cách thiết kế để có thể dễ dàng giúp các đối tượng thực hiện một phương thức mới mà không làm thay đổi các lớp hiện tại. Như thế này, với phương thức mới chúng ta muốn thêm cho đối tượng, ta sẽ tách riêng ra thành lớp interface hoặc trừu tượng Visitor. Như vậy mỗi phương thức visit() trong Visitor sẽ được định nghĩa bao gồm tham số chính là các đối tượng muốn thực hiện phương thức mới. Sau đó để định nghĩa hành động các phương thức mới mà các đối tượng muốn thực hiện, ta tạo ra lớp ConcreteVisitors để ghi đè lại phương thức visit() và thực hiện code ở các phương thức visit có tham số đối tượng tương ứng. Cuối cùng để các phương thức visit() có thể lấy đối tượng muốn thực hiện phương thức mới làm tham số thì ta phải định nghĩa một phương thức accept() ở bên trong các đối tượng này.

##### 4.2.2. Đặt vấn đề

Giả sử ta có một cấu trúc đối tượng bao gồm lớp interface là BigClass có phương thức Action(). Lúc này có hai lớp SmallClass1 và SmallClass2 đều implements đến BigClass và đều phải override lại phương thức Action().

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170731767-35580756-dd19-42e3-96df-e1a2d3f8b10d.png">

Cấu trúc đối tượng ban đầu của phần đặt vấn đề

</div>

Nếu ta mở rộng cấu trúc đối tượng này bằng cách thêm một phương thức mới có tên là do() vào lớp interface BigClass. Thì bắt buộc hai lớp SmallClass1 và SmallClass2 đều phải tiếp tục override lại phương thức do() vừa mới thêm.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170731833-87de52c0-4755-412a-9d8c-9feff4abb370.png">

Cấu trúc đối tượng của phần đặt vấn đề sau khi thêm phương thức do()

</div>

Ở đây ta thấy đây chỉ là một cấu trúc đối tượng đơn giản nên việc thêm phương thức này đối chúng ta sẽ cảm thấy bình thường, không có gì quá nghiêm trọng. Nhưng rõ ràng chúng ta đã vô tình sửa đổi code ở các lớp đối tượng và chính điều này đã vi phạm nguyên tắc đóng mở trong lập trình. Thêm nữa sự thay đổi, mở rộng liên tục xảy ra thì lập trình viên sẽ tốn khá nhiều thời gian, công sức để đi thay đổi code ở từng lớp đối tượng, chưa kể đến việc nếu bất cẩn thì sẽ làm hư luôn cả lớp đối tượng và cuối cùng lập trình viên sẽ nhận được kết quả là một cấu trúc đối tượng rườm rà, khó để đọc và hiểu.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170731855-9e578b78-dbcd-46b2-a308-cf4654acdf04.png">

Cấu trúc đối tượng của phần đặt vấn đề sau khi thêm nhiều phương thức mới

</div>

Cách thêm phương thức mới như trên sẽ gây ra rất nhiều khó khăn cho lập trình viên trong quá trình phát triển, mở rộng ứng dụng, hệ thống trong tương lai.

Vậy chúng ta có thể thấy được vấn đề chúng ta đang gặp phải như sau: khi thêm các phương thức mới vào trực tiếp các lớp đối tượng thì điều này sẽ vi phạm nguyên tắc đóng mở trong lập trình do có sự thay đổi ở các lớp đối tượng. Bên cạnh đó, tùy vào mức độ phức tạp của cấu trúc đối tượng, lập trình viên có thể sẽ có thể tốn nhiều công sức, thời gian để đi thay đổi từng lớp đối tượng và nếu không cẩn thận thì vô tình sẽ làm cho code bị hư hỏng, không hoạt động đúng như mong muốn. Việc thêm trực tiếp các phương thức cũng làm cho các lớp đối tượng trở nên rườm ra, khiến các lập trình viên sẽ cảm thấy không thoải mái, khó khăn khi đọc và cố gắng hiểu được những gì mà đối tượng có thể thực hiện. Chính điều này sẽ gây ảnh hưởng đến hiệu suất làm việc của lập trình viên và cũng gây ảnh hưởng đến khả năng mở rộng và phát triển code.

Do đó nếu áp dụng Visitor Pattern trong trường hợp này ta hoàn toàn có thể giải quyết được vấn đề hiện tại. Ta có thể bảo đảm tính đóng mở trong lập trình và có thể dễ dàng thêm một phương thức mới cho các đối tượng mà không cần tốn quá nhiều công sức thời gian.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170731886-ccbdae85-b5a7-44a0-ad90-1c31ed7e5537.png">

Áp dụng Visitor Pattern vào vấn đề

</div>


##### 4.2.3. Áp dụng Visitor Pattern vào ví dụ cụ thể

Để hiểu rõ hơn về vấn đề mà chúng ta phải đối mặt khi thêm phương thức mới bằng cách thông thường và giải pháp để giải quyết vấn đề này thì chúng ta sẽ đi tìm hiểu thông qua bài toán ứng dụng 2. Chúng ta sẽ có các lớp đối tượng như thế này: một lớp absatract tên Animal gồm một phương thức getName() và một phương thức abstract tạo ra âm thanh là makeSound(). Tiếp đó chúng ta sẽ tạo ra hai lớp Cat và Dog để tiến hành kế thừa lớp Animal và override lại phương thức makeSound(). Đây là cấu trúc đối tượng vật nuôi trong nhà ban đầu của chúng ta.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170733807-fe896cef-5570-4442-9769-12d74de9a83b.png">

Cấu trúc đối tượng vật nuôi ban đầu

</div>

Nhưng sau một thời gian quan sát hành vi các con vật nuôi trong nhà, ta phát hiện thêm chúng có khả năng chơi đùa với những quả banh, do đó ta muốn thêm khả năng này vào trong cấu trúc đối tượng đã tạo. Lúc này ta phải thực hiện các bước như sau: thêm phương thức abstract playWithBall() vào lớp Animal và buộc hai lớp Cat và Dog phải tiếp tục override lại phương thức mới này. Vậy là cấu trúc đối tượng của ta bây giờ đã được mở rộng thêm bằng việc thêm một phương thức mới.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170734240-36ea96ee-a1de-4677-bda7-3a1d7572c936.png">

Cấu trúc lớp đối tượng vật nuôi khi thêm phương thức playWithBall()

</div>

Đến lúc này, chúng ta lại gặp phải vấn đề đã được đề cập ở trên đó là vi phạm nguyên tắc đóng mở trong lập trình do ta đã trực tiếp thay đổi các lớp đối tượng hiện tại của cấu trúc đối tượng. Và nếu ta càng muốn thêm các phương thức mới cho các con vật nuôi thì cấu trúc đối tượng trên sẽ thay đổi liên tục và dần trở nên rườm rà hơn. 

Vậy để giải quyết vấn đề này, chúng ta sẽ áp dụng Visitor Pattern vào trong cấu trúc đối tượng để có thể dễ dàng mở rộng cấu trúc đối tượng bằng việc thêm các phương thức mới mà không sợ bị vi phạm nguyên tắc đóng mở.

Dựa vào cách thiết kế và hoạt động của Visitor Pattern mà chúng ta đã đề cập đến ở phần giới thiệu, chúng ta tiến hành thiết kế lại cấu trúc đối tượng vật nuôi của chúng ta kết hợp với việc sử dụng Visitor Pattern thông qua một sơ đồ lớp.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170734507-ef3b694e-c2c7-42f7-8dc2-e408055f07e1.png">

Sơ đồ Visitor Pattern áp dụng cho ví dụ cụ thể

</div>

Dựa vào sơ đồ lớp được thiết kế, đầu tiên chúng ta sẽ tiến hành tách các phương thức hành động của các con vật nuôi ra một lớp đối tượng riêng biệt là lớp interface AnimalVisitor. Do chúng ta có hai lớp đối tượng Cat và Dog, do đó ta sẽ thêm hai phương thức visit(Cat cat) và visit(Dog dog) vào trong lớp AnimalVisitor.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170735267-81bf8142-ed46-4d0e-b4bb-120373c496ce.png">

Code của lớp AnimalVisitor

</div>

Sau đó ta lần lượt xây dựng lớp đối tượng MakeSoundVisitor đại diện cho phương thức makeSound() và tiến hành override phương thức visit cũng như định nghĩa các hành động make sound tương ứng với tham số đối tượng vật nuôi được truyền vào.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170735273-9b9c26f7-5b77-4463-a476-079431dec204.png">

Code của lớp MakeSoundVisitor

</div>

Tiếp theo là lớp đối tượng PlayWithBallVisitor đại diện cho phương thức playWithBall() và ta cũng tiến hành tương tự.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170735282-b7e34dc9-4a76-4a4a-b1b4-a875f657a86b.png">

Code của lớp PlayWithBallVisitor

</div>

Để cho các lớp Visitor có thể đi vào trong các lớp đối tượng vật nuôi và nhận tham số là đối tượng vật nuôi này để thực hiện hành động tương ứng thì ta tiến hành thêm phương thức accept(AnimalVisitor v) vào cấu trúc lớp đối tượng vật nuôi.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170735289-dc28be5c-dc8e-468d-b9e3-97af8f1de787.png">

Code của lớp Animal sau khi áp dụng Visitor Pattern

</div>


<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170735293-85a8ede2-fe7b-4ebe-9d74-909dc81a7cb5.png">

Code của lớp Cat sau khi áp dụng Visitor Pattern

</div>

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170735297-8619bd10-e04b-48fc-8213-0ff08221b4c3.png">

Code của lớp Dog sau khi áp dụng Visitor Pattern

</div>

Sau khi chúng ta đã thiết kế lại cấu trúc đối tượng vật nuôi kết hợp với việc sử dụng Visitor Pattern thì cách chúng ta chạy chương trình sẽ có một chút thay đổi so với ban đầu. Ví dụ chúng ta tạo ra một đối tượng Dog và chúng ta muốn đối tượng này thực thi hành động tạo ra âm thanh thì chúng ta sẽ tạo ra một đối tượng MakeSoundVisitor và thông qua phương thức accept của đối tượng Dog chúng ta cho phép đối tượng MakeSoundVisitor đi vào bên trong đối tượng Dog và nhận tham số chính là đối tượng Dog thông qua phương thức visit của MakeSoundVisitor. Lúc này phương thức visit được định nghĩa trong lớp đối tượng MakeSoundVisitor có tham số là đối tượng Dog và nó sẽ thực thi hành động tạo ra âm thanh tương ứng với đối tượng Dog.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170735302-7addab27-cc6a-4000-8650-f85747e9b84d.png">

Code lớp Test

</div>

Như vậy chúng ta đã thấy được rằng, sau khi áp dụng Visitor Pattern thì việc chúng ta muốn thêm các phương thức mới sẽ trở nên vô cùng dễ dàng mà vẫn đảm bảo được nguyên tắc đóng mở và vẫn giữ cho cấu trúc đối tượng hiện tại của ta trông vô cùng gọn gàng, dễ hiểu. Ví dụ như đến bây giờ ta phát hiện ra các con vật nuôi của mình cũng có khả năng giữ nhà và ta muốn thêm một phương thức mới là protectHome. Vì đã áp dụng Visitor Pattern rồi nên thay vì thêm phương thức này vào trực tiếp cấu trúc đối tượng ta chỉ cần tạo ra một lớp đối tượng mới tên ProtectHomeVisitor đại diện cho phương thức protectHome của các vật nuôi và cũng implements đến lớp AnimalVisitor. Tương tự như MakeSoundVisitor và PlayWithBallVisitor, ta cũng tiến hành override lại phương thức visit và định nghĩa các hành động giữ nhà tương ứng với các tham số đối tượng vật nuôi.

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170735309-ea0bdcfd-97e4-4da0-b1df-dcaf9aaa5b45.png">

Code của lớp ProtectHomeVisitor

</div>

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170737750-79aa861c-4a5e-4e21-82da-7b754bd28883.PNG">

Kết quả thực thi chương trình sau khi áp dụng Visitor Pattern

</div>

Như vậy, sau khi tìm hiểu qua một ví dụ cụ thể, xác định được vấn đề của ví dụ và đưa ra giải pháp là áp dụng Visitor Pattern thì ta có thể thấy rằng: việc sử dụng pattern này giúp ta dễ dàng thêm phương thức mới cho các đối tượng mà không cần phải thay đổi lớp đối tượng hiện tại, vẫn đảm bảo được nguyên tắc đóng mở trong lập trình và đồng thời cũng làm cho lớp đối tượng của ta trông gọn gàng, dễ nhìn và dễ hiểu.

##### 4.2.4. Tóm tắt Visitor Pattern

Tên pattern: Visitor

Nhóm pattern: nhóm hành vi.

Định nghĩa: Visitor Pattern là một pattern thuộc nhóm hành vi, cho phép lập trình viên có thể dễ dàng định nghĩa các phương thức mới cho các đối tượng mà không làm thay đổi lớp hiện tại của chúng.

Sơ đồ lớp tổng quát:

<div align="center">

<img src="https://user-images.githubusercontent.com/75523801/170736730-680d8718-8531-4bab-ad8d-9597e8712657.png">

Sơ đồ lớp tổng quát của Visitor Pattern

</div>

Các thành của Visitor Pattern:
- Visitor: Có thể là một lớp interface hoặc là một lớp abstract được sử dụng để khai báo các phương thức cho các ConcreteVisitors. Mỗi phương thức được định nghĩa chấp nhận các ConcreteElement làm tham số - phương thức này thường có tên gọi là visit(). Do đó, mặc dù tên các phương thức này có thể giống nhau nhưng sẽ được thực hiện dựa trên việc tham số được truyền vào là gì.
- ConcreteVisitors: Các lớp sẽ override lại các phương thức được khai báo trong lớp Visitors và định nghĩa lại các hoạt động sẽ được thực thi trong các phương thức dựa vào tham số đối tượng được truyền vào.
- Element: Có thể là một lớp interface hoặc là một lớp abstract bắt có định nghĩa phương thức chấp nhận đối tượng Visitor làm tham số - phương thức này thường có tên gọi là accept().
- ConcreteElement: Các lớp sẽ override lại phương thức accept() từ lớp Element.
- Client: Sử dụng phương thức accept() của Element cho phép đối tượng Visitor làm tham số để thực hiện một phương thức tương ứng.

Vấn đề áp dụng: thêm các phương thức mới cho đối tượng bằng cách thông thường sẽ dẫn đến việc phá vỡ nguyên tắc đóng mở trong lập trình và khiến lớp đối tượng trở nên phức tạp hơn. Do đó ta cần một cách để có thể thêm các phương thức mới này mà vẫn giữ nguyên được lớp đối tượng ban đầu.

Các bài toán nên sử dụng Visitor Pattern:
- Khi cần thêm một hay nhiều phương thức mới cho đối tượng mà vẫn muốn đảm bảo nguyên tắc đóng mở trong lập trình.
- Khi phương thức muốn thêm chỉ có ý nghĩa trong một số đối tượng trong cấu trúc đối tượng, vì có thể một số đối tượng khác không thực hiện phương thức này dẫn đến việc vẫn phải thêm phương thức những không định nghĩa nội dung thực hiện phương thức.
- Cấu trúc đối tượng thường xuyên được thêm phương thức mới hoặc các phương thức của cấu trúc đối tượng liên tục bị sửa đổi.

Ưu điểm:
- Bảo đảm nguyên tắc đóng/mở trong lập trình.
- Dễ dàng mở rộng cũng như thay đổi các phương thức của lớp đối tượng.

Khuyết điểm:
- Nếu như xuất hiện hoặc mất đi một đối tượng mới trong cấu trúc đối tượng có áp dụng Visitor Pattern thì buộc phải đổi toàn bộ các lớp Visitor liên quan.
- Các Visitors có thể bị hạn chế truy cập vào các trường dữ liệu hoặc các phương thức thuộc dạng private của đối tượng mà nó đang làm việc.


##### 4.2.4. Kết luận

Đối với bài toán cho việc thêm phương thức mới cho các đối tượng mà không làm thay đổi lớp hiện tại của chúng có thể được giải quyết bởi Visitor Pattern. Nhờ cách thức hoạt động mà khi áp dụng pattern này, lập trình viên có thể dễ dàng mở rộng hệ thống thông qua việc mở rộng các phương thức của lớp đối tượng. Để cho việc mở rộng, phát triển hệ thống trong tương lai được trở nên dễ dàng, thuận tiện thì lập trình viên cần xem xét kĩ càng hơn để áp dụng Visitor Design Pattern vào trong hệ thống. Bên cạnh những ưu điểm thì tất nhiên Visitor Design Pattern cũng sẽ có một số khuyết điểm vì thế, lập trình viên nên tận dụng các Pattern khác để hạn chế khuyết điểm và khiến hệ thống trở lên mạnh mẽ, linh hoạt hơn.

