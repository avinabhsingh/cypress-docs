# 📊 Cypress Report Generation with Mochawesome

`cypress-mochawesome-reporter` is a plugin for Cypress that generates **detailed and visually appealing HTML reports** using the Mochawesome reporting library. It includes:

- ✅ **Test outcomes**: See which tests passed and which failed.
- 🕒 **Duration of tests**: Know how long each test took to complete.
- ❌ **Error messages**: Get detailed error messages with stack traces.
- 📁 **Support for parallel execution**: This helps generate reports for tests run in parallel.
- 🎨 **Customizable report layout**: Modify the appearance and structure of the generated report.

This plugin greatly enhances **test result analysis** and **reporting** for Cypress test suites.

---

## 🛠️ Steps to Install and Configure `cypress-mochawesome-reporter`

### 1. Install the Plugin

Open your terminal in the root of your Cypress project and run the following command:

```bash
npm install cypress-mochawesome-reporter --save-dev
```

This installs the `cypress-mochawesome-reporter` plugin into your project, which is necessary to generate reports.

---

### 2. Update `cypress.config.js` File

Configure Cypress to use the `cypress-mochawesome-reporter` by adding the following configuration to your `cypress.config.js` file:

```js
{
  "reporter": "cypress-mochawesome-reporter"
}
```

This specifies that Cypress should use the `cypress-mochawesome-reporter` plugin to generate HTML reports for your test runs.

---

### 3. Modify `e2e.js` for Reporter Setup

By default, Cypress uses `mochawesome-report-generator`. To switch to `cypress-mochawesome-reporter`, follow these steps:

#### a. Modify `e2e.js` File

Navigate to the `cypress/support/e2e.js` file and add the following line to register the reporter:

```js
import 'cypress-mochawesome-reporter/register';
```

#### b. Modify `cypress.config.js` to Include Plugin

Now, navigate to your `cypress.config.js` file and add the following code to hook up the reporter plugin:

```js
require('cypress-mochawesome-reporter/plugin')(on);
```

---

### 4. Customize Reporter Options (Optional)

You can customize the reporter's behavior and output in the `cypress.config.js` file by adding the following `reporterOptions` section. This allows you to control various aspects like charts, report filename, and whether to overwrite existing reports:

```js
reporterOptions: {
  charts: true,                // Enables charts for test results.
  reportFilename: 'Report',    // Specifies the name of the report file.
  overwrite: false,            // Prevents overwriting of existing reports.
  html: true,                  // Generates HTML report.
}
```
