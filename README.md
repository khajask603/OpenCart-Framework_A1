# OpenCart-Framework_A1
A professional Hybrid Automation Framework for E-commerce testing using Python, Selenium, and Pytest. Features Page Object Model (POM), Data-Driven Testing (DDT) via Excel, and automated timestamped reporting.

# PROJECT OVERVIEW:
it is a high-performance, hybrid automation framework engineered to validate complex e-commerce workflows on the OpenCart platform. The project is designed with a focus on scalability and maintainability, ensuring that UI changes require minimal code updates. By integrating Data-Driven logic, this framework allows for exhaustive testing of authentication and registration flows using externalized Excel data.

# Framework structure
----------------------

Project_Root/
├── configurations/                # Global Environment Settings
│   └── config.ini                 # Stores Base URL, Credentials, and Environment Variables
├── pageObjects/                   # Page Object Model (POM) Implementation
│   ├── base_page.py               # Reusable wrapper methods for Selenium actions
│   ├── Home_Page.py               # Homepage navigation logic
│   ├── login_Page.py              # Authentication & verification logic
│   ├── Account_Page.py            # Dashboard & navigation components
│   └── AccountRegistrationPage.py # Sign-up flow management
├── testCases/                     # Pytest Test Suite
│   ├── conftest.py                # Fixtures for browser lifecycle and reporting hooks
│   ├── pytest.ini                 # Custom Pytest configurations and markers
│   ├── test_001_Reg.py            # Functional sign-up test
│   ├── test_002_Login.py          # Basic authentication test
│   └── test_003_ddtLogin.py       # Advanced Excel-driven testing
├── testData/                      # External Data Management
│   └── Opencart_LoginData.xlsx    # Test data for DDT
├── utilities/                     # Reusable Helper Modules
│   ├── readProperties.py          # Configuration parser
│   ├── custom_Logger.py           # Execution tracking engine
│   ├── XLUtils.py                 # Excel Helper Utilities
│   └── randomString.py            # Dynamic data generator
├── Logs/                          # Runtime Traceability (automation.log)
├── reports/                       # Historical Execution Evidence
│   └── YYYY-MM-DD_HH-MM-SS/       # Isolated folder for each unique run
│       ├── HtmlReports/           # Visual test summary
│       └── screenshots/           # Evidence captured during failures
├── requirements.txt               # Project dependency manifest
├── run.bat                        # One-click Suite Execution
└── install_packages.bat           # One-click Environment Setup
