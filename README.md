# 🛒 LocalStoreProject (Local Market App)

A full-stack iOS application developed using SwiftUI and Firebase, designed to connect local vendors with customers. The application includes separate authentication flows for customers and vendors, product management, interactive maps, and a complete shopping and checkout experience.

## 📦 Technologies

- **Language:** Swift
- **UI Framework:** SwiftUI
- **Local Storage:** Core Data for offline caching and faster data loading
- **Backend:** Firebase Authentication, Cloud Firestore, and Firebase Storage
- **Maps & Location:** MapKit and CoreLocation
- **Image Loading:** SDWebImageSwiftUI
- **Architecture:** MVVM using ObservableObject data managers such as `AuthManager`, `ProductHolder`, `CartHolder`, and `OrderHolder`

## ⚙️ Features

- **Authentication:** Separate registration and login flows for customers and vendors.
- **Product Management:** Vendors can create, edit, and delete products, including uploading product images to Firebase Storage.
- **Shopping Cart & Checkout:** Customers can add products to their cart, manage quantities, and place orders through Firestore.
- **Estimated Delivery Time:** Calculates the estimated delivery time based on the distance between the customer's address and the vendor's location.
- **Interactive Maps:**
  - Displays local vendors on a map using custom annotations.
  - Includes a custom MapKit address picker to search for and save addresses.
- **Order Management:** Customers can access their order history, while vendors can manage incoming orders and update their statuses.
- **Profile Management:** Customers and vendors can edit their profiles and upload profile pictures.

## 🧑‍🍳 The Process

I divided the development process into several stages, focusing on implementing the different features while keeping the frontend and backend properly connected.

1. **Project Setup:** Defined the Core Data models for users, vendors, products, and orders, and configured Firebase in the application.
2. **Authentication & Backend:** Implemented the authentication system and created custom managers to synchronize user information between Firebase Authentication, Core Data, and Firestore. This also allowed the application to distinguish between customer and vendor accounts.
3. **Product Management:** Developed the product creation and editing flows, integrating `PhotosPicker` and Firebase Storage to upload product images.
4. **State Management:** Created custom `ObservableObject` classes to manage carts, products, and orders while keeping the interface responsive.
5. **MapKit Integration:** Implemented the map view and custom address picker, allowing users to visualize vendor locations and select their current address using CoreLocation.
6. **Final Improvements:** Added error handling, loading states, notifications, and synchronization between Core Data and Firestore to improve the overall experience and support offline data access.

## 🧠 What I Learnt

- **Core Data & Firestore:** Improved my understanding of local data persistence and cloud synchronization, particularly when managing data between Core Data and Firestore.
- **SwiftUI State Management:** Gained more experience with `@StateObject`, `@EnvironmentObject`, and sharing data between multiple views.
- **Asynchronous Programming:** Worked with completion handlers, `DispatchGroup`, and Firebase callbacks to manage asynchronous operations without blocking the UI.
- **MapKit Integration:** Learned how to implement custom map annotations, manage camera positions, and use `MKLocalSearch` to convert addresses into geographical coordinates.
- **Data Security:** Better understood how to use Firebase UIDs and Firestore rules to restrict access to user-specific data and prevent unauthorized modifications.

## ☁️ How It Can Be Improved

- **Payment Integration:** Integrate Stripe or Apple Pay to replace the current simulated checkout process.
- **Real-time Messaging:** Allow customers and vendors to communicate directly about products and orders.
- **Push Notifications:** Notify vendors when new orders are placed and customers when their order status changes.
- **Pagination:** Improve performance by loading products and order history progressively.
- **Rating System:** Allow customers to rate vendors and leave reviews after completing an order.

## 🚥 Running the Project

1. Clone the repository.
2. Open `LocalStoreProject.xcworkspace`.
3. Make sure the Firebase dependencies are installed and configured.
4. Add the required `GoogleService-Info.plist` file to the project.
5. Select an iOS Simulator and run the application using `Cmd + R`.
6. To test the complete workflow, create two accounts: one **Vendor** account to publish products and one **Customer** account to browse and purchase them.

## 🎥 Video Demonstration
https://github.com/user-attachments/assets/ccaf6338-dff6-481a-8c64-a2a172f85ae8
