Laravel passport chỉ hỗ trợ giao thức OAUTH không Có SAML	
	
Khi người dùng cố gắng truy cập một ứng dụng từ nhà cung cấp dịch vụ (Laravel), nhà cung cấp dịch vụ sẽ gửi yêu cầu đến bên nhận dạng thứ 3 để xác thực(Slack,Github,Cydas.......).
Nhà cung cấp dịch vụ sau đó sẽ xác minh xác thực và cho phép người dùng đăng nhập.	
	
SAML (Security Assertion Markup Language) và OAuth (Open Authorization) là hai giao thức xác thực phổ biến được sử dụng trong việc quản lý việc xác thực và ủy quyền trong các ứng dụng web. 
Dưới đây là một so sánh giữa hai giao thức này:	
	
1. Mục đích:	
	SAML: Được thiết kế chủ yếu cho việc chia sẻ xác thực giữa các hệ thống khác nhau, thường là giữa nhà cung cấp dịch vụ và nhà cung cấp danh tính.
	OAuth: Tập trung vào việc cấp quyền truy cập từ người dùng cho các ứng dụng bên thứ ba mà không cần chia sẻ thông tin đăng nhập.
2. Phương thức hoạt động:	
	SAML: Dựa trên chứng chỉ (assertions) được phát hành từ một nhà cung cấp danh tính đến một nhà cung cấp dịch vụ để xác thực và ủy quyền.
	OAuth: Sử dụng mã thông báo (tokens) để cấp quyền truy cập từ người dùng cho các ứng dụng bên thứ ba.
3. Phạm vi:	
	SAML: Thường được sử dụng cho các trường hợp SSO (Single Sign-On) và cho việc chia sẻ xác thực giữa các tổ chức khác nhau.
	OAuth: Thường được sử dụng cho việc ủy quyền truy cập từ người dùng cho các ứng dụng bên thứ ba trong cùng một tổ chức.
4. Cấu trúc và chuẩn:	
	SAML: Là một ngôn ngữ đánh dấu dựa trên XML, xác thực bằng chữ ký số và mã hóa.
	OAuth: Là một giao thức xác thực và ủy quyền dựa trên HTTP, thường sử dụng JSON hoặc form-urlencoded để truyền dữ liệu.
5. Bảo mật:	
	SAML: Cung cấp bảo mật cao với việc sử dụng chữ ký số và mã hóa thông điệp.
	OAuth: Bảo mật phụ thuộc vào cách triển khai và cấu hình của các nhà cung cấp OAuth, có thể bảo mật hơn trong các phiên bản mới như OAuth 2.0.
Tóm lại:	
	SAML thích hợp cho việc chia sẻ xác thực giữa các tổ chức khác nhau và triển khai SSO.
	OAuth phù hợp cho việc ủy quyền truy cập giữa các ứng dụng trong cùng một tổ chức.