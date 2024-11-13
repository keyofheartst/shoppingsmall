1.Bài toán : Xây dựng ứng dụng mua sắm và phân tích dữ liệu liên quan sử dụng.
2.Giải pháp: 
	Giải pháp tập trung vào việc xây dựng một ứng dụng mua sắm sử dụng kiến trúc 
	(event-driven architecture). Các sự kiện mua sắm được tạo ra và gửi đến Kafka, 
	sau đó được xử lý và lưu trữ trong BigQuery để phân tích dữ liệu.
3.Trình tự thực hiện: 
- Thiết lập Kafka:

	Kafka được sử dụng như một hệ thống truyền tải sự kiện. 
	Các sự kiện mua sắm (shopping events) được gửi đến các chủ đề (topics) trong Kafka.
	Cài đặt và cấu hình Kafka trên máy chủ hoặc sử dụng dịch vụ Kafka được quản lý.
- Tạo Kafka Producer:

	Sử dụng Python để tạo ra các sự kiện mua sắm giả lập và gửi chúng đến Kafka.
	Sử dụng thư viện kafka-python để tạo Kafka Producer.
	Mã giả lập các đơn hàng và gửi chúng đến chủ đề Kafka.
- Xử lý sự kiện với Kafka Consumer:

	Tạo Kafka Consumer để đọc các sự kiện từ Kafka.
	Sử dụng Python và kafka-python để tạo Kafka Consumer.
	Xử lý các sự kiện mua sắm và chuẩn bị dữ liệu để lưu trữ vào BigQuery.
- Lưu trữ dữ liệu vào BigQuery:

	Sử dụng thư viện google-cloud-bigquery để kết nối và lưu trữ dữ liệu vào BigQuery.
	Tạo bảng trong BigQuery để lưu trữ các sự kiện mua sắm.
	Gửi dữ liệu từ Kafka Consumer đến BigQuery.
- Phân tích dữ liệu:

	Sử dụng BigQuery để chạy các truy vấn phân tích trên dữ liệu mua sắm.
	Tạo các báo cáo và trực quan hóa dữ liệu để hiểu rõ hơn về hành vi mua sắm của khách hàng.