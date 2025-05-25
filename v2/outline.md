**Tóm tắt**

Dự án MediSync nhằm phát triển một ứng dụng di động y tế để hỗ trợ các bệnh viện/trung tâm y tế tại Việt Nam trong việc theo dõi, quản lý sức khỏe người dùng, đồng thời kết nối bệnh nhân với bác sĩ, giảm thiểu thời gian di chuyển và chờ đợi. Ứng dụng này được thiết kế để giải quyết các vấn đề như khó khăn khi đặt lịch khám, hạn chế tiếp cận thông tin y tế đáng tin cậy, gánh nặng công việc giấy tờ cho nhân viên y tế, và những giới hạn của việc tư vấn y tế từ xa. Đối tượng sử dụng bao gồm bệnh nhân (mọi lứa tuổi, trình độ công nghệ đa dạng), bác sĩ, điều dưỡng, ban quản lý bệnh viện, cơ quan pháp lý và dịch vụ bảo hiểm.

Các tính năng chính dự kiến của ứng dụng tập trung vào việc số hóa và tối ưu hóa quy trình chăm sóc sức khỏe, bao gồm quản lý hồ sơ sức khỏe điện tử, đặt lịch hẹn linh hoạt, tư vấn từ xa (chat/video), quản lý thuốc và nhắc nhở, theo dõi chỉ số sức khỏe, và quản lý tiêm chủng. Ứng dụng cần tích hợp với các hệ thống y tế hiện có như EMR/EHR, nhà thuốc, và cơ sở dữ liệu thuốc. Đặc biệt, tính dễ sử dụng (đặc biệt cho người cao tuổi), tính bảo mật dữ liệu, độ chính xác và sự ổn định của hệ thống là những yêu cầu chất lượng được nhấn mạnh. Phân tích các ứng dụng y tế cạnh tranh tại Việt Nam (Long Châu, Pharmacity, eDoctor, UMC Care, JioHealth) cho thấy các tính năng cốt lõi như đặt lịch, tư vấn, hồ sơ sức khỏe và mua thuốc là phổ biến, nhưng việc tích hợp với hệ thống y tế quốc gia và giao diện thân thiện cho người cao tuổi còn là điểm yếu chung. Dự án nhận định rằng việc áp dụng AI cho chẩn đoán chưa phải là ưu tiên cao do lo ngại về độ chính xác và rủi ro. Mô hình kinh doanh dự kiến có thể là freemium, với phiên bản cơ bản miễn phí cho bệnh nhân và các tính năng nâng cao trả phí.

**Dàn ý**

# **Phase 1:**

Dựa trên thông tin từ các nguồn, đây là dàn ý chi tiết về dự án và kế hoạch liên quan:

## **I. Tổng quan dự án (Vision & Scope)**
*   **Mục đích dự án:** Phát triển ứng dụng di động Y tế (MediSync) hỗ trợ bệnh viện/trung tâm y tế theo dõi, quản lý sức khỏe người dùng, kết nối bệnh nhân-bác sĩ, giảm thời gian chờ đợi.
*   **Phạm vi:** Ứng dụng di động cho bệnh viện/trung tâm y tế tại Việt Nam.
    *   Tính năng chính: Theo dõi sức khỏe, đặt/quản lý lịch hẹn, đăng ký tiêm chủng, tư vấn từ xa, truy cập/quản lý hồ sơ sức khỏe điện tử, quản lý thuốc/nhắc nhở, xác minh/tích hợp bảo hiểm.
*   **Phát biểu định vị sản phẩm:** Là nền tảng di động đóng vai trò cầu nối trực tiếp giữa bệnh nhân và nhà cung cấp dịch vụ y tế tại bệnh viện/trung tâm y tế cụ thể.
*   **Đối tượng người dùng/Stakeholders:** Bệnh nhân, Bác sĩ, Điều dưỡng, Ban quản lý bệnh viện, Cơ quan quản lý, Dịch vụ bảo hiểm, Phòng IT.

