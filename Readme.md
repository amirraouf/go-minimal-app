Sure, I'll provide you with a high-level outline of how you can approach this task using Go and PostgreSQL. Keep in mind that this is a simplified implementation and should serve as a starting point for a real product.

1. Project Setup and Database Schema:
   - Set up a Go project with the necessary directories and files.
   - Create a PostgreSQL database and define the schema to store users, products, plans, and bills.

2. User Authentication (User Story 1):
   - Implement a simple login mechanism using email/password.
   - Store hashed passwords in the database for security.
   - Provide an endpoint to authenticate users and generate access tokens for future API requests.

3. Subscription Plans (User Story 2):
   - Create API endpoints to fetch and display the list of products and their subscription plans.
   - Seed the database with sample data for products and plans.
   - Design the response to provide product details along with prices for each plan.

4. Subscription Selection (User Story 3):
   - Implement an API endpoint that allows users to select a subscription plan and billing option.
   - Store the selected subscription in the database for the user.

5. Bill Generation (User Story 4):
   - Implement a background job or a scheduled task to generate bills for active subscriptions.
   - Bills should have a pending status by default.

6. Bill Payment (User Story 5):
   - Create an API endpoint to mark bills as paid when the user initiates the payment.
   - Bills should have a "paid" status after successful payment.

7. Service Restriction (User Story 6):
   - Implement a mechanism to check a user's due bills status when accessing certain functionalities.
   - If the user is 5-days late on the due date, restrict access to the service accordingly.

8. Testing:
   - Write test cases for each API endpoint and business logic.
   - Cover scenarios for user login, subscription selection, bill generation, and payment.

9. Documentation:
   - Document the API endpoints and their usage for better understanding.

Please note that the actual implementation will involve more detailed steps and considerations, such as error handling, input validation, and securing sensitive endpoints. Additionally, for testing, you can use Go's built-in testing framework or third-party testing libraries like "testing" or "goconvey."

Remember that this outline is not a complete implementation, but it should give you a good starting point for building the web application with Go and PostgreSQL based on the provided user stories.