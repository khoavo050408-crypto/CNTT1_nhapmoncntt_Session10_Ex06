PHẦN 1: PHÂN TÍCH HẠN CHẾ VÀ TỐI ƯU HÓA
1. Hai sai lầm trong tư duy lưu trữ của Nam
Sử dụng file nhị phân cho hệ thống Git: File Word (.docx) thực chất là một tệp nén chứa nhiều file XML cấu trúc phức tạp. Hệ thống Git được thiết kế để quản lý và so sánh văn bản thô theo từng dòng (line-by-line diff). Việc dùng file Word khiến Git coi toàn bộ tài liệu là một khối nhị phân đơn lẻ, do đó chỉ cần sửa một dấu phẩy, Git cũng hiểu là toàn bộ file đã bị thay đổi, gây ra lỗi xung đột (Conflict) nghiêm trọng khi làm việc nhóm.
Không đảm bảo tính tương thích trên nền tảng Web: GitHub hỗ trợ xem và chỉnh sửa trực tiếp các tài liệu dạng văn bản thô như Markdown ngay trên trình duyệt. Việc dùng file .docx buộc các thành viên trong nhóm phải tải file về máy, mở bằng phần mềm Microsoft Word rồi mới xem được nội dung, gây bất tiện và làm giảm hiệu suất làm việc.
2. Ưu thế chống hư hại của Markdown so với Rich Text (.docx)
Đặc tính file Rich Text (.docx): Do có cấu trúc đóng gói nén chặt chẽ, nếu quá trình tải lên hoặc tải xuống bị đứt gãy mạng làm mất/lỗi dù chỉ 1 byte dữ liệu, cấu trúc file sẽ bị gãy và Microsoft Word sẽ báo lỗi không thể mở được tệp (File Corrupted).
Đặc tính file Plain Text / Markdown (.md): Markdown là văn bản thô thuần túy. Nếu gặp sự cố mất mát dữ liệu, chỉ duy nhất vị trí ký tự đó bị ảnh hưởng hoặc hiển thị sai, toàn bộ phần nội dung còn lại của tài liệu vẫn hoàn toàn toàn vẹn và đọc được bình thường.
PHẦN 2: CHUYỂN ĐỔI TÀI LIỆU SANG MARKDOWN (GREENTECH-README.MD)
(Dưới đây là mã nguồn Markdown chuẩn để lưu thành file README.md trong thư mục dự án)
Markdown
# 🌿 GreenTech Project
> Dự án công nghệ xanh hỗ trợ giám sát và tối ưu hóa môi trường nông nghiệp thông minh.
## 📌 Giới thiệu dự án
GreenTech là giải pháp phần mềm kết hợp phần cứng IoT nhằm theo dõi các chỉ số môi trường (độ ẩm, nhiệt độ, ánh sáng) tại các trang trại, giúp tự động hóa quy trình tưới tiêu và tiết kiệm tài nguyên nước cho người nông dân.
## 🚀 Tính năng chính* **Giám sát thời gian thực:** Cập nhật liên tục dữ liệu từ các cảm biến môi trường.* **Cảnh báo thông minh:** Gửi thông báo khi các chỉ số vượt ngưỡng an toàn.* **Điều khiển tự động:** Kích hoạt hệ thống bơm/chiếu sáng dựa trên thuật toán tối ưu.
## 🛠️ Công nghệ sử dụng* **Ngôn ngữ:** Python, C++ (cho vi điều khiển)* **Quản lý mã nguồn:** Git & GitHub* **Định dạng tài liệu:** Markdown (.md)
