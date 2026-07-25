# 🐞 BugRepro

> **AI-powered bug reproduction and debugging assistant that reproduces software bugs, generates patch suggestions, verifies fixes through regression testing, and produces comprehensive debugging reports.**

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Docker](https://img.shields.io/badge/Docker-Sandbox-2496ED.svg)
![Status](https://img.shields.io/badge/Status-Active-success.svg)

---

# 🚀 Overview

BugRepro is an AI-powered debugging assistant designed to automate one of the most time-consuming parts of software development: reproducing, analyzing, and validating software bugs.

Instead of simply suggesting code changes, BugRepro follows a structured workflow that reproduces issues, securely executes them inside an isolated Docker sandbox, localizes failures, generates patch suggestions, validates fixes through automated regression testing, and produces detailed debugging reports.

---

# ✨ Features

### 🐞 Automated Bug Reproduction

* Generates reproduction steps from issue descriptions
* Executes reproduction automatically
* Confirms whether the reported issue is reproducible

### 🐳 Secure Docker Sandbox

* Isolated execution environment
* No network access
* CPU, memory, and process limits
* Disposable containers for safer execution

### 🔍 Failure Localization

* Stack trace analysis
* Repository scanning
* Symbol and file matching
* Source code localization

### 🤖 AI Patch Generation

* Generates unified Git diffs
* Explains proposed fixes
* Preserves the original repository

### ✅ Regression Testing

* Applies generated patches to a temporary copy
* Executes the project's test suite
* Detects regressions before recommending a fix

### 📄 Debug Reports

Automatically generates structured reports containing:

* Reproduction status
* Execution logs
* Stack traces
* Failure analysis
* Generated patches
* Regression test results

---

# 🏗️ Architecture

```text
Issue Report
      │
      ▼
AI Reproduction Generator
      │
      ▼
Docker Sandbox
      │
      ▼
Execution Verification
      │
      ▼
Failure Localization
      │
      ▼
Patch Generation
      │
      ▼
Regression Testing
      │
      ▼
Debug Report
```

---

# 🛠 Tech Stack

* Python
* Docker
* Git
* Pytest
* AI / Large Language Models (LLMs)
* Static Analysis
* JSON
* Unified Diff
* Subprocess

---

# 📂 Project Structure

```text
BugRepro/
│
├── bugrepro/
│   ├── sandbox.py
│   ├── regression.py
│   ├── repo_scan.py
│   ├── reporter.py
│   ├── patch_generator.py
│   └── ...
│
├── tests/
├── docs/
├── README.md
└── requirements.txt
```

---

# ⚙️ Installation

```bash
git clone https://github.com/<your-username>/BugRepro.git

cd BugRepro

pip install -r requirements.txt
```

For secure execution, install Docker and ensure it is running before using sandbox mode.

---

# ▶️ Usage

```bash
python main.py
```

or

```bash
python cli.py --issue issue.txt --repo /path/to/repository
```

> Update the commands above if your project's entry point differs.

---

# 🔒 Security

BugRepro executes reproduction scripts inside an isolated Docker environment to reduce the risks associated with running AI-generated code.

Current safeguards include:

* Docker-based isolation
* Disabled network access
* Resource limits
* Temporary workspaces
* Original repository protection
* Patch verification through regression testing

---

# 🎯 Why BugRepro?

Most debugging tools stop after identifying an error.

BugRepro goes a step further by automating the complete debugging workflow:

* Reproduce the issue
* Verify the failure
* Analyze the root cause
* Generate a patch suggestion
* Validate the fix
* Produce a detailed debugging report

The result is a faster, safer, and more reproducible debugging process.

---

# 🚀 Future Improvements

* AST-based repository indexing
* Call graph analysis
* Multi-language support
* GitHub Actions integration
* IDE extensions
* Interactive web dashboard
* Smarter repository understanding

---

# 🤝 Contributing

Contributions, feature requests, and bug reports are welcome.

If you have ideas for improving BugRepro, feel free to open an issue or submit a pull request.

---

# ⭐ Support

If you found BugRepro useful or interesting, consider giving the repository a ⭐.

Feedback, suggestions, and contributions are always appreciated.
