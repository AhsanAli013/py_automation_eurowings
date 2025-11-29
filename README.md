Playwright Automation (TypeScript)
This repository contains automated tests built using Playwright and TypeScript.
The project includes both UI automation and API testing such as automating the Eurowings flight-status API.

🚀 Features
✔ Automated API testing using Playwright's request fixture
✔ UI testing support (Chromium, Firefox, WebKit)
✔ TypeScript support
✔ Clean project structure
✔ Easy to run and extend
📂 Project Structure

QA/
├── playwright.config.ts
├── flight-status-api.spec.ts      # Example API automation test
├── flight-status-tests.ts         # UI or other test files
├── package.json
├── tsconfig.json
└── tests/                         # Additional test suites

🛠️ Installation
Ensure Node.js (v16+) is installed.

npm install
Install Playwright browsers:

npx playwright install
▶️ Running Tests
Run all tests:
npx playwright test
Run a specific test file:
npx playwright test flight-status-api.spec.ts
Run tests with UI:
npx playwright test --ui
Show HTML report:
npx playwright show-report
🧪 Example: Flight Status API Test
The project includes a demo API test that:

Sends a POST request
Parses JSON response
Verifies flight details (e.g., departure TLC, destination TLC, status label)
const response = await request.post(
  'https://www.eurowings.com/flightstatus.search.flightNumber.nocache.html',
  {
    headers: { 'Content-Type': 'application/json' },
    data: {
      airlineCode: 'EW',
      departureDate: '2024-10-05',
      flightNumber: '6'
    }
  }
);
📦 Scripts (package.json)
Useful NPM scripts included:

{
  "scripts": {
    "test": "npx playwright test",
    "report": "npx playwright show-report"
  }
}
# py_automation_eurowings
