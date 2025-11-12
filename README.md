# 🏥 Healthcare Application

A comprehensive Android healthcare application that provides users with easy access to medical services, including doctor appointments, lab tests, medicine purchases, and health articles.

![Android](https://img.shields.io/badge/Platform-Android-green.svg)
![Java](https://img.shields.io/badge/Language-Java-orange.svg)
![SQLite](https://img.shields.io/badge/Database-SQLite-blue.svg)
![Min SDK](https://img.shields.io/badge/Min%20SDK-21-blue.svg)
![Target SDK](https://img.shields.io/badge/Target%20SDK-34-blue.svg)

## 📋 Table of Contents

- [Features](#-features)
- [Technologies Used](#-technologies-used)
- [Installation](#-installation)
- [Project Structure](#-project-structure)
- [Database Schema](#-database-schema)
- [Usage](#-usage)
- [Screenshots](#-screenshots)
- [Contributing](#-contributing)
- [License](#-license)

## ✨ Features

### 🔐 User Authentication
- **User Registration**: Create a new account with username, email, and password
- **User Login**: Secure login with credentials validation
- **Session Management**: Persistent login sessions using SharedPreferences

### 👨‍⚕️ Find Doctors
- Browse doctors by specialty:
  - Family Physicians
  - Dietician
  - Dentist
  - Surgeon
  - Cardiologists
- View doctor details
- Book appointments with selected doctors

### 🧪 Lab Tests
- Browse available lab tests
- View detailed test information
- Add tests to cart
- Book lab tests with delivery details

### 💊 Buy Medicine
- Browse available medicines
- View medicine details and pricing
- Add medicines to cart
- Complete purchase with delivery information

### 📰 Health Articles
- Access health-related articles
- Read detailed article content
- Stay informed about health and wellness

### 🛒 Shopping Cart
- Add lab tests and medicines to cart
- Manage cart items
- Calculate total prices
- Complete orders

### 📦 Order Management
- View order history
- Track order details
- Manage appointments

## 🛠 Technologies Used

- **Language**: Java
- **Platform**: Android
- **Database**: SQLite
- **UI Components**: 
  - Material Design Components
  - CardView
  - ConstraintLayout
- **Architecture**: Standard Android Activities
- **Build Tool**: Gradle (Kotlin DSL)
- **Minimum SDK**: 21 (Android 5.0 Lollipop)
- **Target SDK**: 34 (Android 14)
- **Compile SDK**: 34

## 📦 Installation

### Prerequisites

- Android Studio (Arctic Fox or later)
- JDK 8 or higher
- Android SDK with API level 21 or higher
- Git

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/rishit911/Healthcare_Project.git
   cd Healthcare_Project
   ```

2. **Open in Android Studio**
   - Open Android Studio
   - Select "Open an existing Android Studio project"
   - Navigate to the cloned directory and select it

3. **Sync Gradle**
   - Android Studio will automatically sync Gradle
   - Wait for the sync to complete

4. **Run the application**
   - Connect an Android device or start an emulator
   - Click the "Run" button or press `Shift + F10`
   - Select your device/emulator
   - The app will install and launch

### Building from Command Line

```bash
# Windows
gradlew.bat assembleDebug

# Linux/Mac
./gradlew assembleDebug
```

The APK will be generated at: `app/build/outputs/apk/debug/app-debug.apk`

## 📁 Project Structure

```
Healthcare_Project/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/healthcare/
│   │   │   │   ├── MainActivity.java
│   │   │   │   ├── loginActivity.java
│   │   │   │   ├── RegisterActivity.java
│   │   │   │   ├── HomeActivity.java
│   │   │   │   ├── FindDoctorActivity.java
│   │   │   │   ├── DoctorDetailsActivity.java
│   │   │   │   ├── BookAppointmentActivity.java
│   │   │   │   ├── LabTestActivity.java
│   │   │   │   ├── LabTestDetailsActivity.java
│   │   │   │   ├── LabTestBookActivity.java
│   │   │   │   ├── CartLabActivity.java
│   │   │   │   ├── BuyMedicineActivity.java
│   │   │   │   ├── BuyMedicineDetailsActivity.java
│   │   │   │   ├── BuyMedicineBookActivity.java
│   │   │   │   ├── CartBuyMedicineActivity.java
│   │   │   │   ├── OrderDetailsActivity.java
│   │   │   │   ├── HealthArticlesActivity.java
│   │   │   │   ├── HealthArticlesDetailsActivity.java
│   │   │   │   └── database.java
│   │   │   ├── res/
│   │   │   │   ├── layout/          # XML layout files
│   │   │   │   ├── drawable/        # Images and drawables
│   │   │   │   ├── values/          # Strings, colors, themes
│   │   │   │   └── mipmap/          # App icons
│   │   │   └── AndroidManifest.xml
│   │   └── test/                    # Unit tests
│   └── build.gradle.kts
├── build.gradle.kts
├── settings.gradle.kts
└── gradle/
    └── wrapper/
```

## 🗄 Database Schema

The application uses SQLite database with the following tables:

### Users Table
```sql
CREATE TABLE users(
    username TEXT,
    email TEXT,
    password TEXT
)
```

### Cart Table
```sql
CREATE TABLE cart(
    username TEXT,
    product TEXT,
    price REAL,
    otype TEXT
)
```

### Orders Table
```sql
CREATE TABLE orderplace(
    username TEXT,
    fullname TEXT,
    address TEXT,
    contactno TEXT,
    pincode INTEGER,
    date TEXT,
    time TEXT,
    amount REAL,
    otype TEXT
)
```

## 📱 Usage

### 1. Registration
- Launch the app
- Click on "Register" if you're a new user
- Enter your username, email, and password
- Complete registration

### 2. Login
- Enter your username and password
- Click "Login" to access the home screen

### 3. Find Doctor
- Navigate to "Find Doctor" from the home screen
- Select a doctor specialty
- View doctor details
- Book an appointment by filling in your details

### 4. Lab Tests
- Go to "Lab Test" from the home screen
- Browse available tests
- View test details
- Add tests to cart
- Complete booking with delivery details

### 5. Buy Medicine
- Access "Buy Medicine" from the home screen
- Browse available medicines
- View medicine details
- Add to cart
- Complete purchase

### 6. Health Articles
- Navigate to "Health Articles"
- Browse available articles
- Read detailed content

### 7. Order Details
- View your order history
- Track appointments and purchases

## 📸 Screenshots

> **Note**: Add screenshots of your application here to showcase the UI/UX

### Login Screen
![Login Screen](screenshots/login.png)

### Home Screen
![Home Screen](screenshots/home.png)

### Find Doctor
![Find Doctor](screenshots/find_doctor.png)

### Lab Tests
![Lab Tests](screenshots/lab_tests.png)

### Buy Medicine
![Buy Medicine](screenshots/buy_medicine.png)

## 🔮 Future Enhancements

- [ ] Add doctor search functionality
- [ ] Implement payment gateway integration
- [ ] Add push notifications for appointments
- [ ] Integrate telemedicine features
- [ ] Add user profile management
- [ ] Implement appointment reminders
- [ ] Add prescription management
- [ ] Integrate with medical record systems
- [ ] Add multi-language support
- [ ] Implement dark mode theme
- [ ] Add biometric authentication
- [ ] Integrate with wearable devices

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Rishit**

- GitHub: [@rishit911](https://github.com/rishit911)

## 🙏 Acknowledgments

- Material Design Components
- Android Open Source Project
- SQLite Database

## 📞 Support

For support, email support@healthcareapp.com or create an issue in the repository.

---

⭐ If you found this project helpful, please give it a star!

