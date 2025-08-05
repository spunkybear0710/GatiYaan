# GatiYaan - On-Demand EV Charging Application

GatiYaan is a comprehensive, multi-role web application designed to simulate a real-world service for electric vehicle (EV) owners. Inspired by modern service apps like Swiggy, it provides a seamless experience for customers needing roadside charging, service providers offering the charging service, and administrators managing the platform.

## Key Features

- **Multi-Role Architecture**: Separate, tailored interfaces for Customers, Service Providers, and an Administrator.
- **Customer Panel**: Users can browse available charging vans, book a service, track the provider's arrival on a live map, and view their booking history.
- **Provider Panel**: Service providers can set their availability, receive and accept job requests in real-time, and manage their active jobs.
- **Admin Panel**: A powerful dashboard for administrators to oversee the entire ecosystem, including managing users and service providers.
- **Dynamic & Responsive UI**: Built with React, Tailwind CSS, and Framer Motion for a fluid, modern, and animated user experience that works across devices.
- **Dark Mode**: A beautiful, persistent dark theme is available for user comfort.

---

## Environment Setup (API Keys)

For the application to be fully functional, you must provide API keys for Google Gemini and Google Maps.

1.  **Get Your Keys**:
    *   **Gemini API Key**: Obtain a key from [Google AI Studio](https://aistudio.google.com/app/apikey).
    *   **Google Maps API Key**: Obtain a key from the [Google Cloud Console](https://console.cloud.google.com/google/maps-apis/overview). Ensure the **Maps Static API** is enabled for your project.

2.  **Add Keys to the Project**:
    *   Open the `index.html` file.
    *   At the top of the `<head>` section, you will find a `<script>` tag.
    *   Replace the placeholder strings `YOUR_GEMINI_API_KEY_HERE` and `YOUR_GOOGLE_MAPS_API_KEY_HERE` with your actual keys.

    ```html
    <script>
      window.process = {
        env: {
          API_KEY: 'YOUR_GEMINI_API_KEY_HERE',
          GOOGLE_MAPS_API_KEY: 'YOUR_GOOGLE_MAPS_API_KEY_HERE'
        }
      };
    </script>
    ```

## Logging In: How to Access Different Roles

The application uses a mock OTP system for authentication. Use the following credentials on the **Sign-In** page to access the different panels. The mock OTP is the same for most roles.

**Mock OTP for regular users: `123456`**

### 1. Admin Access

To log in as an administrator and access the Admin Panel to manage users and providers:

-   **Phone Number**: `0000000000`
-   **OTP**: `admin123` *(Note: The admin has a unique OTP for security)*

### 2. Service Provider Access

To log in as a service provider and access the Provider Panel to accept jobs:

-   **Phone Number**: `8765432109`
-   **OTP**: `123456`

### 3. Customer Access

To log in as a regular customer to book a charging van:

-   **Phone Number**: Use any 10-digit phone number that is **not** the Admin's or the Provider's (e.g., `9876543210`).
-   **OTP**: `123456`

If you use a new phone number, the system will automatically create a new customer account for you.