🛡️ AWS Cloud Security Automation Suite
A comprehensive collection of Production-Grade Python Tools designed for automated security auditing, compliance monitoring, and threat detection within AWS environments.

🚀 Projects Overview
1. CIS Compliance Checker
Description: Audits the AWS environment against the CIS AWS Foundations Benchmark v1.4.0.

Key Features: Automated checks for Identity (IAM) and Data Storage (S3) security standards.

Impact: Ensures the infrastructure adheres to global security best practices.

2. Cloud Attack Surface Mapper
Description: Maps all internet-facing assets to identify potential entry points for attackers.

Key Features: Detects Public IPs and identifies unrestricted Security Group rules (e.g., Port 22 open to 0.0.0.0/0).

Impact: Minimizes the external attack vector of the cloud environment.

3. Cloud Backup & Disaster Recovery Validator
Description: Verifies the integrity and encryption status of AWS Backup jobs.

Key Features: Flags failed backup jobs and identifies unencrypted recovery points.

Impact: Guarantees data recoverability during Ransomware or accidental deletion events.

4. Cloud Backup Recency (RPO) Monitor
Description: Tracks the exact timestamp of the latest successful backup to monitor the Recovery Point Objective (RPO).

Key Features: Calculates the time gap since the last backup in a high-precision UTC format.

Impact: Prevents significant data loss by ensuring backups are up-to-date.

5. Cloud Resource Inventory
Description: Generates a real-time snapshot of all active resources across the AWS account.

Key Features: Lists EC2 instances, S3 buckets, and RDS databases for asset management.

Impact: Eliminates "Shadow IT" by providing 100% visibility into deployed assets.

6. CloudTrail Logging & Visibility Auditor
Description: Specifically audits AWS CloudTrail to ensure management events are being recorded.

Key Features: Checks for multi-region trail logging and log file validation.

Impact: Provides an immutable audit trail for security investigations.

7. EC2 Security Group (Firewall) Auditor
Description: Performs deep inspection of Virtual Firewall (Security Group) rules.

Key Features: Detects "Anywhere" (0.0.0.0/0) ingress rules and identifies unused security groups.

Impact: Hardens network perimeter security.

8. Forensic Logging Compliance Checker
Description: Ensures that forensic-level logging (VPC Flow Logs, DNS Logs) is enabled.

Key Features: Verifies if network-level visibility is active for deep packet/traffic analysis.

Impact: Enables rapid root-cause analysis during a security breach.

9. IAM (Identity) Auditor
Description: Audits IAM users, groups, and roles for credential hygiene.

Key Features: Identifies users without MFA, old unused access keys, and inactive accounts.

Impact: Reduces the risk of credential theft and unauthorized access.

10. IAM Privilege Escalation Detector
Description: Scans IAM policies for permissions that could lead to account takeover.

Key Features: Flags wildcard (*) permissions and dangerous API actions.

Impact: Enforces the Principle of Least Privilege (PoLP).

11. MITRE ATT&CK Threat Mapper
Description: Maps cloud security findings to the MITRE ATT&CK for Cloud framework.

Key Features: Translates technical gaps into Attacker Tactics and Techniques (e.g., Persistence, Exfiltration).

Impact: Provides high-level threat context for SOC teams and stakeholders.

12. S3 Public Access Scanner
Description: Scans S3 buckets for public read/write permissions.

Key Features: Inspects Bucket Policies and Access Control Lists (ACLs) for exposure.

Impact: Prevents data breaches caused by misconfigured cloud storage.


/Cloud-Security-Automation-Suite
├── 01_CIS_Compliance_Checker/       # Global Standard Hardening (v1.4.0)
├── 02_Attack_Surface_Mapper/        # External Exposure & Port Analysis
├── 03_Backup_DR_Validator/          # Recovery Readiness & KMS Audit
├── 04_Backup_Recency_Monitor/       # RPO (Recovery Point Objective) Tracking
├── 05_Resource_Inventory_Scanner/   # Asset Visibility & Shadow IT Discovery
├── 06_CloudTrail_Visibility_Audit/  # Management Event & Audit Trail Verification
├── 07_EC2_Security_Group_Auditor/   # Network Firewall & Ingress Risk Analysis
├── 08_Forensic_Logging_Checker/     # VPC Flow Logs & Network Traceability
├── 09_IAM_Identity_Auditor/         # MFA, Key Age & Credential Hygiene
├── 10_IAM_Privilege_Detector/       # Overly Permissive & Wildcard (*) Policy Audit
├── 11_MITRE_ATT&CK_Mapper/          # Threat Context & Tactic Correlation
└── 12_S3_Public_Access_Scanner/     # Data Leakage & Bucket Policy Auditor
🛠️ Tech Stack
Language: Python 3.10+

SDK: boto3 (AWS SDK for Python)

Core Libraries: json, logging, datetime, botocore

Standards: MITRE ATT&CK for Cloud, CIS AWS Foundations Benchmark

Compliance: HIPAA, SOC2, and PCI-DSS Readiness

Environment: AWS Cloud (IAM, S3, EC2, CloudTrail, AWS Backup)

👨‍💻 Author
Anuj Sharma Cloud Security Automation Enthusiast | DevSecOps Specialist | Python & Boto3 Expert
