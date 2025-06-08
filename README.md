### 📦 Mamram Rules 

### 📦 CI Pipeline with GitHub Actions

This repository includes a basic **Continuous Integration (CI)** pipeline using **GitHub Actions**.

#### 🔁 Trigger Conditions

The pipeline runs automatically:

* On every push to the `master` branch
* On pull requests targeting the `master` branch

#### 🔨 Job: `build`

Runs on: `ubuntu-latest`

**Steps:**

1. ✅ **Checkout code** – Uses the official `actions/checkout@v3` to pull the code.
2. 💬 **Run sample command** – Executes a simple `echo` command as a placeholder for real tasks.

```yaml
name: CI Pipeline

on:
  push:
    branches: [ master ]
  pull_request:
    branches: [ master ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v3
        
      - name: Run a sample command
        run: echo "Hello from CI!"
```

---

You can later replace the sample step with:

* Linting
* Unit tests
* Build artifacts
* Deployment scripts
