# QA Automation Portfolio | Vilayat Ali Mirza

A focused index of three public QA automation projects. Start with the E-commerce framework for the latest eventual-success snapshot, then explore Banking for risk-based financial testing and GreenKart for Java/Selenium plus database automation.

## At a glance

| Project | Stack | Documented CI evidence |
|---|---|---|
| [E-commerce Playwright](https://github.com/vilayatalimirza/ecommerce-playwright-framework) | Playwright, TypeScript, GitHub Actions | **100% eventual functional success (90/90 eligible tests)** in main run #63; 98.9% passed first attempt, one retry-passed flaky test, one skipped, zero final failures |
| [Banking QA Automation](https://github.com/vilayatalimirza/banking-qa-playwright) | Playwright, TypeScript, financial invariants | **89.3% aggregate CI execution pass rate (175/196)** in featured run #45; newer run #46 is linked separately and did not pass |
| [GreenKart Selenium](https://github.com/vilayatalimirza/greenkart-selenium-framework) | Java, Selenium, TestNG, REST Assured, JDBC/MySQL | Run #33: **93/93 browser/API** and **2/2 database** executions passed in separate jobs |

These are project-specific, run-specific measures with different scopes and denominators. They should not be compared as though they were the same test set.

---

## 1. E-commerce End-to-End Automation Framework

**Purpose:** Exercise customer journeys on the public Tricentis Demo Web Shop, from authentication and catalogue browsing through cart, checkout, and account management.

**Latest main-branch evidence:** [Workflow run #63](https://github.com/vilayatalimirza/ecommerce-playwright-framework/actions/runs/44395124618)

- **100% eventual functional success: 90/90 eligible tests.**
- 89 passed on the first attempt; one address-deletion test passed on retry and remains classified as flaky; one unsupported volume-tier pricing scenario was skipped.
- Four authentication setup executions passed separately and are not part of the functional denominator.

**Architecture and implementation**
- [Architecture diagram in README](https://github.com/vilayatalimirza/ecommerce-playwright-framework#architecture-at-a-glance)
- [Architecture guide](https://github.com/vilayatalimirza/ecommerce-playwright-framework/blob/main/ARCHITECTURE.md)
- [Test suite map](https://github.com/vilayatalimirza/ecommerce-playwright-framework/blob/main/tests/README.md)
- [Known issues and reproduction notes](https://github.com/vilayatalimirza/ecommerce-playwright-framework/blob/main/KNOWN-ISSUES.md)

**Execution evidence**
- [Latest main workflow](https://github.com/vilayatalimirza/ecommerce-playwright-framework/actions/runs/44395124618)
- [Merged Playwright HTML report artifact](https://github.com/vilayatalimirza/ecommerce-playwright-framework/actions/runs/44395124618/artifacts/14469961346)
- [Machine-readable metrics artifact](https://github.com/vilayatalimirza/ecommerce-playwright-framework/actions/runs/44395124618/artifacts/14471280579)
- [Current metrics JSON](https://raw.githubusercontent.com/vilayatalimirza/ecommerce-playwright-framework/main/metrics/latest.json)

**What to inspect:** typed fixtures, Page Object Model, sharded Playwright execution, retry/flakiness reporting, merged HTML reports, and machine-readable metrics.

---

## 2. Banking QA Automation Platform

**Purpose:** Apply risk-based test design to money movement and account behaviour in the public ParaBank demo, with checks around financial invariants and failure modes.

**Featured aggregate snapshot:** [Workflow run #45](https://github.com/vilayatalimirza/banking-qa-playwright/actions/runs/44341598081)

- **89.3% aggregate CI execution pass rate: 175/196.**
- This is an execution-level aggregate across the jobs documented in that run, not a count of unique test cases.
- Expected known-defect probes that failed as expected are excluded. The project README explains the denominator, retry treatment, and visual-baseline-generation limitation.

**Newer execution status:** [Workflow run #46](https://github.com/vilayatalimirza/banking-qa-playwright/actions/runs/44390733569) is newer and its overall workflow failed. Its unit/type-check job passed 109/109; several full-suite modules and the visual-regression job failed. The 89.3% figure is explicitly tied to run #45, not represented as the newest run's result.

**Architecture and implementation**
- [Architecture diagram in README](https://github.com/vilayatalimirza/banking-qa-playwright#architecture-at-a-glance)
- [Test strategy](https://github.com/vilayatalimirza/banking-qa-playwright/blob/master/docs/TEST-STRATEGY.md)
- [Requirement traceability](https://github.com/vilayatalimirza/banking-qa-playwright/blob/master/docs/TRACEABILITY.md)
- [Defect reports](https://github.com/vilayatalimirza/banking-qa-playwright/blob/master/docs/BUG-REPORTS.md)
- [Runbook](https://github.com/vilayatalimirza/banking-qa-playwright/blob/master/docs/RUNBOOK.md)

**Execution evidence**
- [Featured aggregate run #45](https://github.com/vilayatalimirza/banking-qa-playwright/actions/runs/44341598081)
- [Run #45 merged HTML report artifact](https://github.com/vilayatalimirza/banking-qa-playwright/actions/runs/44341598081/artifacts/14444009481)
- [Run #45 audit-evidence bundle](https://github.com/vilayatalimirza/banking-qa-playwright/actions/runs/44341598081/artifacts/14444653777)
- [Newer run #46 with module/job results](https://github.com/vilayatalimirza/banking-qa-playwright/actions/runs/44390733569)
- [Run #46 merged HTML report artifact](https://github.com/vilayatalimirza/banking-qa-playwright/actions/runs/44390733569/artifacts/14469148680)
- [Run #46 audit-evidence bundle](https://github.com/vilayatalimirza/banking-qa-playwright/actions/runs/44390733569/artifacts/14467984155)

**What to inspect:** integer-minor-unit money assertions, balance invariants, risk-scored requirements, known-defect probes, negative testing, traceability, and audit evidence. Findings describe the public demo only, not vulnerabilities in a production bank.

---

## 3. GreenKart UI, API, and Database Automation

**Purpose:** Demonstrate Java/Selenium UI automation alongside standalone API examples and isolated JDBC/MySQL testing.

**Latest documented main-branch evidence:** [Workflow run #33](https://github.com/vilayatalimirza/greenkart-selenium-framework/actions/runs/43850589978)

- Browser and external Reqres API suite: **93/93 passed**.
- Isolated JDBC/MySQL suite: **2/2 passed**.
- These run in separate jobs and must not be combined into a single test total.

**Architecture and implementation**
- [Architecture diagram in README](https://github.com/vilayatalimirza/greenkart-selenium-framework#architecture-at-a-glance)
- [Architecture guide](https://github.com/vilayatalimirza/greenkart-selenium-framework/blob/master/ARCHITECTURE.md)
- [Manual testing workbook](https://github.com/vilayatalimirza/greenkart-selenium-framework/blob/master/GreenKart_TestingDOC_Enhanced.xlsx)

**Execution evidence**
- [Latest main workflow #33](https://github.com/vilayatalimirza/greenkart-selenium-framework/actions/runs/43850589978)
- [Browser/API Surefire report artifact](https://github.com/vilayatalimirza/greenkart-selenium-framework/actions/runs/43850589978/artifacts/14217935970)
- [Database Surefire report artifact](https://github.com/vilayatalimirza/greenkart-selenium-framework/actions/runs/43850589978/artifacts/14217082385)

**Scope clarification:** Reqres is an external sample API, not a GreenKart backend API. The database job uses a disposable MySQL 8 service, not the database behind the public demo.

**What to inspect:** TestNG suite separation, Selenium Page Objects, WebDriver lifecycle, REST Assured examples, JDBC helpers, SQL CRUD checks, and distinct CI reports.

---

## How to review these projects

1. Read the project README and inspect its architecture diagram.
2. Open the linked workflow and examine the job-level result.
3. Download the report or audit artifact when available.
4. Read the known limitations before interpreting a pass percentage.

**Portfolio owner:** [Vilayat Ali Mirza](https://github.com/vilayatalimirza) · [LinkedIn](https://www.linkedin.com/in/vilayat-ali-mirza/)