## **II. Kế hoạch thu thập yêu cầu (Requirement Elicitation Plan)**
*   **Các kỹ thuật:** Phỏng vấn, Khảo sát (form), Nghiên cứu tài liệu, Phân tích ứng dụng tương tự.
*   **Nguồn thông tin:** Bác sĩ, Điều dưỡng/y tá, Bệnh nhân, Dịch vụ bảo hiểm, Cơ quan pháp lý, Bệnh viện, Các ứng dụng cùng ngành.
*   **Kết quả mong đợi:** Biên bản phỏng vấn, dữ liệu khảo sát, tài liệu pháp lý, biên bản họp bệnh viện, tài liệu tổng hợp/so sánh ứng dụng.
*   **Tình trạng tiếp cận:** Đã thực hiện (Bác sĩ, Điều dưỡng, Bệnh nhân, Ứng dụng cùng ngành), Chưa tiếp cận (Dịch vụ bảo hiểm, Bệnh viện).
*   **Lịch trình công việc:**
    *   Phân tích ứng dụng tương tự (1/4 - 5/4).
    *   Phỏng vấn Bác sĩ, Điều dưỡng (11/3 - 19/3).
    *   Thu thập/Phân tích quy trình khám bệnh (17/3 - 4/4).
    *   Khảo sát bệnh nhân (20/3 - 26/3).
    *   Nghiên cứu pháp lý (24/3 - 29/3).
    *   Phỏng vấn dịch vụ bảo hiểm (24/3 - 26/3).
    *   Tổng hợp dữ liệu, xây dựng vision & scope (28/3 - 6/4).

## **III. Tổng hợp và Phân tích yêu cầu (Requirement Analysis & Synthesis)**
*   **Trọng tâm phân tích:** Quy trình làm việc lâm sàng, Tính năng ưu tiên, Yêu cầu tích hợp, An toàn & Bảo mật, Rào cản triển khai.
*   **Quy trình làm việc lâm sàng:**
    *   Điều dưỡng: Hỗ trợ bác sĩ, hành chính, hỗ trợ bệnh nhân, thủ thuật, theo dõi tái khám, ghi chép hồ sơ (giấy & điện tử). Gánh nặng công việc giấy tờ gây mệt mỏi, sai sót.
    *   Bác sĩ (khám từ xa): Hạn chế khám thực thể (hỏi, nhìn, nghe), khó chẩn đoán cuối cùng, hạn chế kê đơn thuốc. Mục tiêu chính: Đánh giá cấp cứu, tư vấn nhập viện. Cần truy cập nhanh tiền sử bệnh nhân.
*   **Tính năng ưu tiên:**
    *   Bác sĩ: Hồ sơ bệnh án điện tử ("rất cần thiết"), Kê đơn điện tử & giao thuốc ("tiện ích rất lớn", "cần phải có"), Hỗ trợ kiểm tra tương tác thuốc ("rất hữu ích"), Đánh giá tình trạng khẩn cấp (cảnh báo). AI hỗ trợ chẩn đoán/ghi chép chưa cần thiết do lo ngại độ chính xác.
    *   Điều dưỡng & Bệnh nhân: Theo dõi sức khỏe từ xa ("rất cần thiết"), Đặt lịch khám từ xa ("thuận tiện"), Nhắc nhở tự động (tái khám, tiêm chủng, thuốc), Quản lý hồ sơ sức khỏe gia đình ("chắc chắn" cần), Tự động hóa hồ sơ (giảm nhập liệu thủ công).
    *   Bệnh nhân: Cung cấp kiến thức y tế cá nhân hóa ("rất hợp lý").
