1	Đề bài tổng quát áp dụng Design Pattern cho sinh viên CNTT học OOP bằng C#
________________________________________
Bối cảnh bài tập:
Một công ty phần mềm nhỏ muốn xây dựng một hệ thống quản lý đặt hàng sản phẩm kỹ thuật số, bao gồm các sản phẩm như: phần mềm, ứng dụng mobile, gói dịch vụ cloud, API trả phí, và tài liệu số. Hệ thống cần đảm bảo khả năng mở rộng linh hoạt, dễ bảo trì, và có thể triển khai theo từng bước.
________________________________________
2	Yêu cầu chức năng:
1.	Người dùng có thể tạo tài khoản và đăng nhập.
2.	Người dùng có thể đặt hàng một hoặc nhiều loại sản phẩm.
3.	Mỗi loại sản phẩm có cách khởi tạo khác nhau.
4.	Hệ thống chỉ cho phép một phiên bản quản lý cấu hình đơn hàng hoạt động tại một thời điểm (Singleton).
5.	Mỗi loại sản phẩm sẽ có phương pháp tạo riêng (Factory Method).
6.	Có nhu cầu cải tiến dần hệ thống bằng cách thêm các bước kiểm tra trước và sau khi đặt hàng mà không làm gián đoạn toàn bộ hệ thống hiện tại (Strangler Pattern – như chuyển từ xử lý đơn hàng cũ sang xử lý mới từng phần).
3	Quy trình thực hiện:
Bước 1: Nhận diện bài toán
•	Hệ thống quản lý đặt hàng cho các sản phẩm kỹ thuật số.
•	Mỗi sản phẩm có cách xử lý đơn hàng khác nhau.
•	Cần khả năng quản lý phiên bản cấu hình duy nhất cho đơn hàng.
•	Hệ thống cần cải tiến mà không ảnh hưởng lớn đến toàn bộ kiến trúc.
Bước 2: Lựa chọn giải pháp
•	Tách từng phần chức năng thành các lớp, sử dụng nguyên lý SOLID.
•	Áp dụng Design Pattern để giải quyết các vấn đề cụ thể.
Bước 3: Lựa chọn cấu trúc và giải thuật
•	Áp dụng các mẫu thiết kế:
o	Singleton: Quản lý lớp cấu hình đặt hàng (ví dụ OrderConfigurationManager)
o	Factory Method: Tạo đối tượng Product theo từng loại cụ thể (Software, MobileApp, CloudService…)
o	Strangler Pattern: Phân tách xử lý đơn hàng cũ và mới, tiến hành refactor dần.
Bước 4: Lựa chọn ngôn ngữ lập trình
•	Ngôn ngữ: C#
•	Môi trường: Visual Studio, .NET Framework hoặc .NET Core
