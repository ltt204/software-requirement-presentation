
**Dàn ý: Những gì đã xác định được về đề tài và ứng dụng**

1.  **Giới thiệu chung về dự án và ứng dụng**
    *   Tên ứng dụng: Ứng dụng di động Y tế.
    *   Mục tiêu tổng thể: Hỗ trợ bệnh viện/trung tâm y tế theo dõi, quản lý và cải thiện sức khỏe người dùng tại Việt Nam. Hợp lý hóa dịch vụ y tế qua kênh số, cải thiện giao tiếp bệnh nhân-bác sĩ, nâng cao trải nghiệm chăm sóc sức khỏe. Đóng vai trò là cầu nối trực tiếp giữa bệnh nhân và nhà cung cấp dịch vụ y tế mà không cần đến trung tâm y tế.
    *   Phạm vi ứng dụng (các tính năng chính ban đầu được xác định trong phạm vi): Theo dõi sức khỏe cá nhân, lên lịch và quản lý cuộc hẹn khám, đăng ký tiêm chủng, tư vấn y tế từ xa, truy cập và quản lý hồ sơ sức khỏe điện tử, quản lý thuốc và nhắc nhở sử dụng, xác minh và tích hợp bảo hiểm.
    *   Đối tượng mục tiêu của tài liệu SRS: Thành viên đội phát triển, các bên liên quan (bệnh viện, phòng khám, nhà cung cấp y tế), đội ngũ đảm bảo chất lượng, quản lý dự án.

2.  **Các vấn đề tồn tại và nhu cầu từ các bên liên quan (Rationale - Lý do tồn tại)**
    *   **Từ phía bệnh nhân:**
        *   Khó khăn trong việc đặt lịch khám phù hợp với thời gian cá nhân (hệ thống hiện tại gây khó khăn, tốn thời gian chờ đợi).
        *   Tốn thời gian và khó khăn khi di chuyển đến cơ sở y tế, đặc biệt là người cao tuổi.
        *   Không biết tìm kiếm lời khuyên y tế đáng tin cậy cho các vấn đề sức khỏe nhỏ ở đâu (kênh tư vấn trực tiếp hạn chế, thông tin trên internet thiếu tin cậy).
        *   Hay quên uống thuốc theo đơn, đặc biệt là người cao tuổi.
        *   Khó khăn trong việc quản lý giấy tờ y tế và lịch sử khám bệnh (không có hệ thống lưu trữ tập trung, phải tự quản lý hồ sơ giấy).
        *   Cần giao diện đơn giản, dễ sử dụng, phù hợp với nhiều trình độ công nghệ và lứa tuổi.
    *   **Từ phía bác sĩ:**
        *   Thông tin bệnh nhân hạn chế và khó theo dõi sau điều trị.
        *   Giới hạn của tư vấn từ xa (không thể khám thực thể đầy đủ, hạn chế kê đơn một số loại thuốc).
        *   Cần truy cập nhanh tiền sử, bệnh lý của bệnh nhân để chẩn đoán nhanh và chính xác từ xa.
    *   **Từ phía điều dưỡng:**
        *   Gánh nặng công việc giấy tờ (ghi chép thủ công, nhập liệu hai lần giấy và máy tính) gây mệt mỏi, căng thẳng và tiềm ẩn sai sót/mất dữ liệu.
        *   Khó theo dõi bệnh nhân giữa các lần khám, đặc biệt là bệnh nhân mắc bệnh mãn tính.
    *   **Những vấn đề chung được xác định:**
        *   Hạn chế của công nghệ tư vấn từ xa hiện tại.
        *   AI chưa đủ tin cậy để tự động hóa hoàn toàn việc ghi chép hay hỗ trợ chẩn đoán.
        *   Khó khăn trong việc hướng dẫn xử lý cấp cứu hiệu quả qua ứng dụng.
        *   Nguy cơ hệ thống gặp trục trặc, lỗi phần mềm, quá tải dữ liệu.
        *   Sự chấp nhận của người dùng đối với ứng dụng mới.

3.  **Đối tượng người dùng và các bên liên quan**
    *   **Đối tượng người dùng chính:** Bệnh nhân (đa dạng trình độ học vấn, kỹ thuật, tuổi >18), Bác sĩ (có bằng y khoa, chứng chỉ hành nghề, kiến thức kỹ thuật trung bình), Điều dưỡng (có bằng/chứng chỉ điều dưỡng, kiến thức kỹ thuật trung bình).
    *   **Các bên liên quan khác:** Bệnh viện/Trung tâm y tế, Dịch vụ bảo hiểm y tế, Cơ quan pháp lý, Phòng IT bệnh viện, Dược sĩ, Quản trị viên hệ thống.
    *   **Trình độ CNTT:** Rất khác nhau giữa các nhóm đối tượng. Bệnh nhân cao tuổi cần hướng dẫn ban đầu. Nhân viên y tế cần hướng dẫn chi tiết hơn về các tính năng chuyên biệt.

