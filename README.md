# BDD Test Automation Framework Cucumber Java 
## Overview

This repository demonstrates a complete **Cucumber BDD Framework** structure using:

* **Gherkin Feature Files**
* **Step Definitions** (Java)
* **Test Runner** with Cucumber options
* **Page Objects / Business Logic Methods** (optional foundation)

It showcases how Behavior-Driven Development (BDD) brings collaboration between QA, Developers, and Business teams using natural-language test scenarios.

The project follows standard Cucumber folder structure and is ideal for:

* Beginners learning Cucumber from scratch
* QA Automation Engineers preparing for interviews
* People building their first BDD framework with TestNG / JUnit

---

## What is Cucumber BDD?

Cucumber is a testing framework that enables writing tests in **plain English**, using **Gherkin syntax** (`Given/When/Then`).

### ✔ Key Benefits

* Improves collaboration with non-technical stakeholders
* Easy-to-read test cases
* Supports Data Tables & Scenario Outlines
* Integrates with Selenium WebDriver
* Supports parallel execution
* Provides clean separation of Feature files and Automation code

---

## Project Modules

### 🔹 1. Feature Files (`Featuresfile`)

Contains `.feature` files written in **Gherkin syntax**.
Examples include:

* `E-com.feature` — Ecommerce test scenarios
* `login.feature` — Login test scenarios

Each feature file includes:

* Scenario
* Steps (`Given`, `When`, `Then`)
* Data using Scenario Outline (if applicable)

---

### 🔹 2. Step Definitions (`StepDefination`)

Java classes containing automation code linked to Gherkin steps.
Examples:

* `EcommercePurchase.java`
* `LoginStep.java`

Each method is mapped using annotations like:

```java
@Given("user is on login page")
public void user_on_login_page() { ... }
```

---

### 🔹 3. Test Runner (`TestRunner`)

Contains code to run Cucumber tests with options like:

* `features` path
* `glue` path
* `tags` for selective execution
* `plugin` for HTML / JSON reports

Example files:

* `EcomRunner.java`
* `TestRun.java`

Typical runner structure:

```java
@CucumberOptions(
    features = "src/main/java/java/Featuresfile",
    glue = {"StepDefination"},
    plugin = {"pretty", "html:target/cucumber-reports"},
    monochrome = true
)
```

---

## Folder Structure

```
Cucumber-BDD-/
├── src/
│   └── main/
│       └── java/
│           └── java/
│               ├── Featuresfile/
│               │   ├── E-com.feature
│               │   ├── login.feature
│               │   └── package-info.java
│               │
│               ├── StepDefination/
│               │   ├── EcommercePurchase.java
│               │   ├── LoginStep.java
│               │   └── package-info.java
│               │
│               └── TestRunner/
│                   ├── EcomRunner.java
│                   ├── TestRun.java
│                   └── package-info.java
│
├── .settings/
├── .classpath
├── .gitignore
├── .project
└── pom.xml
```

---

## How to Run Cucumber Tests

1. Install dependencies using Maven (`pom.xml`).
2. Open **EcomRunner.java** or **TestRun.java**.
3. Right-click → **Run as Java Application**.
4. Reports will be generated inside `target/` folder.

---

## Notes

* This is a clean BDD example suitable for learning.
* To convert it into a complete framework, you can add:

  * Page Object Model (POM) classes
  * Hooks (`@Before`, `@After`)
  * Logging (Log4j)
  * Extent Reports
  * Parallel execution using TestNG
 
    ## 👨‍💻 Author

**Arpit Choubey — SDET | QA | Automation Engineer**
🔗 **LinkedIn** | **Medium**

## ⭐ Support

If this repository helps you, please **Star 🌟** it!

---
