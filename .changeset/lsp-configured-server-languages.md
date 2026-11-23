---
"@nanocollective/nanocoder": patch
---

Fix an auto-discovered language server taking over the file types of a server configured in `lspServers`. A discovered server now only handles the languages no configured server claims, so the configured one keeps every language it declares. Closes #2339.
