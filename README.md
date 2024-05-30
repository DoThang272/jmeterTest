<!-- # jmeterTest
I) Jmeter là gì?
    - Jmeter là công cụ để đo độ tải và performance của đối tượng, có thể sử dụng để test performance trên cả nguồn tĩnh và nguồn động, có thể kiểm tra độ tải và hiệu năng trên nhiều loại server khác nhau như: Web – HTTP, HTTPS, SOAP, Database via JDBC, LDAP, JMS, Mail – SMTP(S), POP3(S) và IMAP(S)…
    - Jmeter là một phần mềm mã nguồn mở được viết bằng java. Cha đẻ của JMeter là Stefano Mazzocchi. Sau đó Apache đã thiết kế lại để cải tiến hơn giao diện đồ họa cho người dùng và khả năng kiểm thử hướng chức năng.

II) Đặc trung của Jmeter
    - Nguồn mở, miễn phí
    - Giao diện đơn giản, trực quan dễ sử dụng
    - Có thể kiểm thử nhiều kiểu server: Web - HTTP, HTTPS, SOAP, Database - JDBC, LDAP, JMS, Mail - POP3,…
    - Một công cụ độc lập có thể chạy trên nhiều nền tảng hệ điều hành khác nhau, trên Linux chỉ cần chạy bằng một shell scrip, trên Windows thì chỉ cần chạy một file .bat
    - Đa luồng, giúp xử lý tạo nhiều request cùng một khoảng thời gian, xử lý các dữ liệu thu được một cách hiệu quả.
    - Đặc tính mở rộng, có rất nhiều plugin được chia trẻ rộng rãi và miễn phí

    * Jmeter Performance Testing bao gồm:
    - Load testing: Mô hình hóa dự kiến sử dụng bởi nhiều người dùng truy cập một dịch vụ website trong cùng thời điểm.
    - Stress testing: Tất cả các web server có thể tải một dung lượng lớn, khi mà tải trọng vượt ra ngoài giới hạn thì web server bắt đầu phản hồi chậm và gây ra lỗi. Mục đích của stress testing là có thể tìm ra độ tải lớn mà web server có thể xử lý.

III) Tạo một Kế hoạch kiểm thử hiệu năng bằng Jmeter
b1: Thêm Thread Group 
    - Click chuột phải vào Test Plan >> Add >> Threads (Users) >> Thread Group
    - Trên cửa sổ Thread Group ta thực hiện nhập Thread properties như sau:
        .) Number of Threads - Số lượng người sử dụng truy cập vào website: 100
        .) Ramp-Up Period: 100
        .) Loop Count - Số thời gian thực hiện kiểm tra: 5

b2: Thêm phần tử Jmeter
    - Click chuột phải vào Thread Group Vietnamnet >> Add >> Config Element >> HTTP Request Defaults
    - Trên cửa sổ HTTP Request Defaults ta nhập: https://phenikaa-uni.edu.vn/vi
    - Click chuột phải vào Thread Group Vietnamnet >> Add >> Sampler >> HTTP Request
    - Trên cửa sổ HTTP Request, trường Path sẽ chỉ ra URL request nào bạn muốn gửi tới máy chủ:
        .) Nếu để trống JMeter sẽ tạo URL request https://phenikaa-uni.edu.vn/vi tới máy chủ
        .) Nếu muốn tạo URL request https://phenikaa-uni.edu.vn/vi thì nhập: vi/page/tin-tuc

b3: thêm graph réult
    - Hiển thị kết quả dưới dạng biểu đồ
    - Click chuột phải vào Thread Group Vietnamnet >> Add >> Listener >> Graph Results

IV) Chạy và lấy kết quả 
    - Click button "Start" hoặc Ctrl + R để chạy
    - Kết quả test được hiển thị trên Graph với thời gian thực tế

V) Phân tích kết quả -->
