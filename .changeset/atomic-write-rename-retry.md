---
"@nanocollective/nanocoder": patch
---

Fix writes of app data files (artifacts, memory, stats, timeline, the daemon lockfile) failing with `EPERM` on Windows when two writes replace the same file at once. The final rename now retries briefly on a Windows sharing violation, as the session index already did. Closes #2347.
