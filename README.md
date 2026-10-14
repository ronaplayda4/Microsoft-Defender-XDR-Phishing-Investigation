# Microsoft Defender XDR — Phishing Email Investigation

### SOC Analyst Portfolio Project | Microsoft 365 Security

## Project Overview

This project documents an authorized phishing email investigation conducted in a Microsoft 365 lab environment as part of the **30-Day MyDFIR Microsoft SOC Analyst Challenge**.

The objective was to evaluate Microsoft Defender's ability to identify and quarantine a suspicious email and use Microsoft Defender XDR Advanced Hunting to investigate the security events.

The simulated attack involved a refund-themed email designed to encourage a recipient to click a verification link.

## Tools & Technologies

- Microsoft Defender XDR
- Microsoft 365 Security
- Microsoft Defender Quarantine
- Kusto Query Language (KQL)
- Advanced Hunting
- Email Authentication Analysis (SPF, DKIM, DMARC)
- MITRE ATT&CK Framework

## Investigation Summary

**Phishing scenario:** A simulated email titled "Action Required: Your $485.75 Refund Is Pending" was sent to a controlled Microsoft 365 test mailbox.

**Detection:** Microsoft Defender classified the message as phishing and spam, identifying user impersonation and advanced filtering as detection signals.

**Initial response:** The email was blocked from normal inbox delivery and placed in quarantine.

**Threat hunting:** KQL queries were used to validate the original detection and investigate recipient URL-click activity.

**Administrative action:** The email was deliberately released by an authorized administrator during the lab exercise.

**URL interaction:** Microsoft Defender recorded one allowed click associated with the simulated refund-verification link.

## Key Findings

- Microsoft Defender successfully detected and initially quarantined the simulated phishing email.
- Advanced Hunting confirmed the original detection and quarantine action.
- SPF, DKIM, and DMARC passed, demonstrating that email authentication alone does not establish message safety.
- An authorized administrative release was verified.
- One allowed URL-click event was recorded.
- The available evidence did not establish malicious URL blocking, credential theft, malware execution, or account compromise.

## MITRE ATT&CK Mapping

**T1566 — Phishing**

The simulated email used a refund-related financial incentive and urgency to encourage recipient interaction.

## Investigation Report

[View Full SOC Phishing Investigation Report](SOC_Portfolio_Phishing_Investigation.pdf)

The PDF includes investigation findings, Microsoft Defender screenshots, KQL hunting queries, quarantine verification, URL-click evidence, and the final analyst assessment.

## Skills Demonstrated

- Security alert triage and phishing investigation
- Microsoft Defender XDR Advanced Hunting
- KQL query development and event correlation
- Email security and authentication analysis
- Quarantine and administrative-release verification
- Security evidence documentation
- SOC incident reporting

## Disclaimer

This project was completed in an authorized security lab environment for educational and portfolio purposes. The phishing email was simulated, and sensitive account information was redacted for public presentation.
