# E-commerce Web Automation Framework

Automated end-to-end testing framework for **Sauce Demo**, a web application designed for practicing and demonstrating software testing and test automation.

The project focuses exclusively on **QA automation**, applying professional testing practices to validate critical e-commerce workflows such as authentication, product management, shopping cart operations, and checkout.

---

## Project Overview

This project was created to demonstrate the design and implementation of a maintainable **Web UI Test Automation Framework**.

The framework automates critical user journeys through an e-commerce application and applies QA principles such as:

* Test case design
* Functional testing
* Negative testing
* Regression testing
* End-to-end testing
* Test data management
* Page Object Model
* Reusable automation components
* Assertions
* Automated reporting
* Continuous Integration

The goal is to create a scalable automation solution rather than a collection of independent test scripts.

---

## Objectives

* Build a maintainable web automation framework.
* Automate critical e-commerce user journeys.
* Apply Page Object Model architecture.
* Create reusable test components.
* Implement reliable element locators.
* Validate positive and negative scenarios.
* Execute automated regression tests.
* Generate test execution reports.
* Integrate automated tests into CI/CD.
* Demonstrate professional QA automation practices.

---

## Application Under Test

**Application:** Sauce Demo / Swag Labs

The application provides an e-commerce environment with functionality for:

* User authentication
* Product browsing
* Product details
* Shopping cart
* Checkout
* Order confirmation

---

## Testing Scope

### Authentication

* Successful login.
* Invalid credentials.
* Locked user validation.
* Empty username.
* Empty password.
* Logout.

### Products

* Product catalog validation.
* Product details validation.
* Product sorting.
* Add product to cart.
* Remove product from cart.

## Shopping Cart

* Add a single product.
* Add multiple products.
* Remove products.
* Validate cart contents.
* Validate product prices.
* Validate cart totals.

### Checkout

* Checkout with valid information.
* Required field validation.
* Invalid checkout information.
* Order summary validation.
* Successful checkout.
* Order confirmation validation.

---

## QA Approach

The automation suite follows a risk-based approach, prioritizing critical business flows.

### Priority 1 — Critical

* Login.
* Add product to cart.
* Checkout.
* Successful order.

### Priority 2 — High

* Product sorting.
* Product removal.
* Cart validation.
* Checkout validations.

### Priority 3 — Medium

* Product details.
* Secondary navigation scenarios.
* Additional negative scenarios.

---

## Framework Architecture

The framework follows a layered architecture to separate test logic from application interaction.

```text
┌───────────────────────────────┐
│          Test Cases           │
│            JUnit              │
└───────────────┬───────────────┘
                │
                ▼
┌───────────────────────────────┐
│        Page Objects            │
│      Page Interactions         │
└───────────────┬───────────────┘
                │
                ▼
┌───────────────────────────────┐
│      Automation Utilities      │
│  Driver / Browser / Waits      │
│  Test Data / Assertions        │
└───────────────┬───────────────┘
                │
                ▼
┌───────────────────────────────┐
│          Playwright            │
└───────────────┬───────────────┘
                │
                ▼
┌───────────────────────────────┐
│          Sauce Demo            │
└───────────────────────────────┘
```

---

## Technology Stack

| Technology        | Purpose                         |
| ----------------- | ------------------------------- |
| Java              | Programming language            |
| Playwright        | Web automation                  |
| JUnit             | Test execution                  |
| Maven             | Dependency and build management |
| Page Object Model | Framework architecture          |
| Git               | Version control                 |
| GitHub            | Repository and collaboration    |
| GitHub Actions    | CI/CD                           |
| Allure            | Test reporting                  |

---

## Automated Test Flow

The main end-to-end scenario follows this flow:

```text
Open Application
       ↓
Login
       ↓
Validate Products
       ↓
Select Product
       ↓
Add to Cart
       ↓
Open Cart
       ↓
Validate Cart
       ↓
Checkout
       ↓
Enter Customer Information
       ↓
Validate Order Summary
       ↓
Complete Order
       ↓
Validate Confirmation
```

---

## Automation Design Principles

The framework follows several principles to improve maintainability and reliability.

### Page Object Model

Application pages are represented as independent classes containing their elements and interactions.

```text
LoginPage
ProductsPage
ProductDetailsPage
CartPage
CheckoutPage
OrderConfirmationPage
```

### Reusable Components

Common functionality is centralized to avoid duplicated automation code.

Examples:

* Browser initialization.
* Navigation.
* Explicit waiting.
* Element interaction.
* Assertions.
* Screenshots.
* Test data loading.

### Reliable Locators

The framework prioritizes stable selectors and avoids fragile locators whenever possible.

### Independent Tests

Each test should be executable independently whenever possible to reduce test coupling.

---

## Test Types

The project includes different testing categories:

### Functional Testing

Validates that application functionality behaves according to expected requirements.

### Negative Testing

Validates how the application behaves with invalid or unexpected input.

### Regression Testing

Ensures previously implemented functionality continues to work after changes.

### Smoke Testing

A small suite covering the most critical functionality.

### End-to-End Testing

Validates complete business workflows from authentication to successful order completion.

---

## Test Reporting

Automated executions will generate reports containing:

* Test status.
* Execution time.
* Failed scenarios.
* Error information.
* Screenshots.
* Execution history.

Allure will be used to provide a visual representation of test results.

---

## CI/CD Integration

The automation suite will be integrated with **GitHub Actions**.

The pipeline will execute automatically when changes are pushed or pull requests are created.

```text
Developer Push
      ↓
GitHub Repository
      ↓
GitHub Actions
      ↓
Build Project
      ↓
Run Automated Tests
      ↓
Generate Report
      ↓
Publish Results
```

---

## Execution

### Prerequisites

Install:

* Java
* Maven
* Git

Playwright dependencies will be configured through the project.

### Clone Repository

```bash
git clone <repository-url>
cd ecommerce-web-automation-framework
```

### Install Dependencies

```bash
mvn clean install
```

### Run Tests

```bash
mvn test
```

### Run a Specific Test

```bash
mvn test -Dtest=LoginTest
```

---

## Test Documentation

The project documentation will include:

* Test Plan
* Test Strategy
* Test Cases
* Test Data
* Automation Architecture
* Traceability Matrix
* Defect Documentation
* Test Evidence
* Regression Suite
* CI/CD Documentation

---

## Future Improvements

Planned improvements include:

* Parallel test execution.
* Cross-browser testing.
* Data-driven testing.
* Advanced test fixtures.
* API test integration.
* Docker execution.
* Advanced Allure reporting.
* Test execution history.
* Automated screenshots and videos on failure.
* Expanded CI/CD pipeline.
* Integration with test management tools.

---

## Portfolio Goals

This project demonstrates practical experience in:

* Web test automation.
* Playwright.
* Java.
* JUnit.
* Page Object Model.
* End-to-end testing.
* Functional testing.
* Regression testing.
* Negative testing.
* Test architecture.
* CI/CD.
* Automated reporting.
* QA engineering practices.

The project is designed to demonstrate the ability to build a **professional and maintainable automation framework**, rather than simply creating individual automated test cases.

---

## Project Status

**Status:** In Development

The framework is being developed incrementally, starting with the core authentication and e-commerce workflows and progressively expanding the automated regression suite and CI/CD capabilities.

---

## License

This project is intended for educational and portfolio purposes.
