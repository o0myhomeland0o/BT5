## BT5
# Phạm Duy Tiến Minh K225480106048
A. Trình bày lại đầu bài của đồ án PT&TKHT:

Mô tả bài toán của đồ án PT&TKHT, đưa ra yêu cầu của bài toán đó
Cơ sở dữ liệu của Đồ án PT&TKHT : Có database với các bảng dữ liệu cần thiết (3nf), Các bảng này đã có PK, FK, CK cần thiết
B. Nội dung Bài tập 05:

Dựa trên cơ sở là csdl của Đồ án
Tìm cách bổ xung thêm 1 (hoặc vài) trường phi chuẩn (là trường tính toán đc, nhưng thêm vào thì ok hơn, ok hơn theo 1 logic nào đó, vd ok hơn về speed) => Nêu rõ logic này!
Viết trigger cho 1 bảng nào đó, mà có sử dụng trường phi chuẩn này, nhằm đạt được 1 vài mục tiêu nào đó. => Nêu rõ các mục tiêu
Nhập dữ liệu có kiểm soát, nhằm để test sự hiệu quả của việc trigger auto run.
Kết luận về Trigger đã giúp gì cho đồ án của em.
HƯỚNG DẪN CÁCH LÀM:

Hướng dẫn làm phần A:

Chỉ cần nêu ra y/c của đồ án.
Không cần chụp quá trình làm ra db, tables.
Chỉ cần đưa ra db gồm các bảng nào, mỗi bảng có các trường nào, kiểu dữ liệu nào, và pk, fk, ck của các bảng.
Hướng dẫn làm phần B:

Sv tạo repo mới trên github, cho phép truy cập public.
Tạo file Readme.md, đầu file để thông tin cá nhân sv.
Tiếp theo đưa phần A vào file Reame.md .
Các thao tác làm trên csdl bằng phần mềm ssms.
Chụp ảnh màn hình quá trình làm.
Paste ngay vào Readme.md, rồi gõ mô tả ảnh này làm gì, nhập gì, hay đạt được điều gì...
Có thể thêm những nhận xét hoặc kết luận cho việc bản thân đã hiểu rõ thêm về 1 vấn đề gì đó.
Lặp lại các step 4 5 6 cho đến khi hoàn thành yêu cầu của phần B.
Xuất các file sql chứa cấu trúc và data, up lên cùng repo.
Link đến repo cần mở được trực tiếp nội dung, Paste link này vào file excel online ghim trên nhóm. Thầy sẽ dùng tool để check các link này.
DEADLINE: 23H59:59 NGÀY 23/04/2025

p/s:

Sv được phép tham khảo mọi nguồn, nhưng phải tự làm lại.
Đọc thêm nội quy học tập để biết các chế tài.
Đã đến lúc khẳng định bản thân và toả sáng!
Chỗ nào vướng mắc cứ share lên nhóm để cùng tháo gỡ.

## Mô tả và yêu cầu của bài:
Trường ĐH công nghiệp kỹ thuật thái nguyên mỗi năm sẽ phải tiếp một số lượng sinh viên lớn, dẫn đến khó khăn trong việc quản lý điểm số, đặc biệt trong các đợt tổng kết học kỳ và cuối năm. Phòng đào tạo cần một hệ thống quản lý điểm để:
1.Giảm sai sót khi nhập điểm, in bảng điểm.
Theo dõi toàn diện quá trình học tập của sinh viên từ khi nhập học đến khi tốt nghiệp.
Tự động hóa công tác thống kê, xét học bổng, thi lại, lưu ban.
2. Chức năng chính của hệ thống
-Quản lý điểm chi tiết:
Cập nhật điểm theo từng môn học, học kỳ.
Tính điểm trung bình, điểm rèn luyện tự động.
Lưu trữ điểm thi lần 1, lần 2 (nếu có).
-Tra cứu thông tin sinh viên:
Ngày sinh, quê quán, chỗ ở hiện tại.
Lịch sử học tập, kết quả từng học kỳ.
-Thống kê và báo cáo:
Xếp loại học lực, hạnh kiểm.
Hỗ trợ xét học bổng, khen thưởng, cảnh báo sinh viên yếu kém.
Xuất bảng điểm theo lớp/khoa/học kỳ.
-Lưu trữ hồ sơ:
Đảm bảo dữ liệu nhất quán từ khi nhập học đến khi ra trường.
Giảm thiểu giấy tờ, sổ sách thủ công.
3. Đối tượng sử dụng
Phòng đào tạo: Nhập điểm, tổng hợp kết quả học tập.
Giảng viên: Cập nhật điểm thành phần (chuyên cần, giữa kỳ, cuối kỳ).
Sinh viên: Tra cứu điểm cá nhân, xem thông báo.
Ban lãnh đạo: Xem báo cáo tổng quan về chất lượng đào tạo.
4. Lợi ích
Tính chính xác: Loại bỏ sai sót do thủ công.
Tiết kiệm thời gian: Tự động hóa quy trình thống kê.
Minh bạch: Sinh viên có thể tự theo dõi tiến trình học tập.
Lưu trữ bền vững: Dữ liệu được số hóa toàn bộ.

## Bài làm:
# Tạo các table:
* khoa
![image](https://github.com/user-attachments/assets/cdf1f845-3027-4b42-9c93-37aff6c357e8)
* lop
![image](https://github.com/user-attachments/assets/bdfdabec-eb9b-4793-b3a1-501904d42552)
* sinhvien
![image](https://github.com/user-attachments/assets/d5159d5c-5412-41ed-93ae-b2be5d767042)
* hocki
![image](https://github.com/user-attachments/assets/80dd1a9a-4bb6-4938-9ef7-6615aac0fd10)
* monhoc
![image](https://github.com/user-attachments/assets/0f13eecd-707e-4699-ba16-fb2e74b494ee)
* diem
![image](https://github.com/user-attachments/assets/f2e0415e-97cc-40fa-8133-f5c133bd9812)
* thongke
![image](https://github.com/user-attachments/assets/afb47414-5c8a-434a-b4de-9ac3f511c393)
* giangvien
![image](https://github.com/user-attachments/assets/c46e2998-67e6-4a93-9733-71c4e1dae4d9)
* sinhvien_has_monhoc
![image](https://github.com/user-attachments/assets/9b1f53cb-5876-46a7-a11f-5135c98dbc04)
* sinhvien_has_diem
![image](https://github.com/user-attachments/assets/492986a9-b876-46c0-9b89-9339c8a1b937)
* monhoc_has_giangvien
![image](https://github.com/user-attachments/assets/5c122266-f79e-44c4-9b1d-e8bd417608d4)
* sinhvien_has_giangvien
![image](https://github.com/user-attachments/assets/95325b0c-c9ac-4e75-bccc-c6416d2e68ab)
* thongke_has_hocki
![image](https://github.com/user-attachments/assets/f44e40ca-a49d-447f-b3ae-167654201e48)
* thongke_has_lop
![image](https://github.com/user-attachments/assets/1997ddd7-9b40-4bd5-bf98-2a395ba64994)

## Diagram liên kết:
![image](https://github.com/user-attachments/assets/b4e5dfa9-ff04-44fa-b03c-142938285136)
![image](https://github.com/user-attachments/assets/dc07c964-bc79-471a-93a1-1168e95c80e4)



