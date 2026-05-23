# Wazuh Lab

Hands-on SIEM lab: Wazuh 4.12.0 deployed via Docker Compose on WSL2, 
with a Windows endpoint agent, custom detection rules, and active response.

## What this lab demonstrates

- Wazuh single-node deployment via Docker Compose
- Windows agent enrollment and real-time event monitoring
- Raw alert stream analysis via terminal (alerts.json)
- Custom detection rule (rule 100001): Failed login → MITRE T1110 Brute Force, level 10
- Active Response: automatic firewall-drop on rule trigger (180s timeout)
- SCA: CIS Microsoft Windows 10 Enterprise Benchmark assessment (30% baseline)
- MITRE ATT&CK mapping: Defense Evasion, Initial Access, Persistence, Privilege Escalation

## Stack

Wazuh 4.12.0 · Docker Compose · WSL2 · Windows 10 endpoint · XML rule authoring

## Key files

| File | Purpose |
|---|---|
| `rules/local_rules.xml` | Custom detection rule 100001 |
| `config/active-response.xml` | firewall-drop active response config |
