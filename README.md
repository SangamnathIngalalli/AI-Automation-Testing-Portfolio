# 🤖 AI Automation Testing Portfolio

Welcome to my **AI Automation Testing Portfolio** — a collection of hands-on projects focused on testing, evaluating, and validating AI/LLM-powered applications.

This repository serves as a **central portfolio and resume entry point**, with each completed project linked to its dedicated GitHub repository.

---

## 🎯 Portfolio Objective

The goal of this portfolio is to demonstrate practical experience in:

* 🧪 AI / LLM Test Automation
* 🤖 LLM Application Testing
* 📊 LLM Evaluation
* 🧠 LLM-as-a-Judge
* 🔍 Functional & Semantic Validation
* 🛡️ AI Safety & Robustness Testing
* 📈 Quality Engineering for AI Systems
* 🐍 Python Test Automation
* ⚙️ Pytest-based Automation

The projects are designed around **real-world AI testing challenges**, moving from traditional functional validation toward AI-specific evaluation techniques.

---

## 📋 Projects

| # | Project | Description | Status | Links |
|---|---|---|---|---|
| 01 | **LLM Testing Fundamentals** | Foundational functional testing of an LLM-powered application | ✅ Completed | [Repository](https://github.com/SangamnathIngalalli/llm-testing-fundamentals) |
| 02 | **DeepEval LLM Evaluation** | Automated semantic evaluation using DeepEval and LLM-as-a-Judge | ✅ Completed | [Repository](https://github.com/SangamnathIngalalli/deepeval-llm-evaluation) |
| 03 | **Golden Dataset for AI Testing** | Versioned Golden Dataset with synthetic test generation, validation, pytest, and DeepEval | ✅ Completed | [Repository](https://github.com/SangamnathIngalalli/golden-dataset-ai-testing) |

---

# 🧪 Project 01 — LLM Testing Fundamentals

**Status:** ✅ Completed

### 🔗 Repository

[**View LLM Testing Fundamentals →**](https://github.com/SangamnathIngalalli/llm-testing-fundamentals)

### 📌 Overview

A foundational LLM testing project focused on building a **production-style automated test suite** for a Claude-powered AI application.

The project explores how traditional software testing concepts can be adapted for **non-deterministic LLM applications**.

### 🧪 Test Coverage

The test suite contains **20 tests across 8 categories**:

| Category | Purpose |
|---|---|
| ✅ Happy Path | Validate expected user interactions |
| ❌ Negative Inputs | Validate invalid or unexpected inputs |
| 🈳 Empty Input | Test blank and missing input |
| 📏 Long Input | Validate behavior with large prompts |
| 🔍 Edge Cases | Test unusual boundary conditions |
| 🌐 Out-of-Domain | Validate unsupported questions |
| 🔄 Prompt Variations | Test different ways of asking the same question |
| ⚠️ Error Handling | Validate application behavior during failures |

### 🏗️ Testing Approach

The project demonstrates:

* Real Claude API testing for primary application behavior
* Mocked error paths for controlled failure testing
* Pytest-based automation
* HTML test reporting
* Assertion strategies for non-deterministic outputs
* Fail-fast validation
* Separation of real LLM behavior and simulated failures

### 🛠️ Technology Stack

```text
Python
│
├── Pytest
├── Anthropic Claude API
├── Mocking
└── HTML Test Reports
```

### 💡 Key Learning

Traditional assertions such as:

```python
assert response == expected_response
```

are often insufficient for LLM applications.

LLM testing requires validating **behavior, structure, relevance, safety, robustness, and failure handling** rather than relying exclusively on exact string matching.

### 🎯 Skills Demonstrated

* LLM Functional Testing
* Test Case Design
* Negative Testing
* Edge Case Testing
* API Testing
* Mocking
* Pytest Automation
* Test Reporting
* Non-Deterministic System Testing

---

# 📊 Project 02 — DeepEval LLM Evaluation

**Status:** ✅ Completed

### 🔗 Repository

[**View DeepEval LLM Evaluation →**](https://github.com/SangamnathIngalalli/deepeval-llm-evaluation)

### 📌 Overview

The second project extends traditional LLM testing into **automated semantic evaluation** using the DeepEval framework.

Instead of checking only whether the application executes successfully, this project evaluates **the quality of the generated AI response**.

### 🧪 Evaluation Coverage

The project contains **25 evaluation test cases** across multiple categories:

| Category | Test Cases |
|---|---:|
| Happy Path | 15 |
| Negative | 3 |
| Out-of-Domain | 2 |
| Safety | 2 |
| Ambiguous | 2 |
| **Total** | **25** |

### 📊 Evaluation Metrics

| Metric | Purpose |
|---|---|
| **Answer Relevancy** | Measures whether the response addresses the user's question |
| **GEval Correctness** | Evaluates correctness of the generated answer |
| **GEval Safety** | Evaluates whether the response meets safety expectations |
| **GEval Out-of-Domain** | Evaluates handling of unsupported questions |

### 🧠 LLM-as-a-Judge

The project implements a custom Claude-based evaluator using:

```text
DeepEval
    │
    ▼
ClaudeJudge
    │
    ▼
DeepEvalBaseLLM
    │
    ▼
Claude
    │
    ▼
Evaluation Score
```

The evaluator uses an LLM to assess the quality of another LLM's response against defined evaluation criteria.

### 🛠️ Technology Stack

```text
Python
│
├── Pytest
├── DeepEval
├── Anthropic Claude API
├── LLM-as-a-Judge
└── HTML Reports
```

### 💡 Key Learning

Traditional functional testing answers:

> **"Does the application behave correctly?"**

LLM evaluation adds another important question:

> **"How good is the AI-generated response?"**

This project demonstrates how **semantic evaluation** can complement traditional test automation.

### 🎯 Skills Demonstrated

* DeepEval
* LLM Evaluation
* LLM-as-a-Judge
* Semantic Evaluation
* Custom Evaluation Metrics
* Evaluation Thresholds
* Failure Analysis
* Test Data Design
* Pytest Automation
* Automated Reporting

---

# 🏆 Project 03 — Golden Dataset for AI Testing

**Status:** ✅ Completed

### 🔗 Repository

[**View Golden Dataset for AI Testing →**](https://github.com/SangamnathIngalalli/golden-dataset-ai-testing)

### 📌 Overview

Project 03 builds a **production-style Golden Dataset** for an e-commerce customer support AI.

The project focuses on creating a reusable, schema-validated, versioned evaluation dataset that can be used for AI regression testing and LLM evaluation.

### 📊 Dataset Coverage

The current implementation contains **50 Golden test cases**:

| Source | Category | Cases |
|---|---|---:|
| Human-authored | Happy Path | 20 |
| Synthetic | Happy Path | 10 |
| Synthetic | Negative | 5 |
| Synthetic | Edge | 5 |
| Synthetic | Ambiguous | 5 |
| Synthetic | Out-of-Domain | 5 |
| **Total** | | **50** |

The current dataset covers **5 of the planned 10 test categories**. The project structure supports further expansion into positive, boundary, no-answer, adversarial, and safety categories.

### 🧪 Golden Dataset Capabilities

* Golden test case design
* Human-authored test cases
* Synthetic test generation using Claude
* Positive and negative testing
* Edge-case testing
* Ambiguous input testing
* Out-of-domain testing
* JSON Schema validation
* Pydantic data validation
* Dataset versioning
* DeepEval evaluation
* LLM-as-a-Judge
* Failure analysis
* HTML test reporting

### 🏗️ Dataset Workflow

```text
Human-authored Cases
        │
        ▼
Golden Dataset v1
        │
        ├── Schema Validation
        │
        ├── Synthetic Data Generation
        │
        ▼
Combined Golden Dataset
        │
        ▼
Pytest + DeepEval
        │
        ▼
Claude LLM Judge
        │
        ▼
Evaluation Report
```

### 🛠️ Technology Stack

```text
Python 3.11+
│
├── Pytest
├── DeepEval
├── Anthropic Claude API
├── Pydantic 2
├── JSON Schema
├── python-dotenv
└── pytest-html
```

### 📈 Current Results

| Area | Result |
|---|---|
| Dataset size | **50 cases** |
| Human-authored | **20 cases** |
| Synthetic | **30 cases** |
| Current category coverage | **5 / 10 categories** |
| Dataset validation | ✅ |
| Pytest validation | **5 / 5 passed** |
| DeepEval relevance tests | **20 / 20 passed** |
| LLM Judge | **Claude / Anthropic** |
| HTML reporting | ✅ |

> LLM-based evaluation is non-deterministic, so individual evaluation results can vary between runs.

### 🔐 Quality & Security

The project includes:

* Dataset validation before evaluation
* Versioned Golden datasets
* Failure analysis
* Threshold-based evaluation
* Synthetic-data validation
* Environment-based API key configuration
* Protection against committing secrets

API keys are kept outside the repository in `.env` and should never be committed to Git.

### 🎯 Skills Demonstrated

* Golden Dataset Design
* AI Test Data Engineering
* Synthetic Test Data Generation
* DeepEval
* LLM-as-a-Judge
* Dataset Validation
* JSON Schema
* Pydantic
* Dataset Versioning
* Failure Analysis
* Pytest Automation
* AI Quality Engineering

---

# 🔗 How the Projects Connect

These projects demonstrate a progression from functional LLM testing to structured AI evaluation and reusable Golden test data:

```text
┌─────────────────────────────────────────┐
│           AI / LLM Application          │
└────────────────────┬────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────┐
│ Project 01                              │
│ LLM Testing Fundamentals                │
│                                         │
│ "Does the application behave correctly?"│
└────────────────────┬────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────┐
│ Project 02                              │
│ DeepEval LLM Evaluation                 │
│                                         │
│ "How good is the AI response?"          │
└────────────────────┬────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────┐
│ Project 03                              │
│ Golden Dataset for AI Testing           │
│                                         │
│ "How do we build reusable evaluation   │
│  data for AI quality and regression?"   │
└─────────────────────────────────────────┘
```

### Testing Progression

**Functional Testing → Semantic Evaluation → Golden Dataset Engineering**

Project 01 establishes the foundation for testing an LLM application.

Project 02 introduces automated semantic evaluation and LLM-as-a-Judge.

Project 03 introduces **structured Golden test data, synthetic generation, validation, versioning, and reusable evaluation workflows**.

---

# 🧰 Skills Demonstrated

| Area | Skills |
|---|---|
| **Programming** | Python |
| **Test Automation** | Pytest |
| **LLM Testing** | Functional & Behavioral Testing |
| **LLM Evaluation** | DeepEval |
| **AI Evaluation** | LLM-as-a-Judge |
| **API Testing** | Claude API |
| **Test Data Engineering** | Golden Datasets & Synthetic Data |
| **Data Validation** | Pydantic & JSON Schema |
| **Test Design** | Positive, Negative, Edge & Ambiguous Cases |
| **Quality Engineering** | Failure Analysis & Validation |
| **Reporting** | HTML Test Reports |
| **AI Quality** | Relevancy, Correctness & Safety |

---

# 🛠️ Technology Stack

```text
                    AI Testing Portfolio
                           │
              ┌────────────┴────────────┐
              │                         │
           Python                    AI / LLM
              │                         │
        ┌─────┴─────┐             ┌─────┴─────┐
        │           │             │           │
      Pytest     Mocking       Claude      DeepEval
        │                         │           │
        │                    Golden Dataset   │
        │                         │           │
        └─────────────┬───────────┴───────────┘
                      │
                Test Automation
                      │
                HTML Reporting
```

---

# 👨‍💻 About Me

**Sangamnath Ingalalli**

AI / LLM Testing | Test Automation | LLM Evaluation | Quality Engineering | Python Automation | AI QA

### 🔗 Connect

* 💼 [LinkedIn](https://www.linkedin.com/in/sangamnath-ingalalli-a4b954115/)
* 🐙 [GitHub](https://github.com/SangamnathIngalalli)

---

# 🎯 Portfolio Philosophy

> **AI systems require more than traditional testing. They need validation of behavior, quality, robustness, and semantic correctness.**

This portfolio focuses on building practical testing approaches for modern AI-powered applications — combining **traditional automation techniques with AI-specific evaluation strategies**.

---

⭐ **Each project is independently documented with its implementation, test strategy, results, and learnings.**
