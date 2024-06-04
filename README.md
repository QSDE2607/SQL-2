# SQL-2
<h1> Thiết kế và chuẩn hóa cơ sở dữ liệu bán hàng </h1>

<h2> Tổng quan dự án </h2>

Trong bài ASM này, các bạn sẽ cần thiết kế cơ sở dữ liệu cho cửa hàng để quản lý việc bán hàng. Các bạn sẽ cần thực hiện hết các bước trong một bài toán thực tế đó là xác định đối tượng, thiết kế lược đồ ER, ERD và chuấn hoá cơ sở dữ liệu.

<h2> 1. Xác định các đối tượng và quan hệ giữa các đối tượng </h2>

Một tiệm tạp hóa cần quản lý việc mua bán hàng hóa của tiệm tạp hóa. Sau đây là phần mô tả theo các nghiệp vụ hàng ngày của tiệm:

Nhân viên quản lý mỗi hàng hóa trong tiệm nhờ vào tên riêng của hàng hóa và có đơn vị tính khác nhau. Ví dụ như: Nước suối Aquafina với đơn vị là chai, sữa ngôi sao Phương Nam với đơn vị là hộp, …
Mỗi hàng hóa có một mã hàng hóa riêng để phân biệt với các hàng hóa khác. Mã số là các mã vạch được in trên hàng hóa. Mỗi hàng hóa sẽ có giá mua và giá bán riêng sau đó được tính ra giá bình quân và có ghi ngày cập nhật (ngày mua hoặc ngày bán gần nhất của hàng hóa).
Mỗi hàng hóa còn có một đơn vị tính khác như: thùng, lốc, … với số lượng, giá mua và giá bán riêng. Ví dụ: thùng thì có 24 chai, lốc thì có 6 chai, … Đơn vị tính ở đây khác với đơn vị tính của từng hàng hóa đơn lẻ ở trên. 
Khi bán các mặt hàng sẽ có đơn hàng bán để biết được khách hàng nào đã mua hàng, mua vào ngày nào với giá tổng cộng là bao nhiêu và nhân viên nào đã trực tiếp ghi đơn hàng đó.
Mỗi đơn hàng sẽ có chi tiết của đơn hàng riêng cho biết khách hàng đã đặt mua nhưng mặt hàng nào với có giá bán, giá mua, số lượng, và thành tiền là bao nhiêu.
Nhân viên làm việc trong tiệm phải được quản lý về: Tên, địa chỉ, điện thoại, ... và phải cấp quyền để đăng nhập vào hệ thống bán hàng với tên đăng nhập và mật khẩu.
Ngoài ra nhân viên còn có nhiệm vụ nhận hàng từ các nhà cung cấp thông qua đơn hàng mua có ngày đặt hàng, nhà cung cấp và tổng giá tiền là bao nhiêu.
Mỗi đơn hàng mua sẽ có một chi tiết đơn hàng mua riêng cho biết đã mua những mặt hàng nào có giá mua, số lượng và thành tiền là bao nhiêu.
Khi mua hàng ta cần lưu lại thông tin những nhà cung cấp: tên, địa chỉ, điện thoại, … để tiện quản lý.
Nhiệm vụ của các bạn là xác định được các đối tượng cần có trong một cơ sở dữ bán hàng và các thuộc tính của các đối tượng, sau đó thể hiện qua sơ đồ ER.

<h2> 2. Thiết kế ERD </h2>

Từ các đối tượng và quan hệ giữa chúng đã tìm được ở yêu cầu 1, các bạn hãy thiết kế mô hình ERD và tạo các bảng thành công trong cơ sở dữ liệu vật lý.

<h2> 3. Thực hiện tìm ra các mối quan hệ của các cột </h2>

Như các bạn đã được học, khi chuẩn hoá cơ sở dữ liệu các bạn hay dựa vào các phụ thuộc hàm để chuẩn hoá. Ở yêu cầu này, các bạn hãy liệt kê các phụ thuộc hàm của các bảng. Cách liệt kê các bạn có thể tham khảo tại phần tài nguyên.

<h2> 4. Thực hiện chuẩn hoá cơ sở dữ liệu về dạng NF2 </h2>

Các bạn hãy kiểm tra các bảng đã thiết kế ở yêu cầu 2 và đưa về dạng chuẩn hoá NF2.

Gợi ý: Về cách thức hiện chúng ta sẽ có hai cách để đưa về dạng NF2:

Cách 1: Dựa trên phụ thuộc hàm mà các bạn đã thực hiện ở yêu cầu 3 tương tự như các Lab các bạn đã thực hiện.
Cách 2: Dựa vao đặc điểm nhận biết như phần tài nguyên tham khảo. Thông thường ngoài thực tế, chúng ta sẽ dựa theo cách làm này để chuẩn hoá.
Dù thực hiện theo cách nào thì ở yêu cầu này, các bạn đều sẽ phải lập luận để đưa ra kết quả chuẩn hoá.

<h2> 5. Thực hiện chuẩn hoá cơ sở dữ liệu về dạng NF3 (không bắt buộc) </h2> 

Ở yêu cầu này, các bạn hãy kiểm tra và chuẩn hoá cơ sở dữ liệu từ dạng NF2 đã thực hiện ở yêu cầu 4 về dạng NF3.
