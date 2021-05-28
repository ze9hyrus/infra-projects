#### Kiến trúc

Là phần mềm kích thước nhỏ (vài trăm MB) nhưng là một hệ thống phức tạp 

- The kernel: VMkernel - trung tâm của ESXi OS, kiểm soát phần lớn các thành phần khác, quản lý tài nguyên và lập lịch, chạy máy ảo và khởi động các quy trình cần thiết cho máy chủ quản lý.
  - The Virtual Machine Monitor (VMM): gửi các yêu cầu về storage và network tới VMkernel và chuyển tất cả các yêu cầu khác tới quy trình VMX. Có một VMM xử lý cho mỗi CPU ảo trong mỗi máy ảo.
  - The resource scheduler: lấy  các yêu cầu tài nguyên từ quy trình VMM và VMX, lập lịch cho chúng trên hệ thống vật lý. Nó truy cập trực tiếp đến phần cứng vật lý và cấp tài nguyên cho máy ảo
  - User World space: là các quy trình k dựa trên kernel, 2 quy trình quan trọng nhất:
    - Virtual Machine Execution(VMX) : kiểm soát bàn phím, chuột và màn hình (KMS) của VM; remote control; và một số I / O không quan trọng như CD-ROM. Mỗi máy ảo sẽ có một VMX duy nhất
    - Hostd: là một dịch vụ proxy cho VMkernel. Tất cả giao diện đồ họa và dòng lệnh (CLI) và các lệnh gọi giao diện (API) được chuyển đến quá trình VMX  hoặc hạt nhân thích hợp thông qua hostd. Những điều này có thể đến từ máy khách vSphere Host, một lệnh PowerCLI hoặc chính Máy chủ vCenter, và tất cả chúng đến VMkernel thông qua hostd. 

#### Chọn nền tảng cài đặt hệ thống 

- Phần cứng
- Giải pháp lưu trữ
- Giải pháp kết nối (Networking), tích hợp vào hạ tầng mạng hiện có

#### Cài đặt

Các giải pháp cài đặt:

- Thủ công
- Cài đặt bằng tập lệnh script
- Automated provisioning of ESXi