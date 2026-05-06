# IoT-Farm-Scale
IoT Smart Farm Scale: Solar-optimized, automatic Big Data collection, and remote Tare/Calib via MQTT.
📝 Giới thiệu dự án
Dự án tập trung xây dựng hệ thống cân điện tử thông minh ứng dụng trong nông nghiệp công nghệ cao. Thiết bị giải quyết bài toán thu thập dữ liệu khối lượng tự động từ xa, tối ưu hóa năng lượng để hoạt động bền bỉ tại các khu vực canh tác không có nguồn điện lưới.

🎯 Mục tiêu
Tự động hóa: Giảm thiểu công sức đo đạc thủ công, dữ liệu được đẩy trực tiếp lên Cloud.

Hoạt động độc lập: Sử dụng năng lượng mặt trời và chế độ tiết kiệm điện năng để vận hành lâu dài.

Dữ liệu lớn (Big Data): Cung cấp nguồn dữ liệu sạch, chính xác theo chu kỳ để phân tích xu hướng phát triển của nông sản.

🛠 Điểm nhấn kỹ thuật (Key Features)
1. Quản lý năng lượng thông minh
Hybrid Power: Kết hợp pin lithium 2Ah và mạch sạc năng lượng mặt trời (Solar Panel).

Deep Sleep: Tối ưu hóa vi điều khiển ESP8266, chỉ "thức dậy" khi cần đo và gửi dữ liệu.

Peripheral Control: Tự động ngắt nguồn hoàn toàn cho cảm biến HX711 khi không sử dụng để bảo toàn pin.

2. Chế độ vận hành kép (Dual-Mode)
Chế độ liên tục (Continuous): Theo dõi thời gian thực qua Web/App, phù hợp khi cần giám sát biến động nhanh.

Chế độ quãng nghỉ (Interval): Thức dậy mỗi 15 phút một lần trong khung giờ từ 6h00 đến 18h00. Đây là chế độ cốt lõi để thu thập Big Data.

3. Khả năng phục hồi và Ổn định (Reliability)
WiFiManager: Cấu hình mạng dễ dàng qua giao diện Web mà không cần can thiệp vào mã nguồn.

Fail-safe Logic: Tự động đi ngủ sau 10-15 giây nếu không thể kết nối WiFi/MQTT để tránh cạn kiệt pin.

NVS Storage: Lưu trữ các thông số hiệu chuẩn (Calibration/Offset) vào bộ nhớ Flash, đảm bảo độ chính xác ngay cả khi khởi động lại.

4. Hiệu suất truyền tải
Giao thức: MQTT kết hợp với định dạng dữ liệu JSON gọn nhẹ.

Độ trễ thấp: Một chu kỳ hoạt động chỉ mất từ 8 đến 15 giây, cực kỳ tối ưu cho thiết bị IoT chạy pin.

🚀 Định hướng phát triển
Chuyển đổi từ bản mẫu (Prototype) sang mạch in PCB tích hợp hoàn chỉnh (Sử dụng chip dán ESP8266).

Phát triển Dashboard phân tích dữ liệu chuyên sâu để dự báo năng suất dựa trên dữ liệu thu thập được.
