# Quản lý Product Backlog cho chương trình "GreenMart Loyalty"

*Tài liệu vận hành Scrum – Scrum Master kiêm BA, đội Hoa – TechViet*

## Phần A — Thiết kế vận hành Scrum

### A1. Độ dài Sprint: **2 tuần** (4 Sprint trong 8 tuần)

Sprint 2 tuần chia đều 8 tuần thành 4 lần phát hành có thể kiểm tra, đủ ngắn để mỗi thay đổi từ Marketing chờ tối đa ddưới 2 tuần, nhưng đủ dài để hoàn thành trọn một nhóm tính năng Must have kèm kiểm thử. Sprint 1 tuần có chi phí họp quá lớn so với phạm vi công việc; Sprint 4 tuần chỉ cho 2 vòng phản hồi, quá ít để thích nghi.

### A2. Phân vai trò Scrum

| Vai trò | Người đảm nhiệm | Trách nhiệm trong giai đoạn Loyalty |
| --- | --- | --- |
| **Product Owner (PO)** | Đại diện sản phẩm/Marketing được TechViet ủy quyền | Sở hữu và sắp xếp thứ tự Product Backlog; chốt quy tắc nghiệp vụ (tỷ lệ quy đổi, hạn điểm, chính sách ưu đãi); là đầu mối duy nhất tiếp nhận yêu cầu từ Marketing, Kế toán; đặt Sprint Goal cùng đội; nghiệm thu hạng mục tại Sprint Review. |
| **Scrum Master (SM)** (kiêm BA) | Bạn | Bảo đảm Scrum được thực hiện đúng, tổ chức các sự kiện, gỡ trở ngở cho đội, bảo vệ Sprint khỏi thay đổi giữa chừng; với vai trò BA: đặc tả nghiệp vụ, viết/tinh chỉnh user story và Acceptance Criteria, làm cầu nối giữa Marketing – Kế toán – đội kỹ thuật. |
| **Development Team** | Đội Hoa (lập trình, kiểm thử, thiết kế UX) | Tự tổ chức để biến Sprint Backlog thành Increment đạt Definition of Done; ước lượng nỗ lực; cam kết khối lượng Sprint dựa trên năng lực thực tế; kiểm thử và đảm bảo chất lượng. |

### A3. Sự kiện quan trọng nhất: **Sprint Review**

Trong giai đoạn Loyalty, Sprint Review là sự kiện quan trọng nhất vì đây là lúc Marketing, Kế toán và PO trực tiếp xem Increment chạy thật (tích điểm, đổi điểm, đối soát) để đánh giá. Sự kiện này thể hiện rõ nhất trụ cột **Thanh tra (Inspection)**: kiểm tra sản phẩm làm ra có đúng quy tắc nghiệp vụ và số tiền/điểm có khớp hay không. Kết quả thanh tra đó cũng là đầu vào để **Thích nghi** Product Backlog cho Sprint tiếp theo (ví dụ khi Marketing đổi tỷ lệ quy đổi), còn **Minh bạch** được bảo đảm nhờ mọi bên cùng xem một Increment và một Product Backlog.

## Phần B — Product Backlog & ưu tiên hoá bằng MoSCoW

### B1. Tiêu chí ưu tiên (áp dụng thống nhất)

| Loại | Điều kiện xếp loại |
| --- | --- |
| **Must have** | Thiếu thì chương trình không vận hành được, **hoặc** sai điểm/sai tiền gây rủi ro tài chính, đối soát kế toán. Khách hàng không thể nhận giá trị cốt lõi (tích và đổi điểm). |
| **Should have** | Quan trọng cho minh bạch/trải nghiệm hoặc kiểm soát rủi ro, nhưng có thể có workaround tạm thời hoặc chưa cần ngay (chưa đến hạn sử dụng). |
| **Could have** | Tăng giá trị/tiện lợi, không ảnh hưởng vận hành cốt lõi; làm nếu còn nguồn lực. |
| **Won't have this time** | Ngoài phạm vi giai đoạn 8 tuần, ghi nhận để xem xét sau. |

Các yếu tố cân nhắc: (1) giá trị giữ chân khách hàng, (2) rủi ro tài chính/tuân thủ kế toán, (3) mức phụ thuộc giữa các hạng mục, (4) thời điểm thực sự cần (ví dụ điểm đầu tiên chỉ hết hạn sau 12 tháng), (5) nỗ lực ước lượng (story point tương đối).

### B2. Product Backlog

