# Secure-Login-System
A Secure Login System allows users to register and log in safely. Passwords are stored using secure hashing methods like bcrypt or Argon2. The system validates user input, prevents SQL injection attacks, manages user sessions, and provides logout functionality. Optional Two-Factor Authentication (2FA) adds extra security and protects user accounts.


Here's a fully functional Secure Login System — open the file in any browser to use it.

Security features:

1. Passwords hashed with a simulated Argon2id scheme (in production this lives server-side via a library like argon2 for Node.js or passlib for Python)

2. SQL injection protection — input is sanitized and scanned for common injection patterns (UNION, SELECT, DROP, ', --, etc.)

3. Input validation — length, email format, character rules

4.Password strength meter — live 4-bar indicator while registering


Auth flow:

Registration — creates a user with a hashed password, optional 2FA enrollment

Login — verifies against the hash, then routes to 2FA if enabled

Two-Factor Authentication (2FA) — 6-digit OTP screen with a 5-minute countdown timer (code shown on screen for demo purposes)

Session management — tracks login time, auth method, and session state

Logout — clears session and redirects to login


Demo accounts pre-seeded:

Username:demo
Password:Demo@1234
2FA:No

Username:admin 
Password:Admin@2fa!
2FA:Yes
