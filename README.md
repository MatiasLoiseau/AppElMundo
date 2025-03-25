# AppChat

AppChat is an Android application that allows users to create posts with images, comment on others' posts, and manage their own profiles. The app uses Parse Server (Back4App) as the backend for user authentication, data storage, and image hosting.

---

## Technologies Used

- **Java (Android)**
- **Parse SDK (Back4App)**
- **Glide / Picasso** for image loading
- **MVVM Architecture** with ViewModel + LiveData
- **ViewPager2** for image sliders
- **RecyclerView** for dynamic content
- **Bottom Navigation View**
- **DataBinding + XML layouts**

---
      
## Features

### Authentication
- User registration with email and password
- Login with input validation
- Logout functionality

### Posts
- Create posts with title, description, category, duration, and budget
- Upload up to 3 images per post (stored on Parse)
- View post details with image gallery and metadata

### Comments
- Add and view comments on posts
- Comments are linked to users and specific posts

### Image Uploads
- Select images from the device gallery
- Display images in a slider or grid

### Navigation
- Bottom navigation with tabs: Home, Chats, Filters, Profile

---

## Architecture

The app follows the **MVVM** pattern:

- **View**: Activities and Fragments handle UI
- **ViewModel**: Contains UI logic and exposes LiveData
- **Model**: ParseObject subclasses (User, Post, Comment)
- **Providers**: Business logic and communication with Parse (e.g. `AuthProvider`, `PostProvider`)
- **Adapters**: Custom RecyclerView adapters for displaying data

---

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/appchat.git
   ```

2. Open the project in **Android Studio**

3. Configure your `res/values/strings.xml` with your Back4App credentials:
   ```xml
   <string name="back4app_app_id">YOUR_APP_ID</string>
   <string name="back4app_client_key">YOUR_CLIENT_KEY</string>
   <string name="back4app_server_url">https://parseapi.back4app.com/</string>
   ```

4. Run the app on an emulator or physical device

---

## Required Permissions

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.READ_MEDIA_IMAGES" />
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
```
