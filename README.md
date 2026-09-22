## Ziyad Uqdah

**Senior Systems Engineer — cloud & infrastructure architecture.** New Orleans, LA · [ziyaduqdah.com](https://ziyaduqdah.com) · [LinkedIn](https://www.linkedin.com/in/ziyaduqdah)

19+ years across systems administration, infrastructure engineering, and cloud architecture. My work sits on the parts of a migration that carry real risk: estate discovery, wave planning, cutover, and disaster recovery that has been tested rather than assumed.

- **Cloud & hybrid:** Azure (primary), AWS, GCP · VMware, Hyper-V · hybrid Active Directory and Entra ID
- **Data platforms:** SQL Server and Azure SQL, PostgreSQL, MySQL, Snowflake, Databricks, Microsoft Fabric
- **Resilience:** backup and replication architecture, DR runbooks written against contractual SLA, RTO, and RPO
- **Automation:** PowerShell, Bash, CI/CD

### What's in these repos

Ten labs, each built end to end as code and each ending in a test that can fail. The common thread is that the claim gets checked rather than asserted:

**Proving a control actually holds**
- [least-privilege-proven](https://github.com/zuqdah/least-privilege-proven) — RBAC in Terraform, then every identity signs in and attempts what it should be refused
- [entra-cutover-without-lockout](https://github.com/zuqdah/entra-cutover-without-lockout) — Conditional Access deployed report-only and evaluated against a declared matrix of sign-ins before anything is enforced
- [integration-that-survives-failure](https://github.com/zuqdah/integration-that-survives-failure) — Service Bus put through duplicate delivery, poison messages, racing consumers, and replay

**Resilience under measurement**
- [disaster-recovery-actually-failed-over](https://github.com/zuqdah/disaster-recovery-actually-failed-over) — an Azure SQL estate failed over between regions for real, with recovery time measured from the first failed write and data loss counted by comparing acknowledged writes, then graded against the objectives the plan claims

**Migration and modernisation**
- [sql-migration-with-rollback](https://github.com/zuqdah/sql-migration-with-rollback) — SQL Server to Azure SQL behind a pre-flight gate, parity proven by content checksum, rollback restored and verified
- [windows-baseline-automation](https://github.com/zuqdah/windows-baseline-automation) — legacy PowerShell turned into a tested module with `-WhatIf` and proven idempotence

**AI agents in operations**
- [azure-agent-landing-zone](https://github.com/zuqdah/azure-agent-landing-zone) — Terraform landing zone for hosting agents, Container Apps behind APIM with OIDC
- [agentic-ops-copilot](https://github.com/zuqdah/agentic-ops-copilot) — multi-agent ops copilot on Azure AI Foundry, wired to real systems over MCP with approval-gated writes
- [self-healing-aiops](https://github.com/zuqdah/self-healing-aiops) — alert to diagnosis to a policy decision to a verified fix, reported in MTTR and cost
- [copilot-studio-alm](https://github.com/zuqdah/copilot-studio-alm) — a Copilot Studio agent treated as source, promoted dev to prod with drift detection

Each ships its infrastructure-as-code, its tests, and a write-up of what was proven — including the bugs the build found in itself. Every one is deployed manually, verified against live Azure, and torn down the same day. Published labs also appear on [ziyaduqdah.com](https://ziyaduqdah.com/#labs).

📫 [ziyad@ziyaduqdah.com](mailto:ziyad@ziyaduqdah.com)
