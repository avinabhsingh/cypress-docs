# 🖥️ Commands for Cypress Execution

Use the following commands to run your Cypress tests based on your needs:

---

### 1. Run All Spec Files (Headless - Default Electron)

```bash
npx cypress run
```

![Execution-1.1](images/Execution-1.1.png)

![Execution-1.2](images/Execution-1.2.png)

> **Note:** Runs all tests in headless mode using the Electron browser.

---

### 2. Run a Specific Spec File (Headless)

```bash
npx cypress run --spec cypress\e2e\demo_file.cy.js
```

![Execution-2](images/Execution-2.png)

> **Note:** Replace the path with your spec file’s relative path.

---

### 3. Run a Specific Spec File in a Specific Browser (Headless)

```bash
npx cypress run --spec cypress\e2e\demo_file.cy.js --browser chrome
```

![Execution-3](images/Execution-3.png)

> **Note:** Available browsers: `chrome`, `electron`, `firefox`, `edge`

---

### 4. Run All Spec Files in a Specific Browser (Headless)

```bash
npx cypress run --browser edge
```

![Execution-4.1](images/Execution-4.1.png)

![Execution-4.2](images/Execution-4.2.png)

---

### 5. Run a Specific Spec File With Browser UI (Headed)

```bash
npx cypress run --headed --spec cypress\e2e\demo_file.cy.js --browser chrome
```

![Execution-5](images/Execution-5.png)

> **Note:** `--headed` opens the browser instead of running in the terminal.

---

### 6. Run All Spec Files With Browser UI (Default Electron)

```bash
npx cypress run --headed
```

![Execution-6.1](images/Execution-6.1.png)

![Execution-6.2](images/Execution-6.2.png)

---
