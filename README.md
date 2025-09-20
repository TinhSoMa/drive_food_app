# 🚚 Ứng Dụng Tài Xế Giao Hàng - Flutter Mobile App

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev/)
[![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/)
[![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)](https://firebase.google.com/)
[![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://developer.android.com/)
[![iOS](https://img.shields.io/badge/iOS-000000?style=for-the-badge&logo=ios&logoColor=white)](https://developer.apple.com/ios/)

## 📱 Giới thiệu dự án

Ứng dụng di động Flutter dành cho tài xế giao hàng với hệ thống quản lý đơn hàng toàn diện, theo dõi vị trí thời gian thực và tích hợp đầy đủ các dịch vụ Firebase. Ứng dụng hỗ trợ đầy đủ quy trình từ đăng ký, xác thực đến quản lý đơn hàng và thống kê doanh thu.

## ✨ Tính năng chính

### 🔐 Hệ thống xác thực
- **Đăng ký/Đăng nhập**: Xác thực bằng số điện thoại + OTP
- **Đăng nhập mật khẩu**: Hỗ trợ đăng nhập bằng mật khẩu
- **Quản lý session**: JWT token management và auto-refresh
- **Bảo mật**: Đặt/đổi mật khẩu với validation

### 👤 Quản lý hồ sơ tài xế
- **Upload tài liệu**: CMND, GPLX, đăng ký xe, bảo hiểm
- **Xác minh tài liệu**: Hệ thống kiểm tra và xác minh tự động
- **Cập nhật thông tin**: Profile management với validation
- **Trạng thái xác minh**: Theo dõi tiến độ hoàn thiện hồ sơ

### 📦 Hệ thống đơn hàng
- **Quản lý đơn hàng**: Xem theo trạng thái (chờ, đang giao, hoàn thành, hủy)
- **Nhận/Từ chối đơn**: Xử lý đơn hàng với lý do từ chối
- **Chi tiết đơn hàng**: Thông tin khách hàng, địa chỉ, sản phẩm
- **Tích hợp Maps**: Điều hướng với Google Maps API

### 🗺️ Theo dõi vị trí thời gian thực
- **GPS Tracking**: Độ chính xác cao với Geolocator
- **Firebase Realtime**: Cập nhật vị trí mỗi 2 giây
- **Dịch vụ nền**: Tracking ngay cả khi app ở chế độ nền
- **Bản đồ tương tác**: Hiển thị vị trí hiện tại với Flutter Map

### 📊 Thống kê và báo cáo
- **Thống kê doanh thu**: Theo ngày/tuần/tháng
- **Lịch sử giao hàng**: Chi tiết các chuyến giao
- **Báo cáo hiệu suất**: Metrics và KPI cho tài xế
- **Dashboard**: Giao diện trực quan với charts

### 🔔 Thông báo đẩy
- **Tích hợp FCM**: Firebase Cloud Messaging
- **Thông báo đơn hàng**: Nhận đơn mới thời gian thực
- **Cập nhật trạng thái**: Thông báo thay đổi trạng thái đơn
- **Quản lý token**: Tự động làm mới FCM tokens

### 🛠️ Tính năng bổ sung
- **Chia sẻ chuyến đi**: Chia sẻ chuyến đi với người thân
- **Mời bạn bè**: Hệ thống giới thiệu
- **Chứng minh giao hàng**: Chụp ảnh xác nhận
- **Cài đặt**: Tùy chọn và cấu hình

## 🏗️ Kiến trúc và Công nghệ

### Frontend
- **Framework**: Flutter 3.2.3+
- **Language**: Dart
- **State Management**: Provider Pattern
- **UI/UX**: Material Design 3
- **Maps**: Flutter Map + Google Maps API

### Backend Integration
- **API**: RESTful API với HTTP Client
- **Authentication**: JWT Token + OTP
- **File Upload**: Firebase Storage
- **Real-time**: Firebase Realtime Database

### Database & Storage
- **Real-time DB**: Firebase Realtime Database
- **NoSQL**: Cloud Firestore
- **Local Storage**: SharedPreferences
- **File Storage**: Firebase Storage

### Services & Integrations
- **Location**: Geolocator + GPS
- **Push Notifications**: Firebase Cloud Messaging
- **Background**: Flutter Background Service
- **Maps**: Google Maps + Flutter Map
- **Image**: Image Picker + Firebase Storage

## 📁 Cấu trúc dự án

```
lib/
├── config/           # Cấu hình ứng dụng
├── models/           # Data models và entities
├── providers/        # State management (Provider)
├── screens/          # UI screens và pages
│   ├── auth/        # Authentication screens
│   └── home/        # Main app screens
├── services/         # Business logic và API services
├── utils/           # Utilities và helpers
├── widgets/         # Reusable UI components
└── main.dart        # Entry point
```

## 🚀 Hướng dẫn cài đặt và chạy dự án

### Yêu cầu hệ thống
- Flutter SDK 3.2.3+
- Dart 3.0+
- Android Studio / VS Code
- Android SDK / Xcode (cho iOS)

### Cài đặt thư viện
```bash
flutter pub get
```

### Cấu hình Firebase
1. Tạo dự án Firebase
2. Thêm `google-services.json` (Android) và `GoogleService-Info.plist` (iOS)
3. Cấu hình các dịch vụ Firebase:
   - Realtime Database
   - Cloud Firestore
   - Cloud Storage
   - Cloud Messaging

### Chạy ứng dụng
```bash
# Chế độ debug
flutter run

# Chế độ release
flutter run --release

# Nền tảng cụ thể
flutter run -d android
flutter run -d ios
```

## 📱 Hình ảnh ứng dụng

| Xác thực | Màn hình chính | Quản lý đơn hàng |
|----------|----------------|------------------|
| ![Auth](assets/screenshots/auth.png) | ![Home](assets/screenshots/home.png) | ![Orders](assets/screenshots/orders.png) |

| Theo dõi vị trí | Thống kê | Quản lý hồ sơ |
|-----------------|----------|---------------|
| ![Location](assets/screenshots/location.png) | ![Stats](assets/screenshots/stats.png) | ![Profile](assets/screenshots/profile.png) |

## 🔧 Cấu hình API

Cập nhật API endpoints trong `lib/config/app_config.dart`:

```dart
class AppConfig {
  static const String baseUrl = 'YOUR_API_BASE_URL';
  // ... other configurations
}
```

## 📊 Hiệu suất và Tối ưu hóa

- **Dịch vụ nền**: Theo dõi vị trí hiệu quả
- **Quản lý bộ nhớ**: Tối ưu hóa tải và lưu trữ hình ảnh
- **Mạng**: Cơ chế thử lại và hỗ trợ offline
- **Pin**: Sử dụng GPS được tối ưu hóa
- **Giao diện**: Animation mượt mà và thiết kế responsive

## 🧪 Kiểm thử

```bash
# Unit tests
flutter test

# Integration tests
flutter test integration_test/

# Báo cáo coverage
flutter test --coverage
```

## 📈 Thống kê và Phân tích

- **Báo cáo lỗi**: Firebase Crashlytics
- **Hiệu suất**: Firebase Performance Monitoring
- **Phân tích**: Firebase Analytics
- **Sự kiện tùy chỉnh**: Theo dõi hành vi người dùng

## 🔒 Bảo mật

- **Mã hóa dữ liệu**: Mã hóa dữ liệu nhạy cảm
- **Bảo mật API**: Xác thực JWT token
- **Tải file**: Xử lý file an toàn
- **Quyền riêng tư vị trí**: Quản lý sự đồng ý của người dùng

## 🌐 Đa nền tảng

- ✅ **Android**: API 21+ (Android 5.0+)
- ✅ **iOS**: iOS 11.0+
- 🔄 **Web**: Đang phát triển
- 🔄 **Desktop**: Dự kiến

## 📝 Lịch sử phiên bản

### v1.0.0 (Hiện tại)
- ✅ Hệ thống xác thực hoàn chỉnh
- ✅ Quản lý đơn hàng
- ✅ Theo dõi vị trí thời gian thực
- ✅ Tích hợp Firebase
- ✅ Thông báo đẩy
- ✅ Bảng điều khiển thống kê

## 🤝 Đóng góp

1. Fork dự án
2. Tạo nhánh tính năng (`git checkout -b feature/TinhNangMoi`)
3. Commit thay đổi (`git commit -m 'Thêm tính năng mới'`)
4. Push lên nhánh (`git push origin feature/TinhNangMoi`)
5. Tạo Pull Request


## 👨‍💻 Developer

**Công Tình**
- GitHub: [@congtinh](https://github.com/TinhSoMa)
- Email: congtinh06032003@gmail.com

## 🙏 Lời cảm ơn

- Đội ngũ Flutter vì framework tuyệt vời
- Đội ngũ Firebase vì các dịch vụ backend
- Cộng đồng mã nguồn mở vì các package
- Các nhà đóng góp và người kiểm thử

---

⭐ **Hãy star repository này nếu bạn thấy hữu ích!**

📱 **Tải ứng dụng và trải nghiệm quản lý giao hàng mượt mà!**