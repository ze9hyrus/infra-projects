#### vSphere Virtual Symmetric Multi-Processing

Cho phép tạo VM với nhiều cpu ảo và socket ảo cũng như nhiều core ảo trên mỗi cpu

#### vSphere vMotion and vSphere Storage vMotion

​	vMotion cho phép di chuyển một máy ảo đang chạy từ physical host này sang physical host khác mà không cần phải tắt máy ảo và k bị mất kết nối mạng của VM

​	Storage vMotion di chuyển bộ nhớ(storage) của máy ảo trong khi máy ảo vẫn đang chạy

#### vSphere Distributed Resource Scheduler

​	Khi khởi động, DRS cố gắng đặt từng máy ảo trên máy chủ phù hợp nhất để chạy máy ảo đó

​	Khi một máy ảo đang chạy, DRS sẽ tìm cách cung cấp cho máy ảo đó phần cứng cần thiết, giảm thiểu mức độ tranh giành các nguồn lực đó, duy trì mức sử dụng cân bằng.

#### vSphere Storage DRS

Tương tự DRS, áp dụng cho storage

#### Storage I/O Control and Network I/O Control

​	Chỉ định mức độ ưu tiên cho I/O Storage  cũng như chỉ định giới hạn I/O Storage  cho máy ảo.

​	Giúp các máy ảo cần quyền truy cập ưu tiên vào tài nguyên lưu trữ nhận được nhiều tài nguyên hơn khi tắc nghẽn hệ thống Storage  

​	Tương tự với Network 

#### vSphere High Availability

Cung cấp một quy trình di chuyển và khởi động lại máy ảo đang chạy trên máy chủ ESXi tại một thời điểm máy chủ tắt hoặc lỗi khác sang một máy chủ mới đủ điều kiện

#### vSphere Fault Tolerance

 vSphere High Availability giúp cho máy ảo tiếp tục hoạt động trên một máy chủ khác nhưng cần phải khởi động lại, vì vậy sẽ có khoảng thời gian ngắt kết nối. 

vSphere Fault Tolerance khắc phục điều này bằng cách tạo và duy trì một bản sao của máy ảo đó trên một máy chủ khác, ngay khi máy ảo chính gặp vấn đề máy ảo bản sao này sẽ thế chỗ và tiếp tục tạo ra một bản sao của nó ở một máy chủ khác. 

> Nó đảm bảo được hầu hết các trường hợp, nhưng sẽ tốn tài nguyên và sẽ không hiệu quả nếu cả máy chủ của máy ảo chính và máy chủ của bản sao gặp lỗi cùng lúc

#### vSphere Storage APIs for Data Protection and VMware Data Protection

Sao lưu, bảo vệ dữ liệu

#### Virtual SAN (vSAN)

Tận dụng bộ nhớ nội bộ được tìm thấy trong các nút máy tính riêng lẻ và chuyển nó thành một Virtual SAN.

Hỗ trợ hệ thống từ 2-64 ESXi

> Hầu hết các node có một lượng ổ đĩa vật lý hạn chế. vSAN gộp chung bộ nhớ trên các node, cho phép bạn tạo một kho dữ liệu trải dài trên nhiều node

#### vSphere Replication

Sap chép dữ liệu, máy ảo từ môi trường vSphere này sang một môi trường vSphere khác, trên cấp độ từng máy ảo nên nó cung cấp quyền kiểm soát rất chi tiết.

#### vSphere Flash Read Cache

Sử dụng bộ nhớ thể rắn (băng thông rất lớn, tuy nhiên giá thành cao) làm bộ nhớ đệm



