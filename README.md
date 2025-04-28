Bài tập 6: Hệ quản trị CSDL

HOÀNG ĐỨC HỘI - MSV: K225480106085

Chủ đề: Câu lệnh Select

Yêu cầu bài tập: 

Cho file sv_tnut.sql (1.6MB)

1. Hãy nêu các bước để import được dữ liệu trong sv_tnut.sql vào sql server của em
2. dữ liệu đầu vào là tên của sv; sđt; ngày, tháng, năm sinh của sinh viên (của sv đang làm bài tập này)
3. nhập sql để tìm xem có những sv nào trùng hoàn toàn ngày/tháng/năm với em?
4. nhập sql để tìm xem có những sv nào trùng ngày và tháng sinh với em?
5. nhập sql để tìm xem có những sv nào trùng tháng và năm sinh với em?
6. nhập sql để tìm xem có những sv nào trùng tên với em?
7. nhập sql để tìm xem có những sv nào trùng họ và tên đệm với em.
8. nhập sql để tìm xem có những sv nào có sđt sai khác chỉ 1 số so với sđt của em.
9. BẢNG SV CÓ HƠN 9000 ROWS, HÃY LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG  VIỆT, GIẢI THÍCH.
10. HÃY NHẬP SQL ĐỂ LIỆT KÊ CÁC SV NỮ NGÀNH KMT CÓ TRONG BẢNG SV (TRÌNH BÀY QUÁ TRÌNH SUY NGHĨ VÀ GIẢI NHỮNG VỨNG MẮC)

DEADLINE: 23H59:59 NGÀY 25/4/2025

Ghi chú: Giải thích tại sao lại có SQL như vậy.



1. Các bước nhập dữ liệu từ file sv_tnut.sql vào máy chủ sql:

B1: Sau khi kết nối tới sql server, chọn file ---> open ---> file...:


![Screenshot 2025-04-28 230856](https://github.com/user-attachments/assets/7c6a2bd7-b72b-4477-90f4-6dd84f74accc)


B2: Chọn đường dẫn tải file về chọn đúng file sv_tnut.sql:


![Screenshot 2025-04-28 230934](https://github.com/user-attachments/assets/034175fa-b46a-4e57-97bb-b9c091805b76)


B3: Tạo cơ sở dữ liệu với tên sv_tnut để sao chép lệnh use[sv_tnut] của thầy(lệnh sử dụng cơ sở dữ liệu):


![Screenshot 2025-04-28 230953](https://github.com/user-attachments/assets/52d6b06a-a9d4-43e1-9462-bf10d994e53b)


B3: Lệnh đen use[sv_tnut] và lệnh tạo SV bảng để tạo bảng trước đó và mới nhập dữ liệu (bài em tạo bảo rồi nên nó hiện các lỗi).


![Screenshot 2025-04-29 000817](https://github.com/user-attachments/assets/51272dae-5617-4b59-a866-e3875abdc366)



- Kết quả chúng tôi đã tìm thấy cơ sở dữ liệu có sẵn trong bảng dbo.SV:


![Screenshot 2025-04-28 231948](https://github.com/user-attachments/assets/a340c60c-c29d-43c5-88b5-da9d092445ae)


B4: Black(select) các lệnh Insert (toàn bộ mã còn lại) rồi chạy để tải dữ liệu vào SV bảng:

![Screenshot 2025-04-28 232317](https://github.com/user-attachments/assets/834877a6-a45b-4896-8c77-887fbf2c4cd5)


2. Truy vấn thông tin của em ( Hoàng Đức Hội) với đầu vào dữ liệu là tên; sđt; ngày, tháng, năm sinh
Truy vấn mới để truy vấn mã

- Sử dụng lệnh SELECT các trường tên, ngày sinh, số điện thoại từ bảng SV trong đó các trường tên = dữ liệu phù hợp với thông tin của em:


![Screenshot 2025-04-28 232525](https://github.com/user-attachments/assets/ebc13eec-1f0d-408c-9a38-e5812c6805a5)


3. Truy vấn các sinh viên trùng hoàn toàn tháng năm sinh với em:


- Sử dụng lệnh ngày, tháng, năm để lấy ngày, tháng, năm từ các cột có kiểu Date để so sánh:

![Screenshot 2025-04-28 232734](https://github.com/user-attachments/assets/ac039b6d-44f4-48b0-8744-6bfa4fb25cd7)


4. Truy vấn các thông tin trùng lặp ngày và tháng sinh:

![Screenshot 2025-04-28 232818](https://github.com/user-attachments/assets/ee71c2ba-552c-450d-8aed-1e1cf0a1faeb)


5. Truy vấn thông tin những sinh viên trùng tháng và năm sinh với em:

![Screenshot 2025-04-28 233009](https://github.com/user-attachments/assets/3bafba39-429f-4caa-888c-e9fd3b7e4ed0)


6. Truy vấn thông tin các sinh viên trùng tên với em:

![Screenshot 2025-04-28 233050](https://github.com/user-attachments/assets/f72844e1-7b3b-48e0-be7e-5a48299b81e7)


7. Truy vấn thông tin về những sinh viên có trùng họ và tên đệm với em:

![Screenshot 2025-04-28 233158](https://github.com/user-attachments/assets/b0ae8b0f-699f-463c-bdbc-a13ad950c1d9)


8. Truy vấn những sinh viên có sdt khác chỉ 1 số với em:


![Screenshot 2025-04-28 233803](https://github.com/user-attachments/assets/ffa36a5a-7b4a-4c49-a235-edbb423c6fa1)


- Trong danh sách không có sinh viên nào sai số 1 so với SDT của em

9. LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG VIỆT:

![Screenshot 2025-04-28 234236](https://github.com/user-attachments/assets/64c8f144-6e2b-4e9f-a5e8-79a0a2ea5bb8)


Giải thích:

- WHERE lop THÍCH '%KMT': tìm trong cột lop có chuỗi chuỗi nào trùng lặp với ký tự KMT chuỗi thì Người gọi ra

- THU THẬP Vietnamese_CI_AS: Sắp xếp tên và đệm kiểu tiếng Việt theo thứ tự từ a->z

10. Truy vấn các sinh viên nữ chuyên ngành KMT có trong bảng SV:

![Screenshot 2025-04-29 000048](https://github.com/user-attachments/assets/79705088-68a9-4a42-965c-4241d0dbedc5)


- Truy vấn tên của toàn bộ sv KMT
- Cop cột đưa ra tên Chat để giúp suy luận ra tên các bạn nữ
- Sau khi đã có tên thì hãy sử dụng các tên đó kèm theo lệnh WHERE lop THÍCH '%KMT%' AND ten IN ( các tên vừa suy luận)
- Kiểm tra số lượng nhưng ít nhất, khi đó chúng có thể tự động lọc tên các bạn nữ bằng tay
