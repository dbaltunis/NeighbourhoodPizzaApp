
# 🍕 Neighbourhood Pizza App Documentation

## 🧑‍🍳 App Roles

| Role | Key Abilities |
| ---- | ------------- |
| **Buyer** | Logs in as a client, uploads profile image, creates name or nickname, orders pizza by selecting toppings and quantity, schedules pickup, pays, gifts pizza, and engages in the social feed. |
| **Baker** | Manages working hours, creates pizza offerings, views and accepts/rejects orders, sets toppings and prices, sends updates, communicates with clients, and tracks profits. |
| **Admin** | Manages all users and bakers, monitors content and fee settings, manages pizza offerings, and tracks KPIs such as sales, orders, profits, and user activity. |

---

## 📲 Buyer Workflow

### WelcomeView
- Animated intro (e.g., drag pizza to dragon)
- Buttons: “Order Pizza”, “Login as a Baker”
- Background: Pizza-themed design

### PizzaCreationView
1. Map view with slice pins for baker locations
2. Search/filter input
3. Choose daily menu OR select baker
4. View bakers within 30km (glowing markers)
5. Choose pizza → drag & drop toppings
6. Select quantity
7. Schedule pickup (calendar + slot)
   - If unavailable, show fallback message
8. Pay via Apple Pay or Stripe
9. Confirmation screen with “Back to Feed” CTA

### SocialMediaView
- Feed of posts (text/images)
- Floating +: “Upload Photo”, “Invite a Friend or Neighbour”
- “Send Pizza” → Choose recipient, time, pay

---

## 📲 Baker Workflow

### BakerDashboardView
- Set working hours and availability
- Manage orders (accept/reject)
- Update toppings and pricing
- View profits and sales analytics
- Message clients directly or broadcast

---

## 🛠 Architecture Overview

| Component      | Tech Stack / Detail                         |
| -------------- | ------------------------------------------- |
| **UI**         | SwiftUI                                     |
| **Backend**    | Firebase Firestore                          |
| **Payments**   | Apple Pay / Stripe                          |
| **State Mgmt** | @StateObject, @Binding, @AppStorage         |
| **Navigation** | NavigationStack                             |

---

## 🧱 Core SwiftUI Views

- WelcomeView
- PizzaCreationView
- PaymentView
- SocialMediaView
- BakerDashboardView

---

## 📦 Data Models (Example)

```swift
struct PizzaIngredient: Identifiable {
    var id: String
    var name: String
    var image: String
    var isSelected: Bool
}

struct PizzaOrder: Identifiable {
    var id: String
    var buyerId: String
    var bakerId: String
    var ingredients: [PizzaIngredient]
    var quantity: Int
    var pickupDate: Date
    var paymentStatus: String
}

struct Baker: Identifiable {
    var id: String
    var name: String
    var location: GeoPoint
    var isOnline: Bool
    var availableToppings: [PizzaIngredient]
    var schedule: [String: [Date]]
}

struct SocialPost: Identifiable {
    var id: String
    var authorId: String
    var content: String
    var imageUrl: String?
    var timestamp: Date
}
```

---

## 🧼 Development Roadmap

- Admin Dashboard (SwiftUI or Web)
- Real-time pizza imagery updates
- Baker review & rating system
- Live baker availability with booking
- Map view with filterable baker pins
- Smooth animations and UX improvements
- Fallback message when no baker is available
---
git init
git add .
git commit -m "Initial commit with app documentation"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/neighbourhood-pizza-app.git
git push -u origin main