*   **Yêu cầu tích hợp:** Hệ thống EMR/EHR, Nhà thuốc/Đơn vị Dược, Cơ sở dữ liệu Thuốc, Hệ thống Bảo hiểm Y tế (tiềm năng), Nguồn kiến thức Y tế.
*   **An toàn và Bảo mật:** Bảo mật dữ liệu bệnh nhân, Độ chính xác dữ liệu (tránh sai sót từ AI/nhập liệu), Hạn chế chẩn đoán từ xa, An toàn kê đơn (kiểm tra tương tác), Xử lý cấp cứu (chỉ cảnh báo), Độ ổn định hệ thống.
*   **Rào cản triển khai:** Quy trình làm việc hiện tại (giấy & điện tử), Hạn chế công nghệ (khám thực thể, AI, hướng dẫn cấp cứu), Vấn đề kỹ thuật (trục trặc, lỗi, quá tải), Sự chấp nhận của người dùng.
*   **Ưu tiên cao nhất từ phân tích viên:** Hệ thống đặt lịch dễ dùng, linh hoạt; Tư vấn từ xa (chat/video) cho vấn đề đơn giản; Lịch sử khám bệnh chi tiết (EMR); Hệ thống nhắc nhở uống thuốc/tái khám.

## **IV. Đặc tả yêu cầu phần mềm (SRS)**
*   **Danh sách features:**
    *   Quản lý người dùng: Tài khoản, hồ sơ, hồ sơ gia đình, khôi phục mật khẩu, kiểm soát truy cập.
    *   Đặt lịch hẹn khám: Tìm kiếm bác sĩ, hiển thị thời gian thực, đặt/đổi/hủy, nhắc nhở, thông báo cho bác sĩ, quản lý lịch khám của cơ sở y tế, hỗ trợ nhiều hình thức khám.
    *   Quản lý hồ sơ sức khỏe: EMR tập trung, truy cập được ủy quyền, tải tài liệu/hình ảnh, xem theo thời gian, đồng bộ dữ liệu, chia sẻ hồ sơ.
    *   Tư vấn y tế: Video/thoại, nhắn tin an toàn, ghi chép, chia sẻ file, lên lịch.
    *   Quản lý thuốc: Nhắc nhở uống thuốc, thông tin thuốc, kiểm tra tương tác, kê đơn điện tử.
    *   Hệ thống liên lạc: Nhắn tin an toàn giữa các bên, thông báo thời gian thực, lịch sử giao tiếp, khuyến nghị sức khỏe cá nhân hóa.
    *   Quản lý tiêm chủng: Đặt lịch, hồ sơ tiêm chủng, nhắc nhở, thông tin vắc-xin.
    *   Theo dõi sức khỏe: Ghi chỉ số, nhắc nhở thuốc, hiển thị xu hướng, thông tin gia đình, thiết lập mục tiêu.
*   **Yêu cầu phi chức năng:**
    *   Khả dụng: Giao diện trực quan, tiếp cận (WCAG 2.1 AA, text-to-speech, tương phản cao, offline), làm quen (bệnh nhân < 15 phút, chuyên gia < 90 phút).
    *   Độ tin cậy: Sẵn có (95% tổng thể, 99% chức năng quan trọng), Toàn vẹn dữ liệu (xác thực, quản lý giao dịch, lịch sử chỉnh sửa), Sao lưu & phục hồi (hàng ngày, phục hồi < 4 giờ cho chức năng quan trọng).
    *   Hiệu suất: Thời gian phản hồi (<2 giây tương tác, <3 giây tải hồ sơ, <5 giây đặt lịch, <10 giây video), Khả năng chịu tải (ít nhất 1.000 người dùng đồng thời, xử lý cao điểm).
    *   Khả năng hỗ trợ kỹ thuật: Bảo trì (module, logging, giám sát), Hỗ trợ (24/7 cho nhà cung cấp, giờ hành chính cho bệnh nhân, cơ sở kiến thức, chia sẻ màn hình).
*   **Ràng buộc thiết kế:** Nền tảng (Android/iOS, web), Phần cứng (thiết bị di động, máy quét QR/mã vạch, GPS), Giao diện phần mềm (tích hợp hệ thống bệnh viện, cơ sở dữ liệu quốc gia - EMR, bảo hiểm, xét nghiệm, hình ảnh y tế, tiêm chủng, định dạng HL7, FHIR, PDF), Giao thức (TLS 1.2+, HTTPS). Tuân thủ quy định bảo vệ dữ liệu y tế Việt Nam.
*   **Các yêu cầu khác:** Giấy phép (mã nguồn mở, API, EULA), Pháp lý/Bản quyền (thông báo, chính sách bảo mật), Tài liệu hướng dẫn/Hỗ trợ trực tuyến (hướng dẫn chi tiết, video, FAQ, gợi ý UI).

