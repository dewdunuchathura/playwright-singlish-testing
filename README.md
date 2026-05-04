# Playwright Test Automation for Singlish Chat Translator

## Project Overview

This project automates testing for the Singlish to Sinhala chat translator using Playwright and Python. The script reads test cases from an Excel file, sends each Singlish input to the web app, captures the translated output, and writes the result back into the Excel sheet with a status.

## Technologies Used

- Python
- Playwright
- OpenPyXL

## Project Structure

```text
playwright-singlish-testing/
|-- README.md
`-- test_automation/
    |-- test_automation.py
    `-- Assignment 1 - Test cases.xlsx
```

## Setup Instructions

### 1. Install Python

Use Python 3.10 or newer.

Check your version:

```powershell
python --version
```

### 2. Install Dependencies

```powershell
pip install playwright openpyxl
```

### 3. Install Playwright Browsers

```powershell
python -m playwright install
```

## How to Run

From the project root, run:

```powershell
python test_automation/test_automation.py
```

The script already uses these defaults:

- Excel file: `test_automation/Assignment 1 - Test cases.xlsx`
- URL: `https://www.pixelssuite.com/chat-translator`
- Sheet name: ` Test cases`

## Example Command With Options

```powershell
python test_automation/test_automation.py --excel "test_automation/Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 30 --slow-mo-ms 0 --save-every 1
```

## Useful Command Options

- `--excel` to choose a different Excel file
- `--sheet` to target a specific sheet
- `--url` to test a different frontend URL
- `--wait-ms` to control the wait after clicking transliterate
- `--retries` to retry reading the output
- `--retry-wait-ms` to set delay between retries
- `--type-delay-ms` to slow down typing
- `--timeout-ms` to change Playwright timeout
- `--slow-mo-ms` to slow browser actions for visibility
- `--save-every` to save progress during execution
- `--headless` to run without opening the browser UI
- `--keep-open` to leave the browser open after the run

## Output

The script updates the Excel file with:

- Actual output
- Status such as `PASS`, `FAIL`, `COLLECTED`, or `UI Error`

If output and status columns do not already exist, the script can create them automatically.

## Important Notes

- Keep the Excel file closed while the script is running
- Avoid interacting with the browser during execution
- Keep your internet connection stable

## Default Target

The script is currently configured to test:

`https://www.pixelssuite.com/chat-translator`
