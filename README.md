# 🚚 Driver Delivery App - Flutter Mobile Application

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev/)
[![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/)
[![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)](https://firebase.google.com/)
[![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://developer.android.com/)
[![iOS](https://img.shields.io/badge/iOS-000000?style=for-the-badge&logo=ios&logoColor=white)](https://developer.apple.com/ios/)

## 📱 Tổng quan dự án

Ứng dụng di động Flutter dành cho tài xế giao hàng với hệ thống quản lý đơn hàng toàn diện, theo dõi vị trí real-time và tích hợp đầy đủ các dịch vụ Firebase. Ứng dụng hỗ trợ đầy đủ quy trình từ đăng ký, xác thực đến quản lý đơn hàng và thống kê doanh thu.

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

### 🗺️ Theo dõi vị trí Real-time
- **GPS Tracking**: Độ chính xác cao với Geolocator
- **Firebase Realtime**: Cập nhật vị trí mỗi 2 giây
- **Background Service**: Tracking ngay cả khi app ở background
- **Bản đồ tương tác**: Hiển thị vị trí hiện tại với Flutter Map

### 📊 Thống kê và báo cáo
- **Thống kê doanh thu**: Theo ngày/tuần/tháng
- **Lịch sử giao hàng**: Chi tiết các chuyến giao
- **Báo cáo hiệu suất**: Metrics và KPI cho tài xế
- **Dashboard**: Giao diện trực quan với charts

### 🔔 Thông báo Push
- **FCM Integration**: Firebase Cloud Messaging
- **Thông báo đơn hàng**: Nhận đơn mới real-time
- **Cập nhật trạng thái**: Thông báo thay đổi trạng thái đơn
- **Quản lý token**: Auto-refresh FCM tokens

### 🛠️ Tính năng bổ sung
- **Chia sẻ chuyến đi**: Share trip với người thân
- **Mời bạn bè**: Referral system
- **Chứng minh giao hàng**: Chụp ảnh xác nhận
- **Cài đặt**: Preferences và configuration

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

## 🚀 Cài đặt và chạy dự án

### Yêu cầu hệ thống
- Flutter SDK 3.2.3+
- Dart 3.0+
- Android Studio / VS Code
- Android SDK / Xcode (cho iOS)

### Cài đặt dependencies
```bash
flutter pub get
```

### Cấu hình Firebase
1. Tạo project Firebase
2. Thêm `google-services.json` (Android) và `GoogleService-Info.plist` (iOS)
3. Cấu hình Firebase services:
   - Realtime Database
   - Cloud Firestore
   - Cloud Storage
   - Cloud Messaging

### Chạy ứng dụng
```bash
# Debug mode
flutter run

# Release mode
flutter run --release

# Specific platform
flutter run -d android
flutter run -d ios
```

## 📱 Screenshots

| Authentication | Home Screen | Orders Management |
|----------------|-------------|-------------------|
| ![Auth](assets/screenshots/auth.png) | ![Home](assets/screenshots/home.png) | ![Orders](assets/screenshots/orders.png) |

| Location Tracking | Statistics | Profile Management |
|-------------------|------------|-------------------|
| ![Location](assets/screenshots/location.png) | ![Stats](assets/screenshots/stats.png) | ![Profile](assets/screenshots/profile.png) |

## 🔧 Cấu hình API

Cập nhật API endpoints trong `lib/config/app_config.dart`:

```dart
class AppConfig {
  static const String baseUrl = 'YOUR_API_BASE_URL';
  // ... other configurations
}
```

## 📊 Performance & Optimization

- **Background Services**: Efficient location tracking
- **Memory Management**: Optimized image loading và caching
- **Network**: Retry mechanisms và offline support
- **Battery**: Optimized GPS usage
- **UI**: Smooth animations và responsive design

## 🧪 Testing

```bash
# Unit tests
flutter test

# Integration tests
flutter test integration_test/

# Coverage report
flutter test --coverage
```

## 📈 Metrics & Analytics

- **Crash Reporting**: Firebase Crashlytics
- **Performance**: Firebase Performance Monitoring
- **Analytics**: Firebase Analytics
- **Custom Events**: User behavior tracking

## 🔒 Bảo mật

- **Data Encryption**: Sensitive data encryption
- **API Security**: JWT token validation
- **File Upload**: Secure file handling
- **Location Privacy**: User consent management

## 🌐 Đa nền tảng

- ✅ **Android**: API 21+ (Android 5.0+)
- ✅ **iOS**: iOS 11.0+
- 🔄 **Web**: In development
- 🔄 **Desktop**: Planned

## 📝 Changelog

### v1.0.0 (Current)
- ✅ Complete authentication system
- ✅ Order management
- ✅ Real-time location tracking
- ✅ Firebase integration
- ✅ Push notifications
- ✅ Statistics dashboard

## 🤝 Contributing

1. Fork the project
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Developer

**Công Tình**
- GitHub: [@congtinh](https://github.com/congtinh)
- LinkedIn: [Công Tình](https://linkedin.com/in/congtinh)
- Email: congtinh@example.com

## 🙏 Acknowledgments

- Flutter team for the amazing framework
- Firebase team for backend services
- Open source community for packages
- Contributors and testers

---

⭐ **Star this repository if you found it helpful!**

📱 **Download the app and experience the smooth delivery management!**