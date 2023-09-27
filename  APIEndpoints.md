# API Endpoints (Assumptions):

### Authentication Endpoint:

Route: /api/authenticate
Method: POST
Parameters:

- Username: The username provided by the user.
- Password: The user's password.

Description: This endpoint is responsible for authenticating users. Upon successful authentication, it should return a user session token or an error message.

Expected Response:

- On success: { "message": Login successfully", "token": string, UserID: string }
- On error: { "error": "Error message describing the issue" }

### Customer Management Endpoint:

Route: /api/customers
Methods: POST (Create), PUT (Update), DELETE (Delete)
Parameters:

- CustomerID: The unique identifier of the customer.
- CustomerName: The name or identifier of the customer (for updates and deletes).
- ProductLevel: The product level of the customer, which determines the accessible reports.

Description: This endpoint is used for customer management operations. Only users with appropriate permissions should have access to this endpoint.

These endpoints should be designed to handle the specific requirements of the application, including authentication, user settings, permissions, report retrieval, and user and customer management. Additionally, proper authentication and authorization mechanisms should be implemented to ensure that users can only access data and functionality for which they have permission.

Expected Response:

- On success: { "message": "Customer created/updated/deleted successfully" }
- On error: { "error": "Error message describing the issue" }

### User Management Endpoint:

Route: /api/users
Methods: POST (Create), PUT (Update), DELETE (Delete)
Parameters:

- UserID: The unique identifier of the user (for updates and deletes).
- Username: The username of the user (for user creation and updates).
- Password: The user's password (for user creation and updates).
- Role: The role of the user (e.g., "Admin," "Employee").
- Permission: Claims or Permissions which determine which reports that can see

Description: This endpoint is used for user management operations. Only users with appropriate permissions (e.g., Admin) should have access to this endpoint.

Expected Response:

- On success: { "message": "User created/updated/deleted successfully" }
- On error: { "error": "Error message describing the issue" }

### User Settings Endpoint:

Route: /api/user/settings
Method: PUT
Parameters:

- UserID: The unique identifier of the user.
- Language: The preferred language of the user.
- TimeZone: The user's selected time zone.
- DistanceUnit: The user's preference for distance units (e.g., miles or kilometers).

Description: This endpoint allows users to update their settings, including language, time zone, and distance units. It should return the updated user settings or an error message.

### Reports Data Endpoint:

Route: /api/vehicle-reports
Method: GET
Parameters:

- ReportType: The type of report requested (e.g., "Current Location of Vehicles").
- UserID: The unique identifier of the user.

Description: This endpoint retrieves vehicle report data based on the user's permissions and settings.

Expected Response:

- On success: JSON data representing the requested vehicle report.
- On error: { "error": "Error message describing the issue" }

### Vehicle Configuration Endpoint:

Route: /api/vehicle-configuration
Method: PUT
Parameters:

- VehicleID: The unique identifier of the vehicle.
- Description: The updated description of the vehicle.
- RegistrationNumber: The updated registration number of the vehicle.

Description: This endpoint allows users to update vehicle configuration details, such as description and registration number.

Expected Response:

- On success: { "message": "Vehicle configuration updated successfully" }
- On error: { "error": "Error message describing the issue" }
