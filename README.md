SOC Alert Investigation Project (Online SIEM)
Platform Used

LetsDefend – Online SOC Simulation Platform

Objective

The goal of this project was to investigate a security alert in a SIEM environment and determine whether it was a True Positive or False Positive.

Alert Information

Alert Name: CVE-2024-49138 Exploitation Detected

Severity: Medium

Log Source: Windows Host Logs

Investigation Process

Checked the alert summary and understood why it was generated.

Reviewed the affected system and user details.

Analyzed the process execution logs.

Found a suspicious file path:

C:\temp\service_installer\svchost.exe

Checked the parent process and saw it was executed by PowerShell.

Compared the behavior with normal Windows processes.

Analysis

The file name svchost.exe looks like a legitimate Windows process.

However, it was running from the temp folder, which is not normal.

The parent process was PowerShell, which is commonly used in attacks.

Attackers often copy names of real system files to hide malware.

This behavior indicates suspicious activity.

Final Decision

After analyzing all logs and behavior, I concluded that this alert is a True Positive because it shows signs of malicious execution.

Recommended Actions

Isolate the affected system

Remove the suspicious file

Reset user credentials

Monitor the system for further suspicious activity

Skills Practiced

SIEM Alert Investigation

Log Analysis

Windows Process Analysis

Threat Identification

Incident Reporting

Learning Outcome

In this project, I gained hands-on experience investigating a SOC alert.
I learned how attackers disguise malware using legitimate process names.
This helped improve my analytical and investigation skills
