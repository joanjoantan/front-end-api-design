# Login Component:

- Role: Responsible for rendering the login form and handling user authentication.
- Visual: Contains input fields for Customer Username, and Password, and a "Sign In" button.
- UX Behavior: Validates input, triggers authentication, and handles success/failure feedback.

# Navigation Component:

- Role: Manages and displays navigation links based on user permissions and product levels.
- Visual: Presents a menu with links to accessible reports and configuration pages.
- UX Behavior: Dynamically generates links based on user permissions and highlights the active page.

# Compann/Customer Component:

- Role: Allows company to add user.
- Visual: Presents different customer have access to view different report
- UX Behavior: Validates input and handles success/failure feedback.

# Users Settings Component:

- Role: Allows users to configure their language, time zone, and distance units.
- Visual: Provides options for setting preferences.
- UX Behavior: Updates user settings and triggers data refresh upon changes.

# Report Component:

- Role: Displays report data fetched from the API.
- Visual: Presents report data and configuration page

  - Vehicle report: Show those details

    - Current Location of Vehicles,
    - List of Incidents involving Vehicles,
    - Drivers ranked by their Driving Score.

- Configuration page:

  - User Configuration: allow the create or edit user
  - Vehicle Configuration: allow user change the description or registration number of a vehicle.

- UX Behavior: May allow for sorting, filtering, or exporting data.

# API Service:

- Role: Handles API requests and data retrieval.
- Visual: Backend service, not directly visible to users.
- UX Behavior: Ensures data is fetched with the user's preferences (language, time zone, distance units).

# Relationships Between Components:

- The Login Component handles user authentication and sets the session.

- The Navigation Component relies on user permissions and product levels to generate navigation links.

- The Settings Component interacts with the API Service to update user preferences.

- The Report Component communicates with the API Service to fetch and display report data based on user settings.

- The Configuration Component communicates with the API Service to fetch and display configuration data based on user settings.

# Visual Components and UX Behavior:

- The Login Component should have input validation and provide feedback on authentication success or failure.

- The Navigation Component should provide a clear, user-friendly menu and highlight the active page.

- The Settings Component should offer a straightforward interface for setting user preferences.

- The Report Component should display data clearly, possibly with interactive elements for user convenience.

- The Configuration Component should display data clearly, possibly with interactive elements for user convenience.

# React Features:

- State Management: Utilize React's state (useState, useContext) for managing user sessions, settings, and UI state.

- Routing: Use React Router for handling client-side navigation and rendering different reports/pages based on routes.

- Component Lifecycle: Employ useEffect for handling side effects like API requests and updating UI based on settings changes.

- Context API: Use Context for sharing session information and settings across components.

- Conditional Rendering: Render components conditionally based on user permissions and settings.

# Third-Party npm Packages:

- React Router: For managing client-side routing and rendering different reports/pages based on routes.

- Axios: For making HTTP requests to the API. Axios is a widely used package for handling API communication.

- i18next: For internationalization (i18n) support, providing content in the user's selected language.

- moment-timezone: For handling time zone conversions and formatting date times based on the user's time zone.

- react-bootstrap or Material-UI: These UI component libraries can be useful for creating visually appealing and responsive components without starting from scratch.