**V. Phân tích đối thủ cạnh tranh (Competition Analysis)**
*   **Các ứng dụng được phân tích:** Long Châu, Pharmacity, eDoctor, UMC Care, JioHealth.
*   **Điểm mạnh chung:** Mua thuốc online, tư vấn trực tuyến, quản lý hồ sơ sức khỏe, đặt lịch khám trực tuyến.
*   **Điểm yếu chung:** Chưa liên kết sâu với hệ thống y tế quốc gia/bệnh viện, giao diện đôi khi phức tạp cho người cao tuổi, hạn chế phạm vi dịch vụ (JioHealth), tập trung hành chính thay vì y tế chuyên sâu (UMC Care), thiếu thông tin thuốc (eDoctor), thiếu hồ sơ gia đình (JioHealth).
*   **Bài học rút ra:** Giao diện đơn giản, dễ sử dụng rất quan trọng. Mô hình freemium được ưa chuộng.

# **Phase 2: Modeling**

## **I. Mô tả các hoạt động chính của hệ thống MediSync (theo Activity Diagram)**

Phần này mô tả luồng hoạt động được thể hiện trong Activity Diagram, liệt kê các hành động chính và tài liệu liên quan đến chúng:

*   **Bệnh nhân yêu cầu tư vấn từ xa:** Vision Document và Requirement Analysis – 2.2 Tính năng ưu tiên.
*   **Hệ thống đặt lịch và gửi thông báo:** SRS – 3.1.2 Đặt lịch hẹn khám.
*   **Bệnh nhân tham gia cuộc gọi tư vấn:** SRS – 3.1.4 Tư vấn y tế.
*   **Bác sĩ tham gia cuộc gọi tư vấn:** SRS – 3.1.4 Tư vấn y tế.
*   **Xem hồ sơ sức khỏe bệnh nhân:** SRS – 3.1.3 Quản lý hồ sơ sức khỏe.
*   **Tiến hành tư vấn và chẩn đoán:** Requirement Analysis – 2.1 Quy trình làm việc lâm sàng.
*   **Hệ thống ghi lại phiên tư vấn:** SRS – 3.1.4 Tư vấn y tế.
*   **Yêu cầu khám trực tiếp (nếu cần):** Requirement Analysis – 2.1 Hạn chế khám từ xa.
*   **Bệnh viện nhận yêu cầu và sắp xếp bác sĩ chuyên khoa:** SRS – 3.1.2 Đặt lịch hẹn khám.
*   **Bệnh nhân đặt lịch khám trực tiếp:** SRS – 3.1.2 Đặt lịch hẹn khám.
*   **Hệ thống gửi xác nhận lịch khám:** SRS – 3.1.6 Hệ thống liên lạc.
*   **Kê đơn thuốc (nếu cần):** SRS – 3.1.5 Quản lý thuốc.
*   **Hệ thống kiểm tra tương tác thuốc và dị ứng:** SRS – 3.1.5 Quản lý thuốc.
*   **Tạo đơn thuốc điện tử:** SRS – 3.1.5 Quản lý thuốc.
*   **Chọn giao thuốc tận nhà hoặc tự mua thuốc:** Requirement Analysis – 2.3 Tích hợp nhà thuốc.
*   **Đặt lịch tái khám (nếu cần):** SRS – 3.1.2 Đặt lịch hẹn khám.
*   **Hệ thống gửi nhắc lịch tái khám:** SRS – 3.1.6 Hệ thống liên lạc.
*   **Kết thúc tư vấn:**
*   **Ghi chú tư vấn và lưu hồ sơ:**
## **II. Yêu cầu hệ thống (theo Requirement Traceability Matrix - RTM)**

Tài liệu RTM liệt kê và phân loại các yêu cầu của dự án.

