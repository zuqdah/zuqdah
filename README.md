## Ziyad Uqdah

**Senior Systems Engineer | Cloud, Data Platforms & Analytics | DevOps, Migrations & Integrations.** New Orleans, LA · [ziyaduqdah.com](https://ziyaduqdah.com) · [LinkedIn](https://www.linkedin.com/in/ziyaduqdah)

19+ years across systems administration, infrastructure engineering, and cloud architecture. My work sits on the parts of a migration that carry real risk: estate discovery, wave planning, cutover, and disaster recovery that has been tested rather than assumed.

### What's in these repos

Labs, each built end to end as code and each ending in a test that can fail. The common thread is that the claim gets checked rather than asserted — and that the write-up says what the build got wrong along the way.

**Cloud & hybrid architecture**
- [azure-agent-landing-zone](https://github.com/zuqdah/azure-agent-landing-zone) — a Terraform landing zone deployed by GitHub Actions with no stored cloud credentials; every hop on managed identity, spend bounded by design
- [entra-cutover-without-lockout](https://github.com/zuqdah/entra-cutover-without-lockout) — Conditional Access evaluated against a declared sign-in matrix before enforcement: 7 of 7 scenarios as declared, 0 lockouts
- [least-privilege-proven](https://github.com/zuqdah/least-privilege-proven) — RBAC in Terraform, then each identity signs in and attempts what it must not; the pipeline fails if anything succeeds
- [the-upgrade-succeeded](https://github.com/zuqdah/the-upgrade-succeeded) — an AKS upgrade that Azure reported as Succeeded while 181 requests failed in two 30-second outages; the same upgrade with the manifest fixed: zero failures

**Migrations & cutover**
- [sql-migration-with-rollback](https://github.com/zuqdah/sql-migration-with-rollback) — refuses a source that is not migratable, proves parity by content checksum rather than row count, and restores the rollback to show it works
- [before-the-first-sync](https://github.com/zuqdah/before-the-first-sync) — everything that has to be right before a forest syncs to Entra ID, checked against a real forest built from scratch and torn down in the same job

**Data platforms & analytics**
- [the-database-was-not-busy](https://github.com/zuqdah/the-database-was-not-busy) — an Azure SQL database held at 98% of its log-write ceiling while reporting 8% CPU; the throttled workload was the fastest of the three
- [queries-that-quietly-fell-back](https://github.com/zuqdah/queries-that-quietly-fell-back) — a Direct Lake model that silently fell back to DirectQuery, and the one API able to detect it cannot be put in a pipeline
- [the-rows-that-failed-and-loaded-anyway](https://github.com/zuqdah/the-rows-that-failed-and-loaded-anyway) — a Databricks pipeline declared two constraints, reported COMPLETED, and loaded all 340 rows that broke them

**DevOps & automation**
- [pipelines-that-refuse](https://github.com/zuqdah/pipelines-that-refuse) — branch policies, review rules and environment approvals with every bypass attempted for real against a live project, and graded
- [the-second-run-changed-nothing](https://github.com/zuqdah/the-second-run-changed-nothing) — Ansible idempotence measured against a host fingerprint, because `changed=0` is wrong in both directions
- [windows-baseline-automation](https://github.com/zuqdah/windows-baseline-automation) — a legacy hardening script turned into a tested module that audits, remediates only drift, and supports `-WhatIf`, with no RDP and no credentials on the wire

**Integrations & resilience**
- [integration-that-survives-failure](https://github.com/zuqdah/integration-that-survives-failure) — duplicate delivery, poison messages and a consumer dying mid-work, each provoked and survived against a real Service Bus namespace
- [disaster-recovery-actually-failed-over](https://github.com/zuqdah/disaster-recovery-actually-failed-over) — a cross-region failover with recovery time measured from the first failed write and data loss counted, not quoted, graded against the objectives the plan claims

**AI platforms & low-code governance**
- [agentic-ops-copilot](https://github.com/zuqdah/agentic-ops-copilot) — an agent that investigates Azure through an MCP server and cannot change anything without a human approving it; the model never approves its own actions
- [self-healing-aiops](https://github.com/zuqdah/self-healing-aiops) — an agent diagnoses, policy (not the model) decides whether the fix may run unattended, and every incident is measured in time-to-recovery and dollars
- [copilot-studio-alm](https://github.com/zuqdah/copilot-studio-alm) — a Copilot Studio agent kept as source in git and promoted dev to prod by a script that reports what it will change before it changes it
- [the-import-said-success](https://github.com/zuqdah/the-import-said-success) — a managed Power Platform import that reports success, advances the version, and changes nothing; the hand edit in the target wins

Each ships its code, its tests, and a write-up of what was proven — including the bugs the build found in itself. Every lab is verified against the live platform it is about; anything that bills is torn down the same day, and the few that persist run on permanently free tiers. The same labs, grouped the same way, are on [ziyaduqdah.com](https://ziyaduqdah.com/#focus).

📫 [ziyad@ziyaduqdah.com](mailto:ziyad@ziyaduqdah.com)
