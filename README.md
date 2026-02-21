# SOC Alert Investigation Project (Online SIEM)

## Platform Used
LetsDefend (Online SOC Simulation Platform)

## Objective
To investigate a security alert generated in a SIEM environment and determine whether it is a True Positive or False Positive.

## Alert Details
- Alert Name: CVE-2024-49138 Exploitation Detected
- Severity: Medium
- Detection Source: Windows Host Logs

## Investigation Steps

1. Reviewed alert summary and severity level.
2. Checked affected host and user details.
3. Analyzed process execution logs.
4. Observed suspicious file path:
   C:\temp\service_installer\svchost.exe
5. Verified parent process (powershell.exe).
6. Checked threat intelligence indicators.

## Analysis

- The file name mimics legitimate Windows process (svchost.exe).
- Executed from temporary directory (unusual behavior).
- Parent process PowerShell indicates possible malicious execution.

## Verdict

True Positive – Malicious activity detected.

## Recommended Actions

- Isolate affected machine.
- Remove malicious file.
- Reset user credentials.
- Monitor for further suspicious activity.

## Skills Demonstrated

- SIEM Log Analysis
- Threat Investigation
- Incident Reporting
- Windows Process Analysis
- SOC Workflow Understanding

## Learning Outcome

Gained hands-on experience in analyzing alerts in a simulated SOC environment and identifying malicious behavior using log data.
