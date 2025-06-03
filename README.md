Đây là một ứng dụng web mã hóa/giải mã file sử dụng thuật toán AES (Advanced Encryption Standard), được thiết kế với giao diện trực quan, hỗ trợ người dùng dễ dàng bảo mật thông tin trong file cá nhân bằng khóa bí mật tự chọn.

Ứng dụng cho phép:

Mã hóa file tải lên thành định dạng bảo mật .aes.

Giải mã file .aes để khôi phục dữ liệu ban đầu.

Giao diện được thiết kế hiện đại, đẹp mắt, sử dụng font chữ Poppins và hình nền tối để tăng tính bảo mật và trải nghiệm người dùng.

⚙️ CHỨC NĂNG CƠ BẢN
1. Tải file cần mã hóa/giải mã
Người dùng chọn file từ thiết bị thông qua input file.

2. Nhập khóa bảo mật
Người dùng nhập khóa bí mật để dùng cho quá trình mã hóa hoặc giải mã.

Khóa có thể là bất kỳ chuỗi ký tự nào, sau đó được xử lý bằng SHA-256 để tạo khóa thực tế.

3. Mã hóa file
Dùng thuật toán AES-CBC để mã hóa dữ liệu của file.

Sinh một vector khởi tạo (IV) ngẫu nhiên cho mỗi lần mã hóa.

Kết quả mã hóa sẽ được lưu thành file có đuôi .aes và tải về máy.

4. Giải mã file
File .aes được xử lý tách IV và dữ liệu.

Nếu khóa đúng, dữ liệu được khôi phục và tải về.

Nếu khóa sai hoặc file không hợp lệ, sẽ thông báo lỗi.

5. Giao diện tương tác
Có hiệu ứng loading (vòng quay) để hiển thị trạng thái xử lý.

Hiển thị thông báo kết quả ở phần giao diện người dùng.

 KỸ THUẬT – CÔNG NGHỆ SỬ DỤNG
 Giao diện (Frontend)
HTML5: Xây dựng cấu trúc trang.

CSS3: Thiết kế phong cách giao diện (màu tối, hiệu ứng bo góc, responsive).

Google Fonts: Font chữ Poppins.

Ảnh nền cố định với lớp phủ màu tối để tăng tương phản nội dung.

⚙️ Logic (Javascript)
Web Crypto API: Cung cấp khả năng mã hóa/giải mã AES:

crypto.subtle.digest() → tạo khóa SHA-256.

crypto.subtle.importKey() → nhập khóa AES từ hash.

crypto.subtle.encrypt() / decrypt() → mã hóa/giải mã dữ liệu.

ArrayBuffer và Uint8Array: Dùng để xử lý nhị phân dữ liệu file.

Blob + URL.createObjectURL(): Tạo đường dẫn tạm thời để tải file sau khi xử lý.

Event Handling: Bắt sự kiện click, xử lý hiển thị kết quả.
![image](https://github.com/user-attachments/assets/0c729407-8e3e-4b33-bc58-fd19683c6fa0)


