# FreshCart API Testing Project

## Project Overview

This project demonstrates API testing for the FreshCart E-Commerce application using Postman. The testing scope covers Authentication, Products, and Cart modules, including both positive and negative test scenarios.

The objective of this project is to validate API functionality, verify response behavior, test error handling, and identify potential issues based on common REST API standards and best practices.

---

## Tools Used

* Postman
* GitHub
* Jira (Bug Reporting)
* Excel (Test Case Documentation)

---

## Tested Modules

### Authentication

* User Registration
* User Login
* Existing Email Validation
* Invalid Credentials Validation

### Products

* Get All Products
* Get Product by Valid ID
* Get Product by Invalid ID

### Cart

* Add Product to Cart
* Remove Product from Cart
* Invalid Product Validation
* Empty Product Validation

---

## API Testing Activities

* Created and executed API test cases.
* Performed positive and negative testing.
* Validated HTTP status codes.
* Verified API response payloads.
* Used Postman Environment Variables.
* Extracted and reused authentication tokens.
* Extracted product IDs dynamically from API responses.
* Created automated Postman assertions.

---

## Test Results Summary

| Result            | Count |
| ----------------- | ----- |
| Passed Test Cases | 11    |
| Failed Test Cases | 2     |
| Total Test Cases  | 13    |

---

## Key Findings

### Bug #1

**Title:** API returns HTTP 500 when adding an invalid product ID to the cart.

**Expected Result**

* HTTP 400 Bad Request or HTTP 404 Not Found
* Clear validation message

**Actual Result**

* HTTP 500 Internal Server Error
* "Cast to ObjectId failed"

---

### Bug #2

**Title:** API returns HTTP 500 when productId is empty.

**Expected Result**

* HTTP 400 Bad Request
* Validation message indicating that productId is required

**Actual Result**

* HTTP 500 Internal Server Error
* "Cast to ObjectId failed"

---

## Assumptions

Since no official API documentation or API contract was available, expected results were evaluated according to common REST API standards and industry best practices.

---

## Repository Contents

* Postman Collection
* Postman Environment
* API Test Cases (Excel)
* README Documentation

---

## Conclusion

The tested APIs successfully handled most functional scenarios related to authentication, product retrieval, and cart operations. However, error handling within the Cart module revealed validation weaknesses that resulted in unexpected HTTP 500 Internal Server Errors instead of user-friendly validation responses.
