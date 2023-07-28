**Go minimal application**
--
Web application with an API that allows users to subscribe to
plans from a catalog of products.

Here are the steps taken to implement the project

1. Project Setup and Database Schema:
   - Set up a Go project with the necessary directories and files.
   - Create a PostgreSQL database and define the schema to store users, products, plans, and bills.

2. Authentication - As a user, I want to log in to the app, so that I can use the app (User Story 1):
   - Implement a simple login mechanism using email/password.
   - Store hashed passwords in the database for security.
   - Provide an endpoint to authenticate users and generate access tokens for future API requests.

3. Subscription Plans - As a user, I can view the subscription plans of the app, so that I can
decide which one to subscribe to (User Story 2):
   - Create API endpoints to fetch and display the list of products and their subscription plans.
   - Seed the database with sample data for products and plans.
   - Design the response to provide product details along with prices for each plan.

4. Subscription Selection - As a user, I can select a subscription plan and billing option so that I
can be billed accordingly (User Story 3):
   - Implement an API endpoint that allows users to select a subscription plan and billing option.
   - Store the selected subscription in the database for the user.

5. Bill Generation - As a system, I should generate a bill for the subscription at the due
date of the subscription (User Story 4):
   - Implement a background job or a scheduled task to generate bills for active subscriptions.
   - Bills should have a pending status by default.

6. Bill Payment - As a user, I can pay a bill, so that my due bills are settled (User Story 5):
   - Create an API endpoint to mark bills as paid when the user initiates the payment.
   - Bills should have a "paid" status after successful payment.

7. Service Restriction - The user should be unable to use the service when he is 5-days late on the due date (User Story 6):
   - Implement a mechanism to check a user's due bills status when accessing certain functionalities.
   - If the user is 5-days late on the due date, restrict access to the service accordingly.

8. Testing:
   - Write test cases for each API endpoint and business logic.
   - Cover scenarios for user login, subscription selection, bill generation, and payment.

9. Documentation:
   - Document the API endpoints and their usage for better understanding.