| ID | Hạng mục | Lý do xếp loại | MoSCoW | Ước lượng (SP) |
| --- | --- | --- | --- | --- |
| PB-01 | Tích điểm sau thanh toán thành công (10.000đ = 1 điểm) | Giá trị cốt lõi; mọi hạng mục khác phụ thuộc vào số dư điểm | **Must** | 8 |
| PB-02 | Đổi điểm lấy mã giảm giá (100 điểm = 20.000đ) | Giá trị cốt lõi thứ hai; ảnh hưởng trực tiếp số tiền giảm | **Must** | 8 |
| PB-03 | Thu hồi điểm khi đơn bị hủy/hoàn | Không có thì điểm ảo, sai lệch số liệu kế toán | **Must** | 5 |
| PB-04 | Xem lịch sử tích/đổi điểm | Yêu cầu minh bạch của Kế toán và UX; có thể tra tạm qua dữ liệu nội bộ | **Should** | 5 |
| PB-05 | Chặn cộng dồn ưu đãi khi dùng mã đổi điểm (trừ khi hệ thống xác nhận) | Tránh giảm giá chồng sai tiền; hệ thống có thể tạm thời chỉ cho dùng một ưu đãi mỗi đơn | **Should** | 5 |
| PB-06 | Tự động trừ điểm hết hạn sau 12 tháng | Cần trước mốc hết hạn đầu tiên (12 tháng sau), chưa cần ở Sprint 1 | **Should** | 8 |
| PB-07 | Thông báo điểm sắp hết hạn | Cải thiện trải nghiệm, phụ thuộc PB-06 | **Could** | 5 |
| PB-08 | Trang quản trị cấu hình tỷ lệ quy đổi điểm cho Marketing | Tiện lợi, giảm phụ thuộc kỹ thuật khi đổi tỷ lệ; ban đầu có thể cấu hình qua tham số hệ thống | **Could** | 5 |
| PB-09 | Hạng thành viên (Bạc/Vàng) và chuyển điểm giữa các tài khoản | Ngoài phạm vi 8 tuần, rủi ro nghiệp vụ lớn | **Won't (this time)** | – |

### B3. Danh sách Sprint 1

Ràng buộc: toàn bộ Must + tối đa 2 Should.

