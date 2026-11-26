<div align="center">

# Vietnam Filmmaker Manager (VNFMM)

**Công cụ cài đặt, quản lý và sao lưu Plugin, Extension, Script, Preset & Color LUT dành cho người dựng phim.**

![Version](https://img.shields.io/badge/version-v1.0.0-7c6cff?style=flat-square)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS-1f232d?style=flat-square)
[![Website](https://img.shields.io/badge/website-films.vn-3ecf8e?style=flat-square)](https://films.vn)

[**Tải phiên bản mới nhất (v1.0.0)**](../../releases/latest) · [**Hướng dẫn nhanh**](#hướng-dẫn-sử-dụng-nhanh) · [**Câu hỏi thường gặp**](#câu-hỏi-thường-gặp) · [**Hỗ trợ**](#hỗ-trợ--liên-hệ)

<!-- Thay đường dẫn ảnh chụp giao diện thực tế vào đây -->
<!-- <img src="assets/preview.png" alt="Vietnam Filmmaker Manager" width="880" /> -->

</div>

---

## Tải về & Cài đặt

Tải bộ cài đặt chính thức tại mục **[Releases mới nhất](../../releases/latest)**:

| Hệ điều hành | Tệp cài đặt | Yêu cầu |
|---|---|---|
| **Windows (64-bit)** | `*.exe` hoặc `*.msi` | Windows 10 / 11 *(tự động kiểm tra và cài WebView2 Runtime nếu thiếu)* |
| **macOS** | `*.dmg` | macOS *(kéo ứng dụng vào thư mục `Applications`)* |

**Điều kiện sử dụng:**
- Có tài khoản thành viên tại **[films.vn](https://films.vn)**.
- Có kết nối mạng khi mở ứng dụng để xác thực phiên đăng nhập.

---

## Tính năng nổi bật

- **Kéo thả cài đặt thông minh:** Hỗ trợ thả tệp lẻ, thư mục bundle, hoặc nguyên thư mục chứa bộ LUT / MOGRT / Preset. Tự giữ nguyên cấu trúc thư mục con của từng bộ và tự tách các thư mục chứa nhiều loại tài nguyên khác nhau thành từng gói độc lập.
- **Tối ưu cho hệ sinh thái Adobe:**
  - Tự động bật chế độ Debug (`PlayerDebugMode`) cho extension `.zxp`.
  - Hỗ trợ cài `.zxp` và `.ccx` ngay cả khi máy **không cài Creative Cloud**.
  - Cài Script (`.jsx`, `.jsxbin`) và Preset (`.ffx`) cùng lúc vào **nhiều phiên bản After Effects**.
  - Tự nhận diện và cài/gỡ kèm thư mục tài nguyên đi kèm của script.
- **Quản lý toàn bộ gói trên máy:** Tự động quét cả gói cài qua VNFMM lẫn các plugin, extension, script, LUT đã cài sẵn từ trước. Lọc theo phần mềm và danh mục con, sắp xếp theo tên/thời gian/dung lượng, và tìm kiếm tới tận tên thư mục con.
- **Sao lưu & Chuyển máy nhanh (`.filmsbak`):**
  - Sao lưu 1 gói hoặc hàng loạt (tối đa 500 gói/lần), tùy chọn gộp thành 1 tệp hoặc tách từng tệp riêng.
  - Khôi phục toàn bộ hoặc tích chọn từng gói cần cài lại, tự tính lại thư mục đích theo máy mới (hỗ trợ chuyển chéo Windows ↔ macOS) kèm báo cáo kết quả chi tiết.
- **Tự động cập nhật:** Kiểm tra và cập nhật phiên bản mới trực tiếp trong ứng dụng (xác minh chữ ký trước khi cài).

---

## Định dạng hỗ trợ

| Nhóm | Định dạng |
|---|---|
| **Adobe** (Ae, Pr, Ps, Ai…) | `.zxp`, `.ccx`, `.jsx`, `.jsxbin`, `.aex`, `.plugin`, `.ffx`, `.mogrt` |
| **DaVinci Resolve** | `.ofx`, `.bundle` (`.ofx.bundle`), `.drfx`, `.dctl`, `.dctle`, `.fuse`, `.setting`, `.lua` |
| **Audio** | `.vst3`, `.vst`, `.component` *(chỉ macOS)*, `.aaxplugin`, `.aax` |
| **Color LUT** | `.cube`, `.3dl`, `.ilut` *(DaVinci Resolve & Adobe Lumetri Creative)* |
| **Sao lưu & Nén** | `.filmsbak`, `.zip` |

---

## Hướng dẫn sử dụng nhanh

1. **Đăng nhập:** Mở VNFMM → bấm **Đăng nhập qua trình duyệt** → đăng nhập tài khoản `films.vn` → quay lại ứng dụng.
2. **Cài gói:** Đóng các phần mềm dựng phim → kéo thả tệp hoặc thư mục vào cửa sổ VNFMM *(hoặc vào mục **Cài gói**, phím tắt `Ctrl/Cmd + O`)* → chọn phạm vi / phiên bản phần mềm đích → bấm **Cài đặt**.
3. **Sao lưu:** Bấm **Sao lưu** trên từng thẻ gói để lưu nhanh, hoặc vào mục **Sao lưu** ở thanh bên để chọn hàng loạt và xuất tệp `.filmsbak`.
4. **Khôi phục:** Kéo thả tệp `.filmsbak` vào ứng dụng, tích chọn các gói muốn khôi phục rồi bấm **Khôi phục**.

---

## Câu hỏi thường gặp

<details>
<summary><b>Windows: Tại sao khi bật quyền Admin lại không kéo thả tệp từ Explorer vào được?</b></summary>

Cơ chế bảo mật của Windows (UIPI) chặn thao tác kéo thả từ cửa sổ thường (File Explorer) vào ứng dụng đang chạy quyền Administrator. Khi đang ở chế độ Admin, hãy dùng nút **Chọn tệp cài đặt** hoặc **Chọn thư mục (Bundle)** trong mục **Cài gói**.
</details>

<details>
<summary><b>macOS: Cách xử lý khi cài plugin hệ thống hoặc mở ứng dụng lần đầu</b></summary>

- Bạn **không cần** chạy VNFMM bằng quyền root; khi cần ghi/xóa ở thư mục hệ thống, macOS sẽ tự hiện hộp thoại nhập mật khẩu hoặc Touch ID.
- Nếu lần đầu mở ứng dụng mà macOS báo ứng dụng từ nhà phát triển chưa xác định, hãy nhấp chuột phải vào biểu tượng VNFMM trong `Applications` → chọn **Open** (Mở), hoặc vào **System Settings → Privacy & Security → Open Anyway**.
</details>

<details>
<summary><b>Tại sao VNFMM không tìm thấy After Effects hoặc chưa hỗ trợ một số tệp?</b></summary>

- Ở phiên bản `v1.0.0`, VNFMM tự quét After Effects tại thư mục cài đặt mặc định (`C:\Program Files\Adobe` trên Windows và `/Applications` trên macOS).
- Preset Premiere `.prfpset` hiện chưa hỗ trợ cài qua VNFMM.
- Thư mục extension CEP/UXP chưa đóng gói cần được nén thành `.zxp` hoặc `.ccx` trước khi cài.
</details>

<details>
<summary><b>Đổi máy mới hoặc cần Reset thiết bị thì làm thế nào?</b></summary>

Mở **Cài đặt → Tài khoản & Thiết bị** trong VNFMM, bấm **Sao chép** tại dòng **Mã thiết bị** (và **Sao chép nhật ký** nếu cần báo lỗi — toàn bộ đường dẫn cá nhân đã được tự động che ẩn), sau đó gửi cho đội ngũ hỗ trợ của `films.vn`.
</details>

---

## Hỗ trợ & Liên hệ

- **Trang chủ:** [films.vn](https://films.vn)

---

<div align="center">
<sub>© 2026 Vietnam Filmmaker (films.vn). Bảo lưu mọi quyền.</sub>
</div>
