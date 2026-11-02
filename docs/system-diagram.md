# System Diagram - crontrack-cli

```
+-----------------------------------------------------------------------+
|                           crontrack-cli                               |
+-----------------------------------------------------------------------+
                                    |
            +-----------------------+-----------------------+
            |                                               |
            v                                               v
+-----------------------+                       +-----------------------+
|    Crontab Parser     |                       | Process & Log         |
|                       |                       | Collector             |
|  - Parse system &     |                       |                       |
|    user crontabs      |                       |  - `ps`, `grep`, `awk`|
|  - Read schedule specs|                       |  - Inspect log files  |
+-----------------------+                       +-----------------------+
            |                                               |
            +-----------------------+-----------------------+
                                    |
                                    v
                        +-----------------------+
                        |      JSON Engine      |
                        |                       |
                        |  - Structure data with|
                        |    `jq`               |
                        |  - Export state report|
                        +-----------------------+
                                    |
                                    v
                        +-----------------------+
                        | ANSI Terminal         |
                        | Dashboard             |
                        |                       |
                        |  - Real-time terminal |
                        |    status UI (`tput`) |
                        |  - Colorized feedback |
                        +-----------------------+
```

## Description
1. **Crontab Parser**: Reads schedule configurations and command definitions from crontab settings.
2. **Process / Log Collector**: Queries active process status via system utilities (`ps`, `grep`, `awk`) and parses relevant log files.
3. **JSON Engine**: Combines schedule and process execution data into structured JSON objects via `jq`.
4. **ANSI Terminal Dashboard**: Formats and outputs live monitoring information to stdout using ANSI terminal escape codes and `tput`.
