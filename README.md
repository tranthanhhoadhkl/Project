# GovBank Analytics 

Phân tích và trực quan dữ liệu giá cổ phiếu các ngân hàng quốc doanh Việt Nam bằng R.


---

##  Giới thiệu
Dự án tập trung vào thăm dò, phân tích và trực quan hóa dữ liệu giá chứng khoán của các ngân hàng quốc doanh Việt Nam gồm:
- **Agribank**
- **BIDV (BID)**
- **VietinBank (CTG)**

Mục tiêu chính:
-  Dự đoán xu hướng thị trường → Giúp nhà đầu tư nhận biết thời điểm mua/bán hợp lý.
-  Đánh giá hiệu suất cổ phiếu → So sánh hiệu suất và mức biến động giữa các ngân hàng.
-  Quản lý rủi ro → Xác định biến động giá để tối ưu hóa chiến lược đầu tư.
-  Quyết định đầu tư → Cung cấp báo cáo trực quan phục vụ nhà đầu tư.

---

##  Các bước thực hiện

### **1. Thu thập dữ liệu**
- Dữ liệu giá cổ phiếu được lấy từ **Yahoo Finance API** hoặc **VNDirect**.
- Dữ liệu được lưu dưới định dạng `.csv` trong thư mục `data/raw/`.

### **2. Tiền xử lý dữ liệu**
- Xử lý giá trị thiếu, chuẩn hóa định dạng ngày.
- Tính toán các chỉ số thống kê cơ bản:
  - Giá trung bình (`mean`)
  - Độ lệch chuẩn (`std`)
  - Độ biến động (`volatility`)

### **3. Phân tích thăm dò dữ liệu (EDA)**
- So sánh biến động giá giữa các ngân hàng.
- Tìm hiểu mối tương quan giữa giá và khối lượng giao dịch.
- Kiểm tra các giá trị ngoại lai.

### **4. Trực quan hóa dữ liệu**
Sử dụng **ggplot2** và **plotly** để tạo biểu đồ:
- Biểu đồ đường → Xu hướng giá cổ phiếu theo thời gian.
- Biểu đồ cột → So sánh khối lượng giao dịch.
- Biểu đồ hộp (boxplot) → Đo lường mức độ ổn định giá.

### **5. Dự đoán xu hướng**
- Xây dựng mô hình dự báo cơ bản dựa trên dữ liệu lịch sử.
- Dự đoán xu hướng tăng/giảm của giá cổ phiếu.

---

##  Công nghệ sử dụng

| Công nghệ | Vai trò |
|----------|-------------------------|
| **R** | Ngôn ngữ chính |
| **tidyverse** | Tiền xử lý dữ liệu |
| **ggplot2** | Trực quan hóa dữ liệu tĩnh |
| **plotly** | Biểu đồ tương tác |
| **lubridate** | Xử lý dữ liệu thời gian |
| **quantmod** | Lấy dữ liệu chứng khoán |
| **rmarkdown** | Sinh báo cáo tự động |

---
