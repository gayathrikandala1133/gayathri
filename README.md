```
# Flutter Product Listing App

This Flutter application demonstrates a product listing app fetching data from dummyjson.com/products, showcasing modern Flutter development practices.

## Technologies Used

*   Flutter (latest stable)
*   Dio for HTTP client
*   GoRouter for routing
*   Riverpod for state management

## Project Structure

```
lib/
├── main.dart
├── app_router.dart
├── models/
│   └── product.dart
├── services/
│   └── product_service.dart
├── providers/
│   └── product_provider.dart
├── screens/
│   ├── product_list_screen.dart
│   └── product_detail_screen.dart
├── widgets/
│   ├── product_card.dart
│   ├── loading_indicator.dart
│   └── error_message.dart
└── utils/
    └── constants.dart
```

## Core Features

### 1. Navigation & Routing (GoRouter)

*   `app_router.dart`: Defines routes using `GoRouter`.
*   Route guards are not strictly implemented in this example for simplicity, but can easily be added using GoRouter's `redirect` functionality based on authentication status.

### 2. API Integration (Dio)

*   `product_service.dart`: Handles API calls to dummyjson.com/products using Dio.
*   Error handling is implemented using try-catch blocks and custom exceptions.
*   Loading and error states are managed using Riverpod's `AsyncValue`.

### 3. UI Components

*   `product_list_screen.dart`: Displays products in a Grid or List view (toggleable). Implements pull-to-refresh using `RefreshIndicator`.
*   `product_detail_screen.dart`: Shows detailed product information with an expandable description. Includes a share button (basic implementation).
*   `product_card.dart`: Reusable widget for displaying a product in the list/grid.
*   `loading_indicator.dart`: Displays a circular progress indicator.
*   `error_message.dart`: Displays an error message.

### 4. State Management (Riverpod)

*   `product_provider.dart`: Manages the product list using `StateNotifierProvider` and `AsyncValue`. Handles API calls and state updates.
*   `product_list_screen.dart` and `product_detail_screen.dart` consume the state using `ConsumerWidget` and `ref.watch`.

## Screens

### 1. Product List Screen

*   Displays products in a grid or list view.
*   Implements pull-to-refresh.
*   Includes a toggle to switch between grid and list views.
*   Basic filtering (search) can be implemented by filtering the product list in the provider based on user input.

### 2. Product Detail Screen

*   Displays detailed product information.
*   Includes an expandable description.
*   Implements a share button (basic functionality).

## Evaluation Focus Areas

### 1. Code Architecture

*   Clean code structure with separation of concerns.
*   Effective use of Riverpod for state management.
*   Robust API integration with error handling.
*   Clear route management with GoRouter.

### 2. UI Implementation

*   Well-organized widgets and responsive layout.
*   Clear loading and error states.
*   User-friendly UI.

### 3. Best Practices

*   Code organization and readability.
*   Proper error handling.
*   Use of constants for hardcoded values.
*   Reusable widgets.

## Further Improvements

*   Implement proper authentication and route guards.
*   Add more advanced filtering and sorting.
*   Implement a more robust sharing feature.
*   Write unit and widget tests.
*   Improve UI/UX.

## Installation

1.  Clone the repository.
2.  Run `flutter pub get` to install dependencies.
3.  Run `flutter run` to start the app.

## Note

This is a simplified example to demonstrate the core concepts.
