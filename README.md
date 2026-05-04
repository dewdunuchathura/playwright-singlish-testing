# Playwright Test Automation for Singlish Chat Translator

## Project Overview

This project automates the testing of a frontend-only Singlish to Sinhala chat translator using Playwright. It reads test cases from an Excel file, inputs them into the web application, captures the output, and compares it with expected results.

---

## Technologies Used

* Python
* Playwright
* OpenPyXL

---

## Project Structure

```
.
├── test_automation.py
├── Assignment 1 - Test cases.xlsx
├── README.md
```

---

##  Setup Instructions

### 1. Install Python

Make sure Python 3.10+ is installed.

Check:

```
python --version
```

---

### 2. Install Dependencies

Run:

```
pip install playwright openpyxl
```

---

### 3. Install Playwright Browsers

Run:

```
playwright install
```

---

# How to Run the Script

Run the following command:

```
python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1
```

---

## Output

* The script updates the Excel file with:

  * Actual output
  * Status (PASS / FAIL)

---

##  Important Notes

* Ensure Excel file is CLOSED before running
* Do not modify the browser while script is running
* Keep internet connection stable

---

## Repository Access

This repository is public and accessible for evaluation.
