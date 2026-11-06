# CYAN Win2HDD — Downloads

Ứng dụng tiếng Việt để chuẩn bị cài lại Windows 10/11 x64 trên UEFI/GPT, không cần USB. Mã nguồn được quản lý ở repository private riêng; kho này chứa bộ cài và gói cập nhật.

[**Tải CYAN Win2HDD trên CYANPRO**](https://cyanpro.app/tools/cyan-win2hdd) · [Release preview.4](https://github.com/cyan881990/cyan-win2hdd-releases/releases/tag/v0.1.0-preview.4)

**Preview.4** bổ sung đăng nhập CYANPRO, quản lý license, logo mới và cập nhật theo phiên bản/link do CYANPRO cung cấp. Xem cấu hình và tải ISO miễn phí; chuẩn bị bộ cài và tạo lượt boot cần đăng nhập với license hợp lệ.

![CYAN Win2HDD](https://github.com/cyan881990/cyan-win2hdd-releases/releases/download/v0.1.0-preview.4/CYAN-Win2HDD-cover-1920x640.png)

- `CYAN.Win2HDD-win-Setup.exe`: bộ cài cho tài khoản Windows hiện tại, tích hợp cập nhật Velopack qua link CYANPRO.
- `CYAN.Win2HDD-win-Portable.zip`: bản chạy từ thư mục; khi có bản mới, mở link Setup do CYANPRO trả về.
- `.nupkg`, `releases.win.json`, `RELEASES`, `assets.win.json`: dữ liệu dành cho updater.

Trong ứng dụng, chọn **Tải Windows chính thức từ Microsoft**, chọn Windows 10/11 và ngôn ngữ tại Microsoft. Link ISO được tải trực tiếp từ máy chủ Microsoft, có tiến độ/hủy và đối chiếu SHA-256 khi cung cấp hash công bố. Windows 10 có thể chuyển sang Media Creation Tool; tạo ISO bằng công cụ chính thức rồi chọn file trong CYAN. Edition Home/Pro được đọc từ ISO sau đó. Kho này không phân phối lại ISO Windows.

Đã tải ISO Windows 11 x64 English thật 9.047.330.816 byte bằng bộ tải CYAN và khớp SHA-256 Microsoft công bố. Các kiểm thử WPF và phiên đăng nhập dùng dữ liệu mô phỏng. Đã xác minh API CYANPRO → link GitHub → tải toàn bộ Setup/gói cập nhật và checksum; chưa nghiệm thu nâng cấp N → N+1 trên bản đã cài hoặc đăng nhập license bằng tài khoản khách thật.

**Bản preview chưa kiểm chứng cài Windows thật trong VM; chưa có bản stable hoặc chữ ký Authenticode.** Có thể xem giao diện và thử tải ISO. Chỉ thử cài Windows trong VM UEFI dùng riêng, sau khi sao lưu.

Cần phân vùng NTFS riêng để lưu bộ cài; Windows và staging phải giải mã BitLocker hoàn toàn. Chưa hỗ trợ tự thu nhỏ C:, BIOS, ARM64, clone hoặc VHD. Cài lại xóa dữ liệu phân vùng Windows sau xác nhận trong WinPE; BCD backup không khôi phục dữ liệu đã xóa.