*   **Danh sách Yêu cầu Chức năng (Functional Requirements - FRs):** Mô tả các tính năng mà hệ thống phải thực hiện.
    *   Ví dụ: **FR-01** Đăng ký người dùng, **FR-02** Xác minh danh tính người dùng, **FR-03** Quản lý vai trò người dùng, **FR-06** Quản lý hồ sơ người dùng (kết quả khám, tài liệu, tiền sử bệnh, dị ứng, thuốc), **FR-07** Tìm kiếm bác sĩ, **FR-09** Lên lịch khám bệnh, **FR-13** Thông báo cho chuyên gia y tế về cuộc hẹn mới, **FR-14** Hỗ trợ nhiều loại cuộc hẹn (trực tiếp, tại nhà, tư vấn trực tuyến), **FR-15** Truy cập hồ sơ bác sĩ (được ủy quyền), **FR-16** Tải lên tài liệu y tế, **FR-22** Tư vấn video và âm thanh, **FR-25** Tạo đơn thuốc điện tử, **FR-26** Kiểm tra tương tác thuốc, **FR-30** Giao tiếp giữa bệnh nhân và chuyên gia y tế, **FR-34** Tài liệu bàn giao ca làm việc (cho y tá), **FR-35** Đặt lịch tiêm chủng, **FR-36** Quản lý hồ sơ tiêm chủng, **FR-39** Ghi nhận chỉ số sức khỏe.
*   **Danh sách Yêu cầu Phi chức năng (Non-Functional Requirements - NFRs):** Mô tả cách hệ thống hoạt động.
    *   Ví dụ: **NFR-01** Điều hướng rõ ràng, **NFR-03** Hỗ trợ đa ngôn ngữ (Tiếng Việt là chính, Tiếng Anh là lựa chọn), **NFR-04** Khả năng hoạt động trong điều kiện internet không tốt, **NFR-05** Sẵn sàng hoạt động 24/7, **NFR-07** Đảm bảo độ chính xác và nhất quán dữ liệu, **NFR-09** Tự động sao lưu dữ liệu hàng ngày, **NFR-11** Hỗ trợ ít nhất 1.000 người dùng đồng thời, **NFR-12** Xử lý tải cao vào giờ cao điểm, **NFR-13** Quản lý ít nhất 100.000 hồ sơ bệnh nhân, **NFR-14** Xử lý đồng thời 500 cuộc tư vấn video, **NFR-15** Hỗ trợ mở rộng theo chiều ngang, **NFR-16** Tuân thủ tiêu chuẩn mã hóa, **NFR-19** Hỗ trợ đa nền tảng (Android, iOS, web), **NFR-21** Tuân thủ quy định Việt Nam về bảo mật y tế, **NFR-22** Tích hợp hệ thống quản lý bệnh viện qua API chuẩn hóa, **NFR-23** Tích hợp cơ sở dữ liệu BHYT quốc gia, **NFR-24** Tích hợp hệ thống xét nghiệm và chẩn đoán hình ảnh, **NFR-25** Tích hợp cơ sở dữ liệu tiêm chủng quốc gia, **NFR-26** Tuân thủ tiêu chuẩn HL7 FHIR, **NFR-27** Tuân thủ tiêu chuẩn DICOM (cho hình ảnh y tế), **NFR-28** Tuân thủ tiêu chuẩn PCI DSS (cho thanh toán), **NFR-29** Tuân thủ GDPR (bảo vệ dữ liệu), **NFR-30** Khả năng theo dõi và báo cáo, **NFR-31** Hỗ trợ kiểm soát phiên bản.

## **IV. Giao diện người dùng (theo RTM)**

RTM cũng liệt kê các màn hình giao diện có thể xuất hiện trong ứng dụng.

*   **Giao diện Bệnh nhân:**
    *   Bao gồm các màn hình như Đăng nhập/Đăng ký (P1), Trang chủ (P2), Quản lý hồ sơ cá nhân (P3) và gia đình (P4), Đặt lịch hẹn (P5), Theo dõi sức khỏe (P6), Quản lý thuốc (P7), Quản lý tiêm chủng (P8), Tư vấn từ xa (P9), Hồ sơ y tế (P10), Nhắn tin (P11), và Giáo dục sức khỏe (P12).
