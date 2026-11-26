# Sổ thông tin – Android project

Project Android dùng WebView để chạy giao diện Sổ thông tin từ file HTML gốc.

## Tạo APK bằng điện thoại (không cần Android Studio)

Project có sẵn GitHub Actions để biên dịch APK trên máy chủ GitHub.

1. Trên điện thoại, mở github.com và đăng nhập hoặc tạo tài khoản.
2. Tạo repository mới (chọn **Public** để dùng GitHub Actions miễn phí dễ nhất).
3. Giải nén ZIP này trên điện thoại. Tải toàn bộ nội dung bên trong thư mục `SoThongTinAndroid` lên repository, giữ nguyên cấu trúc thư mục và cả thư mục ẩn `.github`.
4. Mở tab **Actions**, chọn **Build Android APK**, rồi bấm **Run workflow** nếu workflow chưa tự chạy.
5. Khi chạy xong, mở lần chạy mới nhất ở tab Actions. Ở cuối trang **Artifacts**, tải `SoThongTin-debug-apk`.
6. Giải nén file artifact đã tải để lấy `app-debug.apk`, mở file APK và làm theo hướng dẫn Android để cài đặt. Android có thể yêu cầu cho phép cài ứng dụng từ nguồn này.

## Tạo APK bằng Android Studio

1. Mở thư mục `SoThongTinAndroid` bằng Android Studio.
2. Chờ Gradle Sync hoàn tất.
3. Chọn **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
4. APK debug nằm tại `app/build/outputs/apk/debug/app-debug.apk`.

## Ghi chú

- Đây là APK debug để cài thử, chưa phải bản phát hành Play Store.
- Dữ liệu hiện được lưu bằng localStorage trên thiết bị. Gỡ ứng dụng hoặc xóa dữ liệu ứng dụng có thể làm mất dữ liệu.
- Bản đồ vệ tinh và thư viện bản đồ cần Internet.
- Chỉ cấp quyền vị trí nếu muốn dùng tính năng định vị trên bản đồ.