- **Must (3/3):** PB-01, PB-02, PB-03 — tổng 21 SP.
- **Should (2/2):** PB-04 (lịch sử giao dịch) và PB-05 (chặn cộng dồn ưu đãi) — tổng 10 SP.
- **Không đưa vào Sprint 1:** PB-06 (để Sprint 2 vì chưa có điểm nào hết hạn trước 12 tháng), PB-07, PB-08 (Could), PB-09 (Won't).

**Sprint Goal đề xuất:** *"Khách hàng tích và đổi điểm đúng quy tắc, điểm bị thu hồi khi đơn hủy, và Kế toán tra được lịch sử giao dịch."*

## Phần C — Acceptance Criteria & Definition of Done

### C1. Hạng mục được chọn: **PB-01 – Tích điểm sau thanh toán thành công**

*Giả định cần PO/Kế toán xác nhận:* điểm = làm tròn **xuống** (số tiền thực thanh toán ÷ 10.000), không tính phí vận chuyển; mỗi điểm có hạn 12 tháng kể từ ngày tích.

**AC1 – Kịch bản chính (đơn thành công):**

- **Given** khách hàng có tài khoản GreenMart Loyalty, số dư 0 điểm
- **When** đơn hàng 255.000đ chuyển sang trạng thái "thanh toán thành công"
- **Then** hệ thống cộng 25 điểm vào tài khoản, ghi một giao dịch "Tích điểm" gắn mã đơn hàng, và gán hạn sử dụng 12 tháng kể từ ngày tích.

**AC2 – Đơn chưa đạt mức tối thiểu:**

- **Given** khách có đơn hàng thanh toán thành công trị giá 9.999đ
- **When** hệ thống xử lý tích điểm
- **Then** khách nhận 0 điểm, không phát sinh giao dịch tích điểm, và không báo lỗi.

**AC3 – Đơn chưa thành công:**

- **Given** đơn hàng ở trạng thái "chờ thanh toán" hoặc "thanh toán thất bại"
- **When** hệ thống nhận cập nhật trạng thái đơn
- **Then** không cộng điểm; điểm chỉ được cộng khi trạng thái chuyển sang "thành công".

**AC4 – Ngoại lệ: thông báo thanh toán trùng (bẫy dữ liệu):**

- **Given** đơn hàng 255.000đ đã được tích 25 điểm
- **When** cổng thanh toán gửi lặp lại cùng thông báo "thành công" cho đơn đó
- **Then** hệ thống không cộng thêm điểm (mỗi mã đơn chỉ tích điểm một lần) và ghi log sự kiện trùng.

**AC5 – Ngoại lệ: đơn bị hủy sau khi đã tích điểm:**

- **Given** đơn hàng 255.000đ đã tích 25 điểm, khách còn 25 điểm
- **When** đơn bị hủy hoặc hoàn tiền
- **Then** hệ thống thu hồi đúng 25 điểm bằng một giao dịch "Thu hồi" gắn mã đơn (chi tiết xử lý trường hợp khách đã đổi hết điểm thuộc PB-03; đề xuất cho phép số dư âm tạm thời và trừ vào lần tích sau, cần Kế toán xác nhận).

### C2. Definition of Done chung cho Sprint 1

DoD không lặp lại các kịch bản đã nêu trong AC mà quy định chuẩn chất lượng áp dụng cho **mọi** hạng mục:

1. **Chất lượng mã nguồn:** đã qua code review bởi ít nhất một thành viên khác, đã merge vào nhánh chính và build thành công trên pipeline.
2. **Kiểm thử:** có unit test cho logic tính điểm và quy đổi với độ bao phủ tối thiểu 80% phần logic này; kiểm thử hồi quy tự động đạt 100%; không còn lỗi mức nghiêm trọng (Sev1/Sev2) đang mở.
3. **Triển khai:** đã triển khai trên môi trường staging và chạy thử qua một luồng đầu–cuối (mua hàng → tích điểm → đổi điểm).
4. **Đối soát kế toán:** tổng điểm cộng trừ trong sổ giao dịch khớp với số dư tài khoản trên bộ dữ liệu mẫu; Kế toán xác nhận định dạng đối soát.
5. **Cấu hình & bảo mật:** các tham số nghiệp vụ (tỷ lệ tích, tỷ lệ quy đổi, thời hạn điểm) không viết cứng trong mã; có ghi nhật ký kiểm toán (audit log) cho mọi thay đổi số dư điểm.
6. **Tài liệu:** tài liệu nghiệp vụ/API đã cập nhật; PO đã xem và nghiệm thu tại Sprint Review.

## Phần D — Xử lý tình huống thay đổi tỷ lệ quy đổi

*Tình huống:* giữa Sprint 1, Marketing yêu cầu đổi từ 100 điểm = 20.000đ sang 100 điểm = 25.000đ.

### D1. Quy trình tiếp nhận không phá vỡ Sprint

1. **Đi qua PO:** Marketing gửi yêu cầu cho PO (không giao thẳng cho đội). PO ghi vào Product Backlog dưới dạng hạng mục mới và xếp thứ tự ưu tiên.
2. **Sprint Goal được bảo vệ:** Sprint Backlog và Sprint Goal không bị thay đổi đơn phương. Scrum Master phối hợp với đội đánh giá nhanh tác động (BA phân tích phạm vi, Dev ước lượng). Nếu PB-02 đã dùng tham số cấu hình (theo DoD) thì thay đổi chỉ là giá trị cấu hình, nhỏ và không đe dọa Sprint Goal.
3. **Hai nhánh xử lý:**
   - *Nhánh khuyến nghị:* nếu nhỏ, PO và đội thương lượng đưa vào Sprint hiện tại bằng cách đổi lấy hạng mục tương đương (ví dụ hoãn bớt một Should), Sprint Goal vẫn giữ nguyên.
   - *Nhánh còn lại:* nếu cần làm lại đáng kể, đưa vào đầu Backlog và triển khai ở Sprint 2 (chờ tối đa vài ngày đến cuối Sprint 1).
4. **Hủy Sprint chỉ là phương án cuối:** chỉ PO có quyền hủy Sprint khi Sprint Goal không còn giá trị; trường hợp này không đáp ứng điều kiện đó.
5. **Thích nghi:** nội dung thay đổi được trình bày lại tại Sprint Review và Sprint Planning kế tiếp; chương trình chưa go-live ở Sprint 1 nên chưa gây ảnh hưởng đến khách hàng thật.

*Câu hỏi cần PO chốt:* tỷ lệ mới áp dụng từ ngày nào, và áp dụng cho cả điểm đã tích hay chỉ cho các lần đổi sau ngày hiệu lực? Kế toán cũng cần được thông báo vì ảnh hưởng đến giá trị nghĩa vụ điểm tồn.

### D2. Tác động đến các tài liệu đã lập

| Tài liệu | Cần cập nhật |
| --- | --- |
| **Product Backlog (Phần B)** | PB-02: sửa mô tả sang 100 điểm = 25.000đ. PB-08 (cấu hình tỷ lệ) nâng từ Could lên **Should** vì đã chứng minh nhu cầu thay đổi thường xuyên. Thêm hạng mục mới PB-10: "Quản lý tỷ lệ quy đổi theo phiên bản và ngày hiệu lực". Sắp xếp lại thứ tự ưu tiên Sprint 2. |
| **Acceptance Criteria (Phần C)** | PB-01 (tích điểm) **không đổi** vì tỷ lệ tích 10.000đ = 1 điểm giữ nguyên. Các AC của PB-02 phải sửa giá trị (ví dụ 100 điểm đổi 25.000đ). Thêm AC mới: đổi điểm trước và sau ngày hiệu lực dùng đúng tỷ lệ tương ứng; đơn hoàn dùng tỷ lệ tại thời điểm đổi. |
| **Definition of Done (Phần C)** | Bổ sung: tỷ lệ quy đổi lấy từ cấu hình có phiên bản và ngày hiệu lực; Kế toán xác nhận đối soát với tỷ lệ mới; hồi quy toàn bộ luồng đổi điểm với cả hai tỷ lệ. Các tiêu chí cũ giữ nguyên. |

*Bài học:* thiết kế tham số hóa tỷ lệ ngay từ DoD giúp việc thay đổi giữa chừng chỉ tốn nỗ lực nhỏ mà không làm gián đoạn Sprint đang chạy.
