---
theme: gaia
_class: lead
paginate: true
backgroundImage: url('./assets/images/pxfuel.jpg')
style: |
  @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');
  section {
    font-family: 'Roboto', sans-serif;
  }
marp: true
---

# **Ứng dụng di động Y tế**  

---

## **Giới thiệu chung**  
- **Mục tiêu tổng thể**  
  - Hỗ trợ bệnh viện/trung tâm y tế theo dõi, quản lý và cải thiện sức khỏe  
  - Hợp lý hóa dịch vụ y tế qua kênh số  
  - Cầu nối trực tiếp giữa bệnh nhân và nhà cung cấp dịch vụ y tế  
- **Phạm vi ứng dụng**  
  - Theo dõi sức khỏe cá nhân, lên lịch và quản lý cuộc hẹn khám
  - Đăng ký tiêm chủng, tư vấn y tế từ xa
  - Quản lý hồ sơ sức khỏe điện tử, quản lý thuốc và nhắc nhở

---

## **Các vấn đề tồn tại và nhu cầu**
### 2.1 Từ phía bệnh nhân  
- Khó khăn đặt lịch khám phù hợp, tốn thời gian chờ đợi
- Khó khăn di chuyển đến cơ sở y tế, đặc biệt người cao tuổi
- Thiếu nguồn tư vấn đáng tin cậy cho vấn đề sức khỏe nhỏ
- Quên uống thuốc theo đơn
- Khó quản lý giấy tờ y tế và lịch sử khám bệnh

---

### 2.2 Từ phía bác sĩ  
- Thông tin bệnh nhân hạn chế và khó theo dõi sau điều trị
- Giới hạn của tư vấn từ xa
- Khó truy cập nhanh tiền sử, bệnh lý của bệnh nhân

### 2.3 Từ phía điều dưỡng  
- Gánh nặng công việc giấy tờ, nhập liệu hai lần
- Khó theo dõi bệnh nhân giữa các lần khám

---

### 2.4 Vấn đề chung  
- Hạn chế của công nghệ tư vấn từ xa hiện tại
- AI chưa đủ tin cậy để tự động hóa hoàn toàn
- Khó khăn trong việc hướng dẫn xử lý cấp cứu hiệu quả
- Nguy cơ hệ thống gặp trục trặc, lỗi phần mềm
- Sự chấp nhận của người dùng đối với ứng dụng mới

---

## **Đối tượng người dùng và các bên liên quan**
### 3.1 Đối tượng người dùng chính  
- **Bệnh nhân**
  - Đa dạng trình độ học vấn, kỹ thuật, tuổi >18
- **Bác sĩ**
  - Có bằng y khoa, chứng chỉ hành nghề
  - Kiến thức kỹ thuật trung bình
- **Điều dưỡng**
  - Có bằng/chứng chỉ điều dưỡng
  - Kiến thức kỹ thuật trung bình

---

### 3.2 Các bên liên quan khác  
- Bệnh viện/Trung tâm y tế
- Dịch vụ bảo hiểm y tế
- Cơ quan pháp lý
- Phòng IT bệnh viện
- Dược sĩ
- Quản trị viên hệ thống

---

## **Ma trận chức năng theo vai trò**
<style scoped>
  table {
    width: 100%;
    border-collapse: collapse;
  }
</style>
| Chức năng        | Bệnh nhân | Bác sĩ |
| ---------------- | :-------: | :----: |
| ĐK/SMS           |     ✓     |    ✗   |
| Quản lý vai trò  |     ✓     |    ✗   |
| Hồ sơ cá nhân    |     ✓     |    ✓   |
| Đặt/đổi lịch     |     ✓     |    ✓   |
| Chọn loại cuộc hẹn|     ✓     |    ✓   |
| Tư vấn (video/âm thanh/chat)|     ✓     |    ✓   |

---
<style scoped>
  table {
    width: 100%;
    border-collapse: collapse;
  }
</style>

| Chức năng        | Bệnh nhân | Bác sĩ |
| ---------------- | :-------: | :----: |
| Tìm bác sĩ & UW   |     ✓     |    ✗   |
| Hồ sơ điện tử (EHR)|     ✓     |    ✓   |
| Kê đơn điện tử|     ✗     |    ✓   |
| Đăng tải bài viết sức khỏe|     ✗     |    ✓   |
| Đăng tải bài viết sức khỏe|     ✗     |    ✓   |

---

## **Yêu cầu phi chức năng** 
### 1. Hiệu năng (Performance)
- Thời gian phản hồi cho tương tác người dùng dưới 2 giây.  
- Thời gian phản hồi cho đặt lịch hẹn dưới 5 giây.  

### 2. Tính mở rộng (Scalability)
- Hỗ trợ mở rộng theo chiều ngang để thích ứng với sự tăng trưởng.  

---

