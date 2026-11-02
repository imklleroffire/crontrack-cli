# crontrack-cli

## Project Goal
crontrack-cli solves fragmented logging and troubleshooting overhead for background scripts and cron jobs with a centralized CLI dashboard.

## MVP Scope
- Cron Parsing
- Process & Log Inspection
- ANSI Status Dashboard
- Structured JSON Report Generation

## Tech Stack
- Bash / POSIX Shell
- crontab, ps, awk, sed, grep, jq, date
- ANSI terminal escape codes / tput

## Future Plans
The 'Schedule' quadrant:
- Slack/Discord webhook alerts on failure
- Remote multi-host monitoring over SSH
- Interactive curses/TUI
- Historical execution trends

## Documentation
- [Eisenhower Matrix](docs/eisenhower-matrix.md)
- [System Diagram](docs/system-diagram.md)
