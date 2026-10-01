# Evidence Checklist

Use this checklist to capture evidence without claiming completion before the task is actually performed.

| Activity | Evidence to capture |
|---|---|
| 01 | Directory tree or recursive listing showing `linux_lab`, `docs`, `scripts`, and the resulting files; show `readme.txt` contents if useful. |
| 02 | `readme.txt` after editing; `head`, `tail`, `wc`, and `grep` outputs. |
| 03 | `ls -l secure.txt` showing the requested permission/ownership states. If you demonstrate both permission states, capture both. |
| 04 | `backup_test` contents, archive creation/compression, restored directory contents, and verification. |
| 05 | `jobs` output, foreground-job state as applicable, PID termination, `ps aux | grep sleep`, and `top`. |
| 06 | `ip a`, successful `ping google.com -c 4`, listening ports, hostname, `/etc/hosts` entry, and successful `ping testsite.local`. |
| 07 | `find` result for `readme.txt`, grep results in `docs`, recent-file search, and `.txt` count. |
| 08 | `apt update`, `tree --version`, package removal, and `packages.txt` evidence. |
| 09 | `hello.sh` contents, executable permission, and script output. |
| 10 | `df -h`, `free -h`, last 10 log entries, `uptime`, `who`, and `lscpu`. |

## Evidence Rules

- Capture only evidence from your own Linux environment.
- Do not fabricate or edit terminal output to make a task appear complete.
- If a command cannot be run because of permissions, distribution differences, or unavailable files, record the issue in the activity documentation.
- Avoid exposing passwords, tokens, private keys, or other sensitive information in screenshots.
