# Sigma Rules for Detection Engineering

Custom Sigma rules I wrote while learning detection engineering.

## Rules

| Rule | Description | MITRE Tactic | Level |
|------|-------------|--------------|-------|
| `failed_logons_sigma.yml` | Detects 5+ failed logons within 60 seconds | Credential Access (T1110) | Medium |
| `admin_login_sigma.yml` | Detects administrator login (EventID 4672) | Privilege Escalation (T1078) | High |
| `service_stopped_sigma.yml` | Detects when a Windows service stops | Impact (T1489) | Medium |
| `failed_sudo_sigma.yml` | Detects failed sudo attempts on Linux | Privilege Escalation (T1548) | Medium |

## How to Use

1. Copy any `.yml` file
2. Go to [uncoder.io](https://uncoder.io)
3. Paste the rule
4. Convert to your SIEM (Splunk, Elastic, QRadar)

## Author

Sidharth — linkedin.com/in/sidharth-sanwariya-3a33a5379

## Tags

`#cybersecurity` `#detection-engineering` `#sigma-rules` `#soc`
