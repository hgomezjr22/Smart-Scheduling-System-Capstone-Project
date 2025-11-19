# ✅ Smart Scheduling System — Test Cases

This document outlines functional test cases for core features of the Smart Scheduling System.  
Each test case includes the objective, prerequisites, steps, and expected results.

---

## 🔵 Test Case 1 — User Login (Employee / Manager)

**Objective:** Ensure users can log in with valid credentials.  
**Prerequisites:** User exists in database.  

**Steps:**  
1. Navigate to the Login page.  
2. Enter valid email and password.  
3. Click "Login."  

**Expected Result:**  
- User successfully logs in and is redirected to their dashboard.

---

## 🔵 Test Case 2 — Invalid Login Attempt

**Objective:** Ensure login fails with incorrect credentials.  

**Steps:**  
1. Go to Login page.  
2. Enter incorrect email or password.  
3. Click "Login."  

**Expected Result:**  
- Error message displays: “Invalid email or password.”  
- User stays on login screen.

---

## 🔵 Test Case 3 — Employee Enters Availability

**Objective:** Confirm employees can input and edit their availability.  

**Steps:**  
1. Log in as an employee.  
2. Navigate to "My Availability."  
3. Select days and time ranges.  
4. Click “Save Availability.”  

**Expected Result:**  
- Availability is saved and shown in the database.  
- Confirmation message appears.

---

## 🔵 Test Case 4 — Manager Creates Manual Schedule

**Objective:** Validate managers can manually assign shifts.  

**Steps:**  
1. Log in as a manager.  
2. Go to “Create Schedule.”  
3. Select an employee.  
4. Pick date and shift time.  
5. Click “Assign.”  

**Expected Result:**  
- Shift appears in the database.  
- Employee sees updated shift in their portal.

---

## 🔵 Test Case 5 — Auto-Scheduling

**Objective:** Test automatic schedule generation using employee availability.  

**Prerequisites:**  
- Multiple employees with availability stored.

**Steps:**  
1. Log in as manager.  
2. Go to “Auto Schedule.”  
3. Select a date range.  
4. Click “Generate Schedule.”  

**Expected Result:**  
- System generates a schedule that respects availability and staffing needs.  
- Manager dashboard displays auto-generated schedule.

---

## 🔵 Test Case 6 — Employee Confirms or Declines Shifts

**Objective:** Ensure employees can respond to assigned shifts.  

**Steps:**  
1. Log in as employee.  
2. Go to “My Shifts.”  
3. Click “Confirm” or “Decline” on a shift.  

**Expected Result:**  
- Confirmation or decline is saved.  
- Manager receives alert in dashboard.

---

## 🔵 Test Case 7 — Staff Request Shift Swap

**Objective:** Verify employees can request shift swaps.  

**Steps:**  
1. Log in as employee.  
2. Open “My Shifts.”  
3. Choose shift → click “Request Swap.”  
4. Select another employee.  
5. Submit request.  

**Expected Result:**  
- Swap request is recorded.  
- Manager sees pending request in dashboard.

---

## 🔵 Test Case 8 — System Alerts Manager for Unconfirmed Shifts

**Objective:** Ensure system notifies manager when employees don’t confirm on time.  

**Steps:**  
1. Assign shift to employee.  
2. Wait until confirmation window expires.  

**Expected Result:**  
- Manager receives alert: “Shift not confirmed.”  
- Shift is marked as “Pending Review.”

---

## 🔵 Test Case 9 — Mobile Responsiveness

**Objective:** Make sure UI adjusts correctly on mobile.  

**Steps:**  
1. Open app on mobile browser.  
2. Navigate across pages.  

**Expected Result:**  
- Pages resize properly.  
- Buttons and text remain usable and visible.

---

## 🔵 Test Case 10 — Data Integrity After Updates

**Objective:** Ensure no data is lost when schedule changes occur.  

**Steps:**  
1. Manager edits a shift.  
2. Confirm employee portal updates.  
3. Review database (Bubble backend).  

**Expected Result:**  
- Old shift is replaced by new one.  
- No duplicate data.  
- History reflects change (if enabled).

---

# ✔️ End of Test Cases
