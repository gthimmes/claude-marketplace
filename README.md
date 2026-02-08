# Claude Skills Marketplace

Engineering leadership skills for [Claude Code](https://claude.ai/code) — analyze tech debt, remediate CVEs, modernize legacy code, and document databases.

## Installation

Add this marketplace once to access all skills:

```
/plugin marketplace add gthimmes/claude-marketplace
```

Then install any skill:

```
/plugin install tech-debt-analyzer
/plugin install jvm-spring-remediator
/plugin install data-dictionary-generator
/plugin install legacy-analyzer
/plugin install tdd
```

---

## Skills

### 📊 Tech Debt Analyzer

Analyze codebases for technical debt and translate findings into business impact with ROI calculations.

**Use when:** You need to justify refactoring work to executives, prioritize tech debt, or quantify the cost of bad code.

```
User: Analyze my codebase for technical debt

Claude: Overall AI Debt Score: 58/100 (MODERATE)
        Annual Cost: $1.24M
        
        Top Priority: UserService.java (Score: 87/100 - CRITICAL)
        Fix: $45K → Saves $195K/year (1,200% ROI)
```

[View repo →](https://github.com/gthimmes/claude-tech-debt-analyzer)

---

### 🔒 JVM Spring Remediator

Analyze and remediate CVE vulnerabilities in Java/Kotlin Spring Boot applications with minimal-impact fixes.

**Use when:** You have a CVE to fix in a Spring Boot app and want exposure assessment + safe remediation.

```
User: /remediate CVE-2024-38816

Claude: Severity: CRITICAL (CVSS 9.8)
        Your Version: 5.3.27 → Recommended: 5.3.39
        Exposure: MEDIUM - RouterFunction usage found
        
        [Applies fix, generates test plan]
```

[View repo →](https://github.com/gthimmes/claude-jvm-spring-remediator)

---

### 📖 Data Dictionary Generator

Generate comprehensive data dictionaries by analyzing database schemas, migration files, backend/frontend code, and documentation.

**Use when:** You need to document your database schema with business context, validation rules, and relationships.

```
User: Generate a data dictionary for our user tables

Claude: [Analyzes PostgreSQL schema, Kotlin entities, TypeScript types]
        
        Table: users
        - id (bigint): Primary key, auto-generated
        - email (varchar): Validated: @Email, unique per tenant
        - Validation (Frontend): z.string().email()
```

[View repo →](https://github.com/gthimmes/claude-data-dictionary-generator)

---

### 🔧 Legacy Analyzer

AI-powered legacy code analysis and modernization for any programming language.

**Use when:** You have gnarly legacy code that needs refactoring, test generation, or architectural review.

```
User: Analyze ~/code/legacy-app for modernization

Claude: This class has 3 responsibilities that should be separated:
        1. User Validation (lines 45-120) → Extract to UserValidator
        2. Email Notifications (lines 121-180) → Extract to EmailService
        
        Here's the refactored code: [shows implementation]
```

[View repo →](https://github.com/gthimmes/claude-legacy-analyzer)

---

### 🧪 TDD Workflow Skill

Enforce strict Test-Driven Development with autonomous iteration until all tests pass.

**Use when:** You want to implement features following TDD principles with comprehensive test coverage.

```
User: /tdd implement user authentication with JWT

Claude: [Spawns sub-agent to write tests first]

        🔄 TDD Iteration 1/5: Running tests...
        Tests: 15 failing → Implementing UserService

        🔄 TDD Iteration 2/5: Running tests...
        Tests: 3 failing → Adding JWT token generation

        ✅ TDD COMPLETE - All 15 tests passing
```

[View repo →](https://github.com/gthimmes/claude-tdd-skill)

---

## About

These skills are designed for **engineering leaders** who need to:

- Translate technical problems into business language
- Make data-driven decisions about tech debt and security
- Document and modernize legacy systems
- Communicate ROI to executives

All skills run locally within Claude Code — your code stays private.

## License

MIT — use freely in your organization.

---

Built by [@gthimmes](https://github.com/gthimmes)
