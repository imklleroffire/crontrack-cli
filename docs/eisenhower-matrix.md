# Eisenhower Matrix - crontrack-cli

## Overview
This matrix categorizes tasks and features for crontrack-cli to guide development priorities.

| Quadrant | Priority | Scope / Features |
| --- | --- | --- |
| **Do First** | Urgent & Important (MVP) | - Cron Parsing<br>- Process & Log Inspection<br>- ANSI Status Dashboard<br>- Structured JSON Report Generation |
| **Schedule** | Not Urgent but Important (Future) | - Slack/Discord webhook alerts on failure<br>- Remote multi-host monitoring over SSH<br>- Interactive curses/TUI<br>- Historical execution trends |
| **Delegate** | Urgent but Not Important | - System utilities/logging wrappers<br>- OS-level daemon setup & crontab installation scripts |
| **Don't Do / Backlog** | Not Urgent & Not Important | - GUI / Desktop web app wrapper<br>- Heavy database storage engines<br>- Cloud SaaS integrations |

## Quadrant Breakdown

### 1. Do First (MVP)
- **Cron Parsing**: Parse crontab entries.
- **Process & Log Inspection**: Inspect active cron processes (`ps`, `grep`) and logs.
- **ANSI Status Dashboard**: Display job status using terminal escape codes / `tput`.
- **JSON Engine**: Generate structured JSON reports with `jq`.

### 2. Schedule (Future)
- **Failure Alerts**: Webhooks for Slack/Discord.
- **Remote Monitoring**: Multi-host monitoring over SSH.
- **Interactive TUI**: Advanced terminal interface.
- **Execution Trends**: Historical execution and performance analytics.

### 3. Delegate
- **System Utilities**: Rely on POSIX standard tools (`awk`, `sed`, `grep`, `date`).
- **Logging Wrappers**: External logging setup and rotation.

### 4. Don't Do / Backlog
- Desktop GUI or heavy web servers.
- Complex database dependencies.