4.  ~~**Các yêu cầu chức năng (Functional Requirements - FR) đã xác định**~~

| Actor              | ĐK/SMS | Quản lý vai trò | Hồ sơ cá nhân & gia đình | Tìm bác sĩ & UW | Đặt/đổi/hủy lịch | Chọn loại cuộc hẹn | Tư vấn (video/âm thanh/chat) | Upload kết quả XN | Hồ sơ điện tử (EHR) | Kê đơn điện tử | Nhắc thuốc & tiêm chủng | Kiểm tra tương tác | Tin nhắn bảo mật | Thông báo & Alert | Thanh toán & BHYT | Audit log | Báo cáo thống kê |
| ------------------ | :----: | :-------------: | :----------------------: | :-------------: | :--------------: | :----------------: | :--------------------------: | :---------------: | :-----------------: | :------------: | :---------------------: | :----------------: | :--------------: | :---------------: | :---------------: | :-------: | :--------------: |
| **Bệnh nhân**      |    ✓   |        ✓        |             ✓            |        ✓        |         ✓        |          ✓         |               ✓              |         ✓         |          ✓          |        ✗       |            ✓            |          ✗         |         ✓        |         ✓         |         ✓         |     ✗     |         ✗        |
| **Bác sĩ**         |    ✗   |        ✗        |             ✓            |        ✓        |         ✓        |          ✓         |               ✓              |         ✗         |          ✓          |        ✓       |            ✗            |          ✓         |         ✗        |         ✓         |         ✗         |     ✗     |         ✓        |
| **Điề  ✗        |         ✗        |          ✗         |               ✗              |         ✗         |          ✓          |        ✗       |            ✓            |          ✗         |         ✗        |         ✓         |         ✗         |     ✗     |         ✓        |
| **Admin/Hệ thống** |    ✗   |        ✓        |             ✗            |        ✗        |         ✗        |          ✗         |               ✗              |         ✗         |          ✗          |        ✗       |            ✗            |          ✗         |         ✗        |         ✓         |         ✓         |     ✓     |         ✓        |


5.  **Các yêu cầu phi chức năng (Non-Functional Requirements - NFR) và Ràng buộc đã xác định**
    *   **Bảo mật và An toàn:**
        *   Tuân thủ quy định bảo vệ dữ liệu y tế của Việt Nam (bao gồm Nghị định 13/2023/NĐCP).
        *   Triển khai mã hóa đầu cuối cho tất cả dữ liệu bệnh nhân.
        *   Đảm bảo quyền riêng tư và an toàn cho thông tin y tế nhạy cảm.
        *   Kiểm soát truy cập dựa trên vai trò.
        *   Duy trì nhật ký kiểm tra (audit log) cho việc truy cập và sửa đổi dữ liệu.
        *   Cần có cơ sở dữ liệu đầy đủ về thuốc và tương tác thuốc để hỗ trợ kiểm tra tương tác an toàn.
        *   Tính năng cảnh báo tình trạng khẩn cấp chỉ nên dừng ở mức cảnh báo, không cố gắng hướng dẫn cấp cứu trực tiếp.
    *   **Độ tin cậy:**
        *   Duy trì **95% thời gian hoạt động hàng tháng**.
        *   Sẵn có 24/7 với thời gian bảo trì được thông báo trước.
        *   Các chức năng quan trọng (đặt lịch, nhắc nhở, hồ sơ sức khỏe) có tính sẵn có **99%**.
        *   Khả năng khôi phục hoạt động bình thường sau sự cố mà không mất dữ liệu.
        *   Sao lưu dữ liệu tự động ít nhất hàng ngày.
        *   Thời gian khôi phục tối đa là 4 giờ cho các chức năng quan trọng.
        *   Đảm bảo **độ chính xác và nhất quán của dữ liệu** y tế.
    *   **Khả năng sử dụng (Usability):**
        *   Giao diện người dùng trực quan, điều hướng rõ ràng, bố cục nhất quán.
        *   Bệnh nhân mới thành thạo trong vòng **15 phút tự học**.
        *   Chuyên gia y tế thành thạo trong vòng **90 phút đào tạo**.
        *   Cung cấp hướng dẫn từng bước, video hướng dẫn, FAQ, hỗ trợ trong ứng dụng.
        *   Tài liệu riêng cho bệnh nhân và nhà cung cấp dịch vụ y tế.
    *   **Khả năng tiếp cận (Accessibility):**
        *   Tuân thủ hướng dẫn về khả năng tiếp cận (WCAG 2.1 AA).
        *   Hỗ trợ chức năng chuyển văn bản thành giọng nói.
        *   Cung cấp tùy chọn độ tương phản cao.
        *   Hỗ trợ tiếng Việt là ngôn ngữ chính, có tùy chọn tiếng Anh.
    *   **Môi trường hoạt động:**
        *   Hoạt động trên thiết bị có kết nối internet hạn chế và có khả năng ngoại tuyến thích hợp.
        *   Hỗ trợ Android 9.0+ và iOS 12.0+.
    *   **Hiệu suất:**
        *   Thời gian phản hồi cho tương tác người dùng dưới 2 giây.
        *   Thời gian phản hồi cho đặt lịch hẹn dưới 5 giây.
        *   Hỗ trợ mở rộng theo chiều ngang để thích ứng với sự tăng trưởng.
    *   **Khả năng hỗ trợ kỹ thuật:**
        *   Hỗ trợ kỹ thuật 24/7 cho nhà cung cấp dịch vụ y tế và trong giờ làm việc cho bệnh nhân.
        *   Cơ sở kiến thức và hỗ trợ khắc phục sự cố từ xa (chia sẻ màn hình).
    *   **Yêu cầu về tích hợp:**
        *   Tích hợp với Hệ thống Hồ sơ Bệnh án Điện tử (EMR/EHR).
        *   Tích hợp với Nhà thuốc/Đơn vị Dược.
        *   Tích hợp với Cơ sở dữ liệu Thuốc.
        *   Có tiềm năng tích hợp với Hệ thống Bảo hiểm Y tế.
        *   Tích hợp với Nguồn kiến thức Y tế.
        *   Tích hợp với hệ thống quản lý bệnh viện.
        *   Sử dụng dịch vụ bên thứ ba cho gọi video, thanh toán, SMS, bản đồ, thư viện mã hóa.
    *   **Tiêu chuẩn áp dụng:**
        *   Tuân thủ các tiêu chuẩn mã hóa công nghiệp.
        *   Tuân thủ ISO 13485, IEC 62304, ISO 14971 cho phần mềm y tế.

