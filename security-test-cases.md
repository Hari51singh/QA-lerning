# Security Test Cases – Login Feature

## Objective
To verify that the login functionality is secure against common security vulnerabilities.

---

## Test Scenarios

### 1. SQL Injection
- Input: `' OR 1=1 --`
- Expected Result: Login should fail and show a generic error message.

### 2. XSS Attack
- Input: `<script>alert('XSS')</script>`
- Expected Result: Script should not execute and input should be sanitized.

### 3. Brute Force Protection
- Action: Attempt login with wrong password more than 5 times
- Expected Result: Account should be temporarily locked or captcha shown.

### 4. Error Message Validation
- Action: Invalid username/password
- Expected Result: Error message should not reveal whether username or password is incorrect.

### 5. Session Handling
- Action: Login and refresh page
- Expected Result: User session should remain active.

---

## Notes
- Security test cases should be executed in staging or test environment only.
