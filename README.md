I've prepared the **Copilot Sonnet 4.6 prompt as a Markdown file**. It is specifically designed for your situation with multiple isolated `.NET 10` solutions/projects and a **single standardized audit contract/framework** across all applications.

[Download the Copilot Audit Framework Prompt](sandbox:/mnt/data/common_audit_framework_copilot_prompt.md)

The prompt makes Copilot:

* Analyze **all solutions and `.csproj` files first**
* Build **one reusable audit framework**
* Enforce **one canonical audit schema** across every application
* Support both **UI/API actions and Step Functions**
* Capture **record-level actions**
* Correlate `recordId`, `operationId`, `correlationId`, and Step Functions execution IDs
* Support a centralized **DynamoDB audit table + Splunk pipeline**
* Handle retries/idempotency
* Keep Splunk-specific implementation out of business logic
* Work with your **VSA + Clean Architecture**
* Add **contract tests** so one application cannot silently produce a different audit format
* Require Copilot to **analyze first and wait for approval before implementation**.

