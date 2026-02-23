# stanton-times

> Star Citizen newsroom pipeline for source monitoring, clustering, and staged publishing.
> Status: `Production` (actively maintained)

![CI](https://github.com/zachyzissou/stanton-times/actions/workflows/baseline-ts-ci.yml/badge.svg?branch=main)
![License](https://img.shields.io/github/license/zachyzissou/stanton-times)
![Security](https://img.shields.io/badge/security-SECURITY.md-green)

## Overview
Star Citizen newsroom pipeline for source monitoring, clustering, and staged publishing.

## Problem / Value
- **Problem:** Standardizes docs and CI while preserving manual publishing control for editor safety.
- **Value:** Standardized docs and governance reduce maintenance burden and security risk.
- **Users:** Editors and maintainers operating Stanton Times automation.

## Architecture
```text
Source Inputs --> Validation --> Processing --> Delivery
              \--> Operations + Governance
```

## Features
- ✅ Source + approval + publish pipeline is present
- ✅ Operational documentation and cron guidance are present
- ✅ Baseline CI and governance files added
- ✅ Branch-aware deployment guidance included in README

## Tech Stack
- Runtime: Python 3.12 + Node tooling
- Framework: Custom Python CLI + integration scripts
- Tooling: pytest, node scripts, cron wrappers
- CI: GitHub Actions
- Storage: Local JSON/SQLite state and logs

## Prerequisites
- Git
- Language runtime aligned with repository code
- Required service credentials injected securely

## Installation
```bash
git clone https://github.com/zachyzissou/stanton-times.git
cd stanton-times
```

## Configuration
| Key | Required | Default | Notes |
| --- | --- | --- | --- |
| `BRANCH_DEFAULT` | no | `master` | Target branch policy |
| `LOG_LEVEL` | no | `info` | debug/info/warn/error |
| `APP_ENV` | no | `dev` | Use `prod` in deployment |

## Usage
```bash
npm test
```

## Testing & Quality
```bash
npm test
```


## Security
- Report issues via `SECURITY.md`.
- Never commit secrets or credentials.
- Protect default branch and require review before merge.

## Contributing
1. Branch from default branch (`main`)
2. Run checks in this repo and include outputs in PR
3. Keep PRs focused and add rationale for behavioral changes
4. Request review and obtain approval before merge

## Deployment / runbook
- Deployment target: default branch `master`
- Rollback: revert commit and redeploy previous release/tag
- Emergency: pause workflows and disable risky automation if needed

## Troubleshooting
- CI not running: verify workflow path and branch filters
- Test failures: run locally and capture logs
- Config issues: validate config files and required keys

## Observability
- Health checks: local logs and workflow status
- Alerts: PR and workflow notifications
- SLO target: timely green checks on PRs

## Roadmap
- Expand tests and automation coverage
- Add dependency updates policy and security scanning
- Improve deployment/runbook section with real endpoints

## Known Risks
- Branch naming and legacy scripts can diverge by repo
- Some repos are early-stage and may not have all checks available

## Release Notes / Changelog
- Baseline governance, deep README, and CI workflow added.

## License & contact
- License: Project-specific baseline
- Contact: @zachyzissou / Security: see SECURITY.md

_Last updated: 2026-02-23_
