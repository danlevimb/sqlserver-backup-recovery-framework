# SQL Server Automated Backup & Recovery Framework

A production-oriented framework to automate **backup, verification, retention cleanup, and restore workflows** for Microsoft SQL Server.  
Designed to demonstrate DBA best practices around **RPO/RTO**, reliability, and operational discipline.

## Key Features
- Full / Differential / Transaction Log backup automation
- Backup verification and integrity checks
- Retention cleanup (policy-based)
- Restore runbook (full, full+diff, point-in-time)
- Logging and audit trail of operations
- SQL Agent job templates for scheduling

## Tech Stack
- Microsoft SQL Server (2016+ recommended; tested on 2022 Developer Edition)
- T-SQL
- SQL Server Agent (jobs & schedules)

## Repository Structure
- `docs/` → documentation & runbooks
- `scripts/` → backup/restore scripts and support objects
- `jobs/` → SQL Agent job scripts/exports
- `config/` → configurable variables/templates
- `samples/` → demo walkthrough and sample database setup

## Quick Start (Local Demo)
1. Create a test database using `samples/sample_db_setup.sql`
2. Run prerequisites in `scripts/00-prerequisites/`
3. Configure variables in `config/variables.example.sql`
4. Execute a full backup from `scripts/01-backups/full_backup.sql`
5. Validate using `scripts/01-backups/verify_backups.sql`

## RPO / RTO Strategy
See `docs/02-rpo-rto-strategy.md`

## Restore Runbook
See `docs/03-restore-runbook.md`

## License
MIT
