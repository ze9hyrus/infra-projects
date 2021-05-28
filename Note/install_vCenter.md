#### Các tính năng cốt lõi:

- Centralized user authentication
  - vCenter Single Sign-On: mỗi máy chủ ESXi đều cần đăng nhập tài khoản quản trị viên để quản lí. Nếu hệ thống có quy mô lớn, đồng nghĩa với việc cần phải đăng nhập tài khoản trên từng máy chủ, hoặc khi đổi mật khẩu cũng cần đổi trên từng máy chủ. Vì vậy SSO(Single Sign-On) là điều không thể thiếu và cần có trước khi cài đặt vCenter Server. Nói chung, SSO là một cách xác thực an toàn đối với các sản phẩm VMware
- Web Client server: Các client HTML5 mới, là một dịch vụ phía máy chủ để quản trị vSphere từ trình duyệt web
- Extensible framework: framework này cung cấp nền tảng cho các dịch vụ cốt lõi của vCenter Server và cho phép các nhà phát triển bên thứ ba tạo các ứng dụng được xây dựng xung quanh Máy chủ vCenter.

#### Chọn phiên bản, phần cứng và lên kế hoạch cài đặt

- Chọn phiên bản vCenter 
- Chọn phần cứng vật lý
- Kế hoạch cài đặt:
  - Protecting the Platform Services Controller
  - Protecting vCenter Servers
  - Protecting the vCenter Database