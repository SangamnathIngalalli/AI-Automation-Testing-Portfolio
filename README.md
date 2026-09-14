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

| #  | Project                      | Description                                                     | Status      | Links                                                                         |
| -- | ---------------------------- | --------------------------------------------------------------- | ----------- | ----------------------------------------------------------------------------- |
| 01 | **LLM Testing Fundamentals** | Foundational functional testing of an LLM-powered application   | ✅ Completed | [Repository](https://github.com/SangamnathIngalalli/llm-testing-fundamentals) |
| 02 | **DeepEval LLM Evaluation**  | Automated semantic evaluation using DeepEval and LLM-as-a-Judge | ✅ Completed | [Repository](https://github.com/SangamnathIngalalli/deepeval-llm-evaluation)  |

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

| Category             | Purpose                                         |
| -------------------- | ----------------------------------------------- |
| ✅ Happy Path         | Validate expected user interactions             |
| ❌ Negative Inputs    | Validate invalid or unexpected inputs           |
| 🈳 Empty Input       | Test blank and missing input                    |
| 📏 Long Input        | Validate behavior with large prompts            |
| 🔍 Edge Cases        | Test unusual boundary conditions                |
| 🌐 Out-of-Domain     | Validate unsupported questions                  |
| 🔄 Prompt Variations | Test different ways of asking the same question |
| ⚠️ Error Handling    | Validate application behavior during failures   |

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

| Category      | Test Cases |
| ------------- | ---------: |
| Happy Path    |         15 |
| Negative      |          3 |
| Out-of-Domain |          2 |
| Safety        |          2 |
| Ambiguous     |          2 |
| **Total**     |     **25** |

### 📊 Evaluation Metrics

| Metric                  | Purpose                                                     |
| ----------------------- | ----------------------------------------------------------- |
| **Answer Relevancy**    | Measures whether the response addresses the user's question |
| **GEval Correctness**   | Evaluates correctness of the generated answer               |
| **GEval Safety**        | Evaluates whether the response meets safety expectations    |
| **GEval Out-of-Domain** | Evaluates handling of unsupported questions                 |

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

### 🏗️ Project Structure

```text
deepeval-llm-evaluation/
│
├── app/
│   ├── claude_client.py
│   └── deepeval_config.py
│
├── tests/
│   ├── test_deepeval_smoke.py
│   └── test_deepeval_llm.py
│
├── test_data/
│   ├── deepeval_llm_cases.json
│   └── failures.md
│
├── reports/
│
└── .env
```

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

# 🔗 How the Projects Connect

The two projects demonstrate two complementary layers of AI testing:

```text
┌──────────────────────────────────────┐
│       AI / LLM Application           │
└──────────────────┬───────────────────┘
                   │
                   ▼
┌──────────────────────────────────────┐
│  Project 01                          │
│  LLM Testing Fundamentals            │
│                                      │
│  "Does the application behave        │
│   correctly?"                        │
└──────────────────┬───────────────────┘
                   │
                   ▼
┌──────────────────────────────────────┐
│  Project 02                          │
│  DeepEval LLM Evaluation             │
│                                      │
│  "How good is the AI response?"      │
└──────────────────────────────────────┘
```

### Testing Progression

**Functional Testing → Semantic Evaluation**

Project 01 establishes the foundation for testing an LLM application.

Project 02 builds on that foundation by introducing automated evaluation of **response quality and semantic behavior**.

---

# 🧰 Skills Demonstrated

| Area                    | Skills                          |
| ----------------------- | ------------------------------- |
| **Programming**         | Python                          |
| **Test Automation**     | Pytest                          |
| **LLM Testing**         | Functional & Behavioral Testing |
| **LLM Evaluation**      | DeepEval                        |
| **AI Evaluation**       | LLM-as-a-Judge                  |
| **API Testing**         | Claude API                      |
| **Test Design**         | Positive, Negative & Edge Cases |
| **Quality Engineering** | Failure Analysis & Validation   |
| **Reporting**           | HTML Test Reports               |
| **AI Quality**          | Relevancy, Correctness & Safety |

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
