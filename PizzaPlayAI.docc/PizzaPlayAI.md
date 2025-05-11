@Article

# 🍕 Neighbourhood Pizza App Overview

Welcome to the **Neighbourhood Pizza App**! This documentation gives you an overview of the project, key components, and how it all works together.

## Roles in the App

- **Buyers**: Order and customise pizzas, gift to others, engage socially.
- **Bakers**: Set working hours, manage orders, send updates.
- **Admin (planned)**: Manage users, content, and fees.

## Features Implemented

- Drag pizza into baby dragon’s mouth (welcome screen)
- Multi-step pizza builder (toppings, quantity, schedule, pay)
- Firebase + Apple Pay integration
- Social feed with gifting and invites
- Baker dashboard with orders, availability, and messages

## Core SwiftUI Views

- ``WelcomeView``
- ``PizzaCreationView``
- ``PaymentView``
- ``SocialMediaView``
- ``BakerDashboardView``

## Data Models

- ``PizzaOrder``
- ``PizzaIngredient``

## Architecture

- **UI:** SwiftUI
- **Backend:** Firebase Firestore + Apple Pay (stub)
- **State:** `@StateObject`, `@Binding`, `@AppStorage`
- **Navigation:** `NavigationStack`

## Next Steps

- Admin dashboard
- Pizza imagery
- Review system for bakers
- Real-time baker availability
