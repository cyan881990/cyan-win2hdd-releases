# CYAN Win2HDD — Downloads

Ứng dụng tiếng Việt để chuẩn bị cài lại Windows 10/11 x64 trên UEFI/GPT, không cần USB. Mã nguồn được quản lý ở repository private riêng; kho này phát hành bộ cài và gói cập nhật.

[**Tải bản thử nghiệm preview.3**](https://github.com/cyan881990/cyan-win2hdd-releases/releases/tag/v0.1.0-preview.3)

**Preview.3** sửa hộp lưu từ WebView2, tiến độ/hủy/thử lại, trạng thái nút và lựa chọn edition khi đổi ISO. Giữ logo CYAN riêng, giao diện sáng và trình cài đặt 3 bước.

![Giao diện CYAN Win2HDD preview.3](https://github.com/cyan881990/cyan-win2hdd-releases/releases/download/v0.1.0-preview.3/CYAN-Win2HDD-preview.png)

- `CYAN.Win2HDD-win-Setup.exe`: bộ cài cho tài khoản Windows hiện tại, tích hợp cập nhật Velopack.
- `CYAN.Win2HDD-win-Portable.zip`: bản chạy từ thư mục; cài bằng Setup để dùng cập nhật tự động.
- `.nupkg`, `releases.win.json`, `RELEASES`, `assets.win.json`: dữ liệu dành cho updater.

Trong ứng dụng, chọn **Tải Windows chính thức từ Microsoft**, chọn Windows 10/11 và ngôn ngữ tại trang Microsoft. Link ISO được tải trực tiếp từ máy chủ Microsoft, có tiến độ/hủy và đối chiếu SHA-256 khi bạn cung cấp hash Microsoft công bố. Windows 10 có thể chuyển sang Media Creation Tool; tạo ISO bằng công cụ chính thức rồi chọn file trong CYAN. Edition Home/Pro được đọc từ ISO sau đó. Kho này không phân phối lại ISO Windows.

Đã tải ISO Windows 11 x64 English thật 9.047.330.816 byte bằng bộ tải CYAN và khớp SHA-256 Microsoft công bố; hủy tải thực rồi tải lại cũng đã qua. Kiểm tra nút WPF dùng handler và dữ liệu mô phỏng; chưa hoàn tất bấm chuột end-to-end trong desktop. Form Microsoft đã được thao tác trong Chrome, còn trang Microsoft trong WebView2 đã được kiểm tra mở thành công.

**Bản preview chưa kiểm chứng cài Windows thật trong VM; chưa có bản stable hoặc chữ ký Authenticode.** Có thể dùng để xem giao diện và thử luồng tải. Chỉ thử chức năng cài Windows trong VM UEFI dùng riêng. Chưa kiểm chứng cập nhật N → N+1 trên bản đã cài.

Bản đầu cần một phân vùng NTFS riêng để lưu bộ cài; Windows và phân vùng lưu phải giải mã BitLocker hoàn toàn. Chưa hỗ trợ tự thu nhỏ C:, BIOS, ARM64, clone hoặc VHD. Cài lại sẽ xóa dữ liệu phân vùng Windows sau xác nhận trong WinPE; BCD backup không khôi phục dữ liệu đã xóa.

No stable release is available. Preview releases are experimental; do not treat them as production-ready disk deployment software.
