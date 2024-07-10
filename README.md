# GPSCal
# Hướng dẫn sử dụng app
# 1. App datn
App Android được sử dụng để thu dữ liệu GNSS. 

Nhấn nút Display, sau đó nhấn nút Start để bắt đầu ghi dữ liệu, Stop để kết thúc. Chú ý đến những nơi thông thoáng để bắt được tín hiệu GNSS. (Nếu app không chạy thì copy code sang một file khác rồi nạp code lại)

File .csv GNSS sau khi ghi xong được lưu trong thư mục Documents của điện thoại. Gửi file đến máy tính để tiếp tục xử lý. Tên file có dạng gnss_YYYY_MM_DD_HH_MM.csv
  
# 2. App MyApplication
App Android được sử dụng để ghi lại dữ liệu GPS lấy từ API có sẵn trong điện thoại. 

Sau khi mở app, chờ một lúc để app định vị được vị trí, nhấn nút View để màn hình di chuyển đến vị trí hiện tại. Start để bắt đầu thu, Stop để kết thúc. 

File .csv GPS sau khi ghi xong được lưu trong thư mục Documents. Gửi file đến máy tính để tiếp tục xử lý. Tên file có dạng ground_truth_YYYY_MM_DD_HH_MM.csv (Dữ liệu này không phải ground truth vì vẫn tồn tại sai số)

Chú ý không dùng điện thoại Samsung để cài app, không biết vì sao nhưng mà app định vị dùng trên máy Samsung toàn bị lỗi. 

# Hướng dẫn sử dụng code
# 1. File get_sat_data.jpynb
Thay path = "Tên file .csv vừa thu được từ điện thoại"

Run code để nhận đầu ra là file .csv có thêm cột Pseudorange và Satellites Position + Velocity. Tên file đầu ra có dạng gnss_YYYY_MM_DD_HH_MM_sat.csv

# 2. File get_position_csv
Thay path = "Tên file .csv vừa thu được từ code trên"

Hoặc path = "Link dẫn tới file device_gnss.csv trong tập data Google"

Run code để nhận đầu ra là file .csv chứa tọa độ được tính bởi hệ thống. Tên file đầu ra có dạng position_data_YYYY_MM_DD_HH_MM_sat.csv

# 3. File calculate_distance
Thay path gnss bằng file tọa độ vừa tính, ground bằng file thu được từ app MyApplication hoặc ground truth trong tập Google. 

Run code, nhận được kết quả là trung bình sai lệch giữa 2 tập tọa độ.





