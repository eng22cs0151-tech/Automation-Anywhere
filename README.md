# Automation-Anywhere
 Automation Assignment – UI & API Testing (Playwright)
 Project Overview

This project automates UI and API test scenarios for the Automation Anywhere Community Edition application using Playwright.

The framework follows Page Object Model (POM) principles to ensure clean structure, reusability, and maintainability.
Both UI workflows and backend API validations are covered as part of the assignment.

# Tech Stack & Tools

Automation Framework: Playwright

Language: JavaScript

Test Runner: Playwright Test

Design Pattern: Page Object Model (POM)

Assertions: Playwright built-in expect

API Testing: Playwright APIRequestContext

Version Control: Git & GitHub

IDE: VS Code

# Project Structure
Playwright-Automation/
│
├── pages/                  # Page Object classes
│   ├── LoginPage.js
│   ├── DashboardPage.js
│   ├── AutomationPage.js
│   ├── MessageBoxTaskPage.js
│   ├── FormBuilderPage.js
│
├── tests/                  # Test specifications
│   ├── ui/
│   │   ├── messageBoxTask.spec.js
│   │   ├── formUpload.spec.js
│   │
│   ├── api/
│   │   ├── learningInstance.spec.js
│
├── utils/                  # Helpers and utilities
│   ├── apiHelper.js
│   ├── testData.js
│
├── playwright.config.js
├── package.json
├── README.md

# Prerequisites

Node.js v18+

Git

VS Code

Valid Automation Anywhere Community Edition account

#  Setup Instructions

Clone the repository

git clone https://github.com/your-username/Playwright-Automation.git
cd Playwright-Automation


Install dependencies

npm install


Install Playwright browsers

npx playwright install
# Test Execution
Run all tests
npx playwright test

Run only UI tests
npx playwright test tests/ui

Run only API tests
npx playwright test tests/api

View test report
npx playwright show-report

# Environment Configuration

Create a .env file in the root directory:

BASE_URL=https://www.automationanywhere.com
USERNAME=your-username
PASSWORD=your-password


 Note: Credentials are not committed to GitHub for security reasons.

 Test Scenarios Covered
# Use Case 1: Message Box Task (UI Automation)

Objective: Automate creation of a Message Box Task Bot.

Validations Implemented:

Login functionality

Navigation to Automation section

Task Bot creation

UI element visibility checks

Message Box action selection

Right panel UI interaction verification

Save configuration

Success confirmation validation

 Assertions:

Element visibility & interaction

Correct data entry

Successful task creation

End-to-end functional flow

# Use Case 2: Form with Upload Flow (UI Automation)

Objective: Automate Form creation with Textbox and File Upload.

Validations Implemented:

Form creation flow

Drag and drop Textbox & File Upload elements

UI configuration verification

Text input interaction

File selection from shared folder

File upload confirmation

Form save validation

Assertions:

UI element presence and behavior

File upload success status

Form submission behavior
# Use Case 3: Learning Instance API Flow (API Automation)

Objective: Validate Learning Instance creation via APIs.

Validations Implemented:

Login API authentication

Learning Instance creation API

API response validation

Field-level assertions

✔ API Assertions:

HTTP status codes (200 / 201)

Response body structure

Field values (ID, name, status)

Functional correctness of instance creation

Response time (where applicable)

# Framework Design (POM)

Each page has its own class

Locators and actions are separated from test logic

Improves:

Code reusability

Maintainability

Scalability