### 3. Bảo mật (Security)
- Tuân thủ quy định bảo vệ dữ liệu y tế của Việt Nam (Nghị định 13/2023/NĐ-CP).  
- Triển khai mã hóa đầu cuối cho tất cả dữ liệu bệnh nhân.  
- Đảm bảo quyền riêng tư và an toàn cho thông tin y tế nhạy cảm.  
- Kiểm soát truy cập dựa trên vai trò.  
- Duy trì nhật ký kiểm tra (audit log) cho việc truy cập và sửa đổi dữ liệu.  

---
### 3. Bảo mật (Security)
- Cần có cơ sở dữ liệu đầy đủ về thuốc và tương tác thuốc để hỗ trợ kiểm tra an toàn.  
- Tính năng cảnh báo tình trạng khẩn cấp chỉ dừng ở mức cảnh báo, không hướng dẫn cấp cứu trực tiếp.  
- Tuân thủ các tiêu chuẩn mã hóa công nghiệp (ví dụ: TLS, AES).  
- Tuân thủ ISO 13485, IEC 62304, ISO 14971 cho phần mềm y tế.  

---

### 4. Tính khả dụng (Usability & Accessibility)
#### Usability  
- Giao diện trực quan, điều hướng rõ ràng, bố cục nhất quán.  
- Bệnh nhân mới thành thạo trong vòng 15 phút tự học.  
- Chuyên gia y tế thành thạo trong vòng 90 phút đào tạo.  
- Cung cấp hướng dẫn từng bước, video hướng dẫn, FAQ, hỗ trợ trong ứng dụng.  
- Tài liệu riêng cho bệnh nhân và nhà cung cấp dịch vụ y tế.  

---

#### Accessibility  
- Tuân thủ WCAG 2.1 AA.  
- Hỗ trợ chuyển văn bản thành giọng nói.  
- Tùy chọn độ tương phản cao.  
- Hỗ trợ tiếng Việt (chính) và tùy chọn tiếng Anh.  

---

### 5. Độ tin cậy (Reliability & Availability)
- Duy trì 95% thời gian hoạt động hàng tháng.  
- Các chức năng quan trọng (đặt lịch, nhắc nhở, hồ sơ sức khỏe) có tính sẵn sàng 99%.  
- Sẵn sàng 24/7, có thông báo trước khi bảo trì.  
- Khả năng khôi phục sau sự cố mà không mất dữ liệu.  

---
### 5. Độ tin cậy (Reliability & Availability)
- Sao lưu dữ liệu tự động ít nhất hàng ngày.  
- Thời gian khôi phục tối đa 4 giờ cho các chức năng quan trọng.  
- Đảm bảo độ chính xác và nhất quán của dữ liệu y tế.  
- Hỗ trợ kỹ thuật 24/7 cho nhà cung cấp và trong giờ làm việc cho bệnh nhân.  

---

## **Phân tích cạnh tranh**

- Đã khảo sát các ứng dụng: Long Châu, Pharmacity, eDoctor, UMC Care
- **Điểm mạnh đối thủ**: 
  - Long Châu: tư vấn dược/bán thuốc
  - Pharmacity: công cụ theo dõi sức khỏe
  - eDoctor: khám/xét nghiệm tại nhà
  - UMC Care: liên kết với bệnh viện uy tín

---
### Cơ hội cạnh tranh
- Thiếu tích hợp sâu với hệ thống bệnh viện lớn
- Thiếu tính năng khám chữa bệnh chuyên sâu
- Giới hạn về phạm vi dịch vụ
- Giao diện phức tạp với người lớn tuổi
- Một số ứng dụng chưa có quản lý hồ sơ gia đình

---

<style scoped>
  table {
    width: 100%;
    border-collapse: collapse;
  }
  th{
    padding: 8px;
    text-align: center;
    border-bottom: 1px solid #ddd;
  }

  td{
    padding: 8px;
    font-size: 30px;
  }

  
</style>

## **Ưu tiên và Lộ trình triển khai**


|Ưu tiên cao nhất|Triển khai theo giai đoạn|
|---|---|
|*-* Hệ thống đặt lịch/quản lý lịch khám dễ sử dụng <br> *-* Tư vấn từ xa (chat/video) <br> *-* Hồ sơ khám bệnh chi tiết/toàn diện <br> *-* Quản lý thuốc/nhắc nhở <br> *-* Theo dõi bệnh nhân từ xa |*-* Bắt đầu với chức năng cơ bản/thiết yếu <br> *-* Mở rộng dựa trên phản hồi người dùng|

---

## **Kết luận** 
- Cần ứng dụng hỗ trợ quy trình làm việc của bác sĩ và điều dưỡng
- Cung cấp tính năng tiện lợi cho bệnh nhân
- Tích hợp chặt chẽ với các hệ thống y tế hiện có
- Chú trọng tính chính xác, an toàn, bảo mật dữ liệu
- Nhận thức và giải quyết các hạn chế của công nghệ