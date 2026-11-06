# CYAN Win2HDD — Downloads

Ứng dụng tiếng Việt để chuẩn bị cài lại Windows 10/11 hoặc Windows Server 2019/2022/2025 x64 trên UEFI/GPT, không cần USB. Mã nguồn nằm trong repository private riêng; kho này chứa bộ cài và gói cập nhật.

[**Tải CYAN Win2HDD trên CYANPRO**](https://cyanpro.app/tools/cyan-win2hdd) · [Release preview.7](https://github.com/cyan881990/cyan-win2hdd-releases/releases/tag/v0.1.0-preview.7)

**Preview.7** sửa lỗi JSON khi đọc ISO bằng cách tách nhật ký khỏi dữ liệu trả về, đã kiểm tra qua PowerShell thật. Tiếp tục hỗ trợ ISO Windows Server 2019/2022/2025, phân biệt Server Core/Desktop Experience và sửa lỗi nhận diện WinPE khiến ISO x64 hợp lệ bị từ chối. Danh sách tải có các trang Microsoft Evaluation Center chính thức.

![CYAN Win2HDD](https://github.com/cyan881990/cyan-win2hdd-releases/releases/download/v0.1.0-preview.7/CYAN-Win2HDD-preview.png)

- `CYAN.Win2HDD-win-Setup.exe`: bộ cài cho tài khoản Windows hiện tại, tích hợp cập nhật Velopack qua link CYANPRO.
- `CYAN.Win2HDD-win-Portable.zip`: bản chạy từ thư mục; khi có bản mới, mở link Setup do CYANPRO trả về.
- `.nupkg`, `releases.win.json`, `RELEASES`, `assets.win.json`: dữ liệu dành cho updater.

Bấm **Chọn file ISO trên máy** → **Đọc ISO** và cấp quyền quản trị → chọn edition thực sự có trong file. Với Server, **Desktop Experience** có giao diện desktop; **Server Core** quản lý bằng PowerShell/từ xa. Cài mới sẽ xóa dữ liệu và vai trò máy chủ trên phân vùng Windows sau xác nhận trong WinPE.

Chưa có ISO: chọn **Tải Windows chính thức từ Microsoft**. Có thể mở trình duyệt ngoài để tải hoặc tạo ISO rồi chọn file trong CYAN. Link ISO được tải từ máy chủ Microsoft, có tiến độ/hủy và đối chiếu SHA-256 khi cung cấp hash công bố. Evaluation Server có thời hạn; license CYAN không cấp bản quyền Windows Server. Kho này không phân phối lại ISO Windows.

Xem cấu hình và tải/chọn ISO miễn phí. Chuẩn bị bộ cài và tạo lượt boot cần đăng nhập CYANPRO với license hợp lệ. CYANPRO cung cấp phiên bản và link cập nhật.

Máy chạy tool: Windows 10 2004+/11 hoặc Server 2022/2025 có Desktop Experience, x64, UEFI/GPT, RAM từ 8 GB. Cần phân vùng Windows từ 64 GB và phân vùng NTFS riêng để lưu bộ cài; Windows và staging phải giải mã BitLocker hoàn toàn. Chưa hỗ trợ tự thu nhỏ C:, BIOS, ARM64, clone hoặc VHD.

**Đây là bản preview, chưa nghiệm thu cài Windows/Server thật trong VM và chưa ký Authenticode.** Đã kiểm tra metadata bằng kiểu DISM thật với fixture, handler WPF, guard an toàn, tải ISO Windows 11 thật và checksum. Chỉ thử triển khai trong VM UEFI dùng riêng sau khi sao lưu. BCD backup không khôi phục dữ liệu đã xóa.
