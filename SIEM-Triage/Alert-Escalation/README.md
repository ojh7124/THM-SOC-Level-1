<img width="1897" height="1032" alt="Screenshot (461)" src="https://github.com/user-attachments/assets/f4d4271f-65f3-459c-b9ad-ebc05ee2d40f" />

### Why I Escalated This Incident to Tier 2

* **Confirmed Active Attack:** The process tree confirmed commands were executed by a malicious reverse shell (`C:\Users\Public\revshell.exe`), proving an attacker had live remote control over the server.
* **High-Value Target at Risk:** The compromised host was `DMZ-MSEXCHANGE-2013` running with full `NT AUTHORITY\SYSTEM` administrative privileges, giving the attacker complete local control over a critical server.
* **Threat of Lateral Movement:** The attacker was actively gathering internal intelligence (`net group "Domain Admins"`, `nltest`) to target Domain Controllers and expand their access across the network.
* **Response Beyond L1 Scope:** Containing an active breach requires network-level host isolation, killing malicious process trees, and conducting deep web-server forensics—remediation actions that fall directly under Tier 2 / Incident Response duties.
