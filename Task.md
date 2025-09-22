Task 1 – Password Hashing Authentication
👉 Implement a simple Node.js + Express server with these features:
Register API
Accepts username and password.
Hash the password using bcrypt.
Store it in an in-memory array (no database required).
Login API
Accepts username and password.
Verify the password using bcrypt.compare.
If valid → return "Login Successful".
If invalid → return "Invalid credentials".
📌 Expected Routes
POST /register → Register new user.
POST /login → Login user.

Task 2 – JWT Authentication (with Hashing)
👉 Extend your Task 1 project by adding JWT Authentication.
On successful login:
Generate a JWT token using jsonwebtoken.
Send token back to client.
Create a Protected Route /profile:
Only accessible if user provides a valid JWT in the Authorization header (format: Bearer <token>).
If valid, return "Welcome <username>".
If invalid/expired, return "Unauthorized".
📌 Expected Routes
POST /register → Register new user with hashed password.
POST /login → Login user and generate JWT.
GET /profile → Protected route, requires token.
