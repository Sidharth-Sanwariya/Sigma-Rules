# SIEM Queries from Sigma Rules

## Admin Login Detection (EventID 4672)

**Splunk:**
source=WinEventLog:Security EventCode=4672


**Elastic:**
event.code: "4672"


## Multiple Failed Logons (EventID 4625)

**Splunk:**
source=WinEventLog:Security EventCode=4625
| stats count by Source_Network_Address
| where count > 5


**Elastic:**
event.code: "4625"
| STATS COUNT() BY source.address
| WHERE COUNT() > 5


## Service Stopped (EventID 7036)

**Splunk:**
source=WinEventLog:System EventCode=7036 Message="stopped"


**Elastic:**
event.code: "7036" and message: "stopped"


## Failed Sudo Attempt (Linux)

**Splunk:**
source=/var/log/auth.log "sudo" "FAILED."

**Elastic:** (Not supported - Linux keyword search not available in ES|QL)