*   **Giao diện Chuyên gia y tế:**
    *   Bao gồm các màn hình như Đăng nhập (H1), Bảng điều khiển (H2), Danh sách bệnh nhân (H3), Hồ sơ bệnh nhân (H4), Quản lý lịch hẹn (H5), Giao diện tư vấn từ xa (H6), Đơn thuốc điện tử (H7), Trung tâm nhắn tin (H8), Bàn giao ca (H9), và Quản lý khám tại nhà (H10).
*   **Giao diện Admin hệ thống:**
    *   Bao gồm các màn hình như Bảng điều khiển quản trị (A1), Quản lý người dùng (A2), Cấu hình hệ thống (A3), Phân tích & Báo cáo (A4), Quản lý nội dung (A5), và Quản lý hỗ trợ kỹ thuật (A6).
*   **Ma trận liên kết Yêu cầu và Màn hình:** Tài liệu cung cấp ma trận chi tiết thể hiện yêu cầu chức năng và phi chức năng được hỗ trợ bởi màn hình nào. Ví dụ, yêu cầu **FR-06** Quản lý hồ sơ người dùng liên quan đến màn hình P3 (Hồ sơ cá nhân bệnh nhân) và H4 (Hồ sơ bệnh nhân của chuyên gia y tế). Yêu cầu **NFR-01** Điều hướng rõ ràng áp dụng cho tất cả các màn hình từ P1-P12, H1-H10 và A1-A6.

**V. Đặc tả các Use Case chính (theo Use-Case Specification)**

Tài liệu này mô tả chi tiết từng trường hợp sử dụng (Use Case), bao gồm ID, tên, mô tả, tác nhân, điều kiện tiên quyết, luồng chính, luồng thay thế và điều kiện sau.

*   **Use Cases của Bệnh nhân:**
    *   **UC-1: Đăng ký tài khoản bệnh nhân**: Cho phép người dùng mới tạo tài khoản và xác minh danh tính (qua SĐT).
    *   **UC-2: Đăng nhập tài khoản**: Cho phép người dùng đã đăng ký đăng nhập. Hỗ trợ khôi phục mật khẩu.
    *   **UC-3: Đặt lịch hẹn tư vấn từ xa**: Tìm chuyên gia, chọn lịch, nhập lý do, kiểm tra/thanh toán chi phí có tích hợp bảo hiểm. Có luồng thay thế cho lọc chuyên gia, thanh toán thất bại, vấn đề xác minh bảo hiểm.
    *   **UC-4: Cập nhật hồ sơ sức khỏe**: Cập nhật thông tin cá nhân, tiền sử bệnh, dị ứng.
    *   **UC-5: Quản lý thông tin bảo hiểm**: Thêm, cập nhật, xóa thông tin BHYT, có thể xác minh thủ công hoặc tự động, quản lý nhiều thẻ.
    *   **UC-6: Quản lý thuốc và lịch uống thuốc**: Thêm, chỉnh sửa thuốc đang dùng, cài đặt nhắc nhở.
    *   **UC-7: Theo dõi sức khỏe**: Nhập chỉ số sức khỏe định kỳ (huyết áp, đường huyết...) và xem biểu đồ.
    *   **UC-8: Quản lý hồ sơ sức khỏe gia đình**: Thêm và theo dõi hồ sơ thành viên gia đình từ một tài khoản.
    *   **UC-9: Nhận thông báo lịch hẹn**: Nhận thông báo tự động (đẩy, SMS, email) về lịch hẹn sắp tới, bao gồm trạng thái thanh toán.
    *   **UC-10: Xem hồ sơ y tế điện tử cá nhân**: Truy cập lịch sử y tế (chẩn đoán, điều trị, thuốc, xét nghiệm, tiêm chủng), có thể lọc hoặc tải về.
    *   **UC-11: Tham gia tư vấn từ xa**: Tham gia cuộc gọi video/âm thanh với bác sĩ, có xử lý vấn đề kỹ thuật hoặc bác sĩ trễ.
    *   **UC-12: Gửi tin nhắn bảo mật để hỏi về y tế**: Gửi tin nhắn không khẩn cấp cho chuyên gia (có giới hạn lượt miễn phí), có thể đính kèm tệp. Xử lý khi hết lượt nhắn tin.
    *   **UC-13: Đặt lịch tiêm chủng**: Đặt lịch tiêm vaccine, chọn hình thức (tại cơ sở/tại nhà), kiểm tra/thanh toán chi phí có tích hợp bảo hiểm, nhận nhắc nhở. Có luồng cho thành viên gia đình, bảo hiểm chi trả toàn phần, xác minh bảo hiểm/thanh toán thất bại, hủy lịch.
    *   **UC-14: Thanh toán dịch vụ y tế**: Thanh toán lịch hẹn, tư vấn, tiêm chủng qua nhiều phương thức, tích hợp bảo hiểm, tạo biên lai điện tử. Xử lý thanh toán thất bại, áp dụng mã giảm giá, thanh toán tại chỗ.
    *   **UC-15: Xem lịch sử thanh toán**: Xem, lọc, tìm kiếm lịch sử giao dịch, tải biên lai/báo cáo, yêu cầu hoàn tiền.
    *   **UC-16: Quản lý số lượng tin nhắn**: Kiểm tra số lượt nhắn tin miễn phí còn lại, xem gói đã mua, mua thêm gói tin nhắn.

