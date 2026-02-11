# Katalon E-Commerce Automation

## Project Overview
Web UI automation project built using **Katalon Studio Record & Playback**, without writing any code.  
The goal of this project is to demonstrate **real-world QA automation practices**, including test design, positive and negative testing, and maintainable test structure.

**Current repo status**: This repository currently contains **Login** automation (positive + negative). Other e-commerce flows listed in scope below are **planned** but not yet committed as automated tests.

---

## Application Under Test
**Sauce Demo**  
[https://www.saucedemo.com](https://www.saucedemo.com)

### Test credentials (Sauce Demo)
- **Valid user**: `standard_user`
- **Valid password**: `secret_sauce`

---

## Test Scope

### In Scope
- Login functionality (positive and negative scenarios)  
- Product listing  
- Add to cart  
- Checkout process  
- Logout  

### Out of Scope
- Performance testing  
- Security testing  
- Cross-browser testing  

---

## Tools & Technologies
- Katalon Studio (Record & Playback)  
- Selenium (built-in with Katalon)  
- GitHub Desktop for version control  

---

## Test Design Approach
- Manual test cases designed before automation  
- Positive and negative scenarios recorded with Katalon Recorder  
- Object Repository used for element management  
- Assertions added for validation (via Record & Playback)  
- Waits (`waitForElementVisible`, `waitForElementClickable`) added for stable execution  
- Descriptions and tags added for clarity and portfolio-readiness  

---

## Project Structure (Katalon)
- **`Katalon-ecommerce-automation.prj`**: Katalon project file (created/updated with Katalon Studio **10.4.3**)
- **`Test Cases/`**: automated test cases (`.tc`)
  - `Test Cases/Login/`: login test cases
- **`Object Repository/`**: saved UI locators (`.rs`)
  - `Object Repository/LoginPage/`: login page elements + assertions
- **`Profiles/`**: execution profiles (global variables)
- **`Test Suites/`**: suites to run multiple tests together (**not included yet** in this repo)
- **`Keywords/`** / **`Include/scripts/groovy/`**: custom keywords (Groovy) (**not used yet**; this project is Record & Playback focused)

---

## How to Run the Tests
1. Clone this repository  
2. Open the project in **Katalon Studio** (tested with Katalon Studio **10.4.3**)  
3. Open the **Test Cases** or **Test Suites** folder  
4. Select a test case (or a suite, if you add one)  
5. Click **Run → Chrome**  

### Notes
- If you don’t see any suites: this repo currently ships with **test cases only** (no `Test Suites/` yet). You can still run any test case directly from the **Test Cases** tree.
- The project uses the **Object Repository** for selectors (CSS/XPath), so element maintenance is centralized there.

---

## Test Cases Included
| Test Case | Description | Tags |
|-----------|-------------|------|
| `TC_Valid_Login_RnP` | Valid login for `standard_user`; verifies Products page is displayed | Login, Positive, Smoke |
| `TC_Invalid_Password_RnP` | Login with invalid password; verifies error message | Login, Negative, Regression |
| `TC_Empty_Credentials_RnP` | Login with empty username/password; verifies validation message | Login, Negative, Regression |
