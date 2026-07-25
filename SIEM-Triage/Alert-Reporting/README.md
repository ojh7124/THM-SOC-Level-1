<img width="1894" height="1024" alt="Screenshot (460)" src="https://github.com/user-attachments/assets/8f2c7fb8-9db1-421c-8fe0-a5bc8bfde857" />


## Incident Report: Phishing Alert Triage
* **Analyst:** Level 1 SOC Analyst  
* **Severity:** Medium  
* **Verdict:** True Positive  

## Alert Summary
* **Alert Title:** Email Marked as Phishing after Delivery
* **Target Recipient:** Eddie Huffman, IT Manager (`e.huffman@tryhackme.thm`)
* **Claimed Sender:** Microsoft Support (`support@microsoft.com`)
* **Subject:** Important Update: Microsoft Teams Pricing Increase
* **Attachment:** `REPORT.rar`

## Investigation & Analysis
1. **Email Authentication Failure:** Security checks show **SPF/Fail** and **DKIM/Fail**. This confirms the sender's address was spoofed to mimic official Microsoft communications.
2. **Suspicious Attachment:** The message includes a `.rar` compressed file (`REPORT.rar`). Archives are commonly used by attackers to bypass basic email filter scanning.
3. **Urgency Tactics:** The body content attempts social engineering using high-urgency language ("600% price increase; urgent notice").
   
## Escalation & Next Steps
* **Status:** In Progress (True Positive)
* **Action Taken:** Logged comment, flagged spoofing indicators, and escalated for endpoint/mailbox triage.
* **Remediation Recommendation:** Purge the email from the recipient's inbox and verify if the archive attachment was executed on the victim's host.