*   **Use Cases của Chuyên gia y tế:**
    *   **UC-17: Xem bảng lịch hẹn sắp tới**: Xem và quản lý lịch hẹn (theo ngày/tuần/tháng), xem chi tiết, thêm ghi chú, chặn thời gian không sẵn sàng.
    *   **UC-18: Nhận thông báo về các cuộc hẹn mới**: Nhận thông báo (đẩy, email) khi có cuộc hẹn mới.
    *   **UC-19: Truy cập lịch sử bệnh án**: Xem lịch sử đầy đủ của bệnh nhân (chẩn đoán, điều trị, thuốc, xét nghiệm...), có thể lọc dữ liệu.
    *   **UC-20: Ghi chẩn đoán và kê đơn**: Nhập chẩn đoán (theo mã chuẩn hóa), tìm thuốc trong CSDL, kê đơn điện tử, hệ thống kiểm tra tương tác thuốc và dị ứng, gửi đơn thuốc cho bệnh nhân. Xử lý khi phát hiện tương tác nguy hiểm.
    *   **UC-21: Chia sẻ tài liệu giáo dục**: Chia sẻ tài liệu từ thư viện hoặc tải lên tài liệu tùy chỉnh cho bệnh nhân.
    *   **UC-22: Thực hiện tư vấn từ xa**: Thực hiện cuộc gọi video/âm thanh với bệnh nhân, xem trước thông tin, ghi chú trong buổi tư vấn, nhập tóm tắt sau tư vấn. Xử lý bệnh nhân vắng mặt hoặc sự cố kỹ thuật.
    *   **UC-23: Trả lời tin nhắn bảo mật từ bệnh nhân**: Xem và trả lời tin nhắn, có thể đề nghị hẹn khám trực tiếp nếu cần.

*   **Use Cases của Quản trị viên:**
    *   **UC-24: Quản lý vai trò và quyền truy cập**: Quản lý danh sách người dùng, thay đổi vai trò/quyền, tạo vai trò mới, vô hiệu hóa tài khoản.
    *   **UC-25: Quản lý giá tiền dịch vụ**: Thiết lập và quản lý giá các dịch vụ (tư vấn, tiêm chủng, tin nhắn), thiết lập giảm giá/khuyến mãi, lên lịch thay đổi giá.

*   **Use Case chung/khác:**
    *   **UC-26: Tìm thông tin thuốc bằng QR**: Cho phép bệnh nhân hoặc chuyên gia y tế quét mã QR trên hộp thuốc để tra cứu thông tin. Xử lý mã QR không hợp lệ hoặc không tìm thấy thông tin.