6.  **Phân tích cạnh tranh (Những gì đã xác định được về thị trường)**
    *   Đã khảo sát và phân tích các ứng dụng cùng ngành như Long Châu, Pharmacity, eDoctor, UMC Care.
    *   Các ứng dụng hiện tại có điểm mạnh riêng (vd: Long Châu mạnh về tư vấn dược/bán thuốc, Pharmacity có công cụ theo dõi sức khỏe, eDoctor có khám/xét nghiệm tại nhà, UMC Care liên kết chặt với một bệnh viện uy tín).
    *   Các điểm yếu/khoảng trống được xác định:
        *   Thiếu tích hợp sâu với hệ thống bệnh viện lớn và hồ sơ bệnh án quốc gia.
        *   Thiếu tính năng khám chữa bệnh chuyên sâu hoặc chỉ tập trung vào thủ tục hành chính.
        *   Giới hạn về phạm vi dịch vụ (vd: khám tại nhà chỉ ở một số thành phố).
        *   Giao diện đôi khi còn phức tạp hoặc nhiều chữ gây khó khăn cho người lớn tuổi.
        *   Một số ứng dụng chưa có tính năng quản lý hồ sơ gia đình.
    *   Thị trường ứng dụng y tế tại Việt Nam đang phát triển mạnh.
    *   Số lượng người dùng tiềm năng đông đảo (người bận rộn, người cao tuổi, người chăm sóc, bệnh nhân mãn tính, chuyên viên y tế).

7.  **Ưu tiên và Lộ trình triển khai ban đầu**
    *   **Ưu tiên cao nhất:** Hệ thống đặt lịch/quản lý lịch khám dễ sử dụng, linh hoạt; tư vấn từ xa (chat/video); hồ sơ khám bệnh chi tiết/toàn diện; quản lý thuốc/nhắc nhở; theo dõi bệnh nhân từ xa.
    *   **Ưu tiên thấp:** Chẩn đoán hỗ trợ bởi AI (chưa cần thiết và rủi ro).
    *   Việc triển khai cần theo từng giai đoạn, bắt đầu với các chức năng cơ bản/thiết yếu, sau đó mở rộng dựa trên phản hồi người dùng.

8.  **Kết luận các vấn đề và nhu cầu chính**
    *   Cần một ứng dụng hỗ trợ quy trình làm việc của bác sĩ và điều dưỡng (truy cập hồ sơ, kê đơn, theo dõi từ xa).
    *   Cung cấp các tính năng tiện lợi cho bệnh nhân (đặt lịch, nhắc nhở, quản lý hồ sơ gia đình, kiến thức y tế).
    *   Yêu cầu tích hợp chặt chẽ với các hệ thống y tế hiện có (EMR, nhà thuốc).
    *   Phải đặc biệt chú trọng tính chính xác, an toàn, bảo mật dữ liệu và độ ổn định của hệ thống.
    *   Cần nhận thức và giải quyết các hạn chế của công nghệ và rào cản quy trình làm việc hiện tại.
