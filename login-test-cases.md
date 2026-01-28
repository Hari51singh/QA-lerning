
# Login Test Cases

## Test Case 1: Valid Login
Steps:
1. Open the application
2. Enter valid Email or Student ID
3. Enter valid password
4. Click Login

Expected Result:
- User should login successfully
--

## Test Case 2: Invalid Password
Steps:
1. Open the application
2. Enter valid Email or Student ID
3. Enter invalid password
4. Click Login

Expected Result:
- Error message should be displayed
## Negative & Security Test Cases

| ID | Scenario | Test Data | Expected Result |
|----|--------|-----------|----------------|
| TC-09 | Empty email & password | "", "" | Error message displayed |
| TC-10 | SQL Injection | ' OR 1=1 | Login should fail |
| TC-11 | XSS input | <script>alert(1)</script> | Input sanitized |
| TC-12 | Leading spaces | " user@email.com " | Spaces trimmed |
| TC-13 | Long input | 256+ characters | Validation error |
