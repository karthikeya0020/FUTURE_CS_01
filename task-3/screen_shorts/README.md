## Evidence Screenshots

The following screenshots document the security testing process and validate the identified vulnerabilities.

---

### 1. Public User Listing Without Authentication
**File:** 01_public_users_list_no_auth.png  

- Endpoint: GET /users  
- Status: 200 OK  
- Observation: Full user dataset accessible without authentication headers.  
- Risk: Unrestricted data exposure.

---

### 2. Object-Level Access Manipulation (User ID 1)
**File:** 02_object_access_user1_excessive_data.png  

- Endpoint: GET /users/1  
- Status: 200 OK  
- Observation: Complete user object returned without authorization checks.  
- Risk: Broken Object Level Authorization (BOLA).

---

### 3. Absence of Authentication Headers
**File:** 03_no_authentication_headers_proof.png  

- Observation: No Authorization or Bearer token included in request headers.  
- Risk: Missing authentication enforcement.

---

### 4. Unauthorized Access to Another User (User ID 2)
**File:** 04_bola_user2_access_success.png  

- Endpoint: GET /users/2  
- Status: 200 OK  
- Observation: Access to another user's data by modifying ID.  
- Risk: Broken Object Level Authorization.

---

### 5. POST Request Accepted Without Authentication
**File:** 05_post_method_user2_no_auth.png  

- Endpoint: POST /users/2  
- Status: 201 Created  
- Observation: POST request accepted without authentication or validation.  
- Risk: Improper authentication and method handling.

---

## Screenshot Integrity Note

All screenshots were captured during controlled testing and are included for documentation and validation purposes only.
