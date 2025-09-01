# AWS Certified Security – Specialty (SCS-C02) Exam Services

This repository documents the **in-scope AWS services and features** relevant to the AWS Certified Security – Specialty exam (SCS-C02). Each section includes:
- A brief description of the service
- An official documentation link
- Example use cases
- Key points to remember for the exam
- Quick summary

---

## Identity and Access Management

### AWS Identity and Access Management (IAM)
- **Docs:** [IAM Documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)
- **Example:** Create IAM policies to enforce least privilege across accounts.
- **Exam Tips:**
  - Understand policy types (managed, inline, resource-based).
  - Use IAM Access Analyzer and IAM Policy Simulator for troubleshooting.
  - Enforce MFA and credential rotation.
- **Summary:** IAM is the foundation of all AWS security.

### AWS IAM Identity Center (AWS SSO)
- **Docs:** [IAM Identity Center](https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html)
- **Example:** Configure centralized SSO for AWS accounts with MFA.
- **Exam Tips:**
  - Supports SAML and federation with identity providers.
  - Key for multi-account access control.
- **Summary:** Simplifies identity management across accounts.

### Amazon Cognito
- **Docs:** [Amazon Cognito](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html)
- **Example:** Manage app authentication with user pools.
- **Exam Tips:**
  - MFA support.
  - Social identity provider integration.
- **Summary:** Used for application-level authentication.

### AWS Security Token Service (STS)
- **Docs:** [STS Documentation](https://docs.aws.amazon.com/STS/latest/APIReference/Welcome.html)
- **Example:** Issue temporary credentials for cross-account access.
- **Exam Tips:**
  - STS tokens are temporary and reduce risk.
- **Summary:** Enables secure short-term access.

---

## Threat Detection & Monitoring

### Amazon GuardDuty
- **Docs:** [GuardDuty](https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html)
- **Example:** Detect compromised IAM keys or EC2 instances.
- **Exam Tips:**
  - Ingests CloudTrail, VPC Flow Logs, DNS logs.
  - Integrates with Security Hub & EventBridge.
- **Summary:** Core threat detection service.

### Amazon Inspector
- **Docs:** [Inspector](https://docs.aws.amazon.com/inspector/latest/user/what-is-inspector.html)
- **Example:** Scan EC2 and ECR for vulnerabilities.
- **Exam Tips:**
  - Supports agentless scans.
  - Findings can trigger SSM automation.
- **Summary:** AWS-native vulnerability management.

### Amazon Macie
- **Docs:** [Macie](https://docs.aws.amazon.com/macie/latest/user/what-is-macie.html)
- **Example:** Discover PII in S3 buckets.
- **Exam Tips:**
  - Automates sensitive data classification.
- **Summary:** Focuses on data discovery and protection.

### Amazon Detective
- **Docs:** [Detective](https://docs.aws.amazon.com/detective/latest/adminguide/what-is-detective.html)
- **Example:** Investigate GuardDuty findings.
- **Exam Tips:**
  - Visualizes relationships between resources and events.
- **Summary:** Incident investigation tool.

### AWS Security Hub
- **Docs:** [Security Hub](https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html)
- **Example:** Centralize GuardDuty, Inspector, and Macie findings.
- **Exam Tips:**
  - Supports automated remediation via EventBridge.
- **Summary:** Central dashboard for security findings.

### Amazon CloudWatch
- **Docs:** [CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html)
- **Example:** Create metric filters for IAM policy changes.
- **Exam Tips:**
  - Logs, metrics, alarms.
  - CloudWatch Logs Insights for querying.
- **Summary:** Monitoring and alerting backbone.

### AWS CloudTrail
- **Docs:** [CloudTrail](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html)
- **Example:** Track IAM API activity.
- **Exam Tips:**
  - Multi-account logging.
  - CloudTrail Insights detect anomalies.
- **Summary:** Logging of all AWS API calls.

### AWS Config
- **Docs:** [AWS Config](https://docs.aws.amazon.com/config/latest/developerguide/WhatIsConfig.html)
- **Example:** Detect unencrypted S3 buckets.
- **Exam Tips:**
  - Config rules + Conformance Packs.
- **Summary:** Compliance and drift detection.

---

## Infrastructure Security

### Amazon VPC (and features)
- **Docs:** [Amazon VPC](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)
- **Example:** Secure workloads with Security Groups and NACLs.
- **Exam Tips:**
  - VPC Flow Logs, Reachability Analyzer.
  - PrivateLink and VPC Endpoints.
- **Summary:** Core network isolation and controls.

### AWS Network Firewall
- **Docs:** [Network Firewall](https://docs.aws.amazon.com/network-firewall/latest/developerguide/what-is-aws-network-firewall.html)
- **Example:** Block traffic with stateful inspection.
- **Exam Tips:**
  - Integrates with VPCs for network segmentation.
- **Summary:** Managed firewall service.

### AWS WAF
- **Docs:** [AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html)
- **Example:** Protect web apps from SQL injection.
- **Exam Tips:**
  - Combine with CloudFront for layered defense.
- **Summary:** Web Application Firewall.

### AWS Shield
- **Docs:** [AWS Shield](https://docs.aws.amazon.com/waf/latest/developerguide/ddos-overview.html)
- **Example:** Protect apps against DDoS.
- **Exam Tips:**
  - Shield Advanced = enterprise DDoS protection.
- **Summary:** DDoS protection at the edge.

### AWS Firewall Manager
- **Docs:** [Firewall Manager](https://docs.aws.amazon.com/waf/latest/developerguide/fms-chapter.html)
- **Example:** Enforce WAF rules org-wide.
- **Exam Tips:**
  - Delegated admin model.
- **Summary:** Central policy enforcement for WAF, SGs, and more.

---

## Data Protection & Cryptography

### AWS Key Management Service (KMS)
- **Docs:** [KMS](https://docs.aws.amazon.com/kms/latest/developerguide/overview.html)
- **Example:** Encrypt S3 objects with CMKs.
- **Exam Tips:**
  - Understand key policies vs IAM policies.
  - Supports symmetric and asymmetric keys.
- **Summary:** Central encryption key management.

### AWS CloudHSM
- **Docs:** [CloudHSM](https://docs.aws.amazon.com/cloudhsm/latest/userguide/introduction.html)
- **Example:** Use HSM cluster for RDS encryption.
- **Exam Tips:**
  - Dedicated hardware appliance.
- **Summary:** Hardware-based key management.

### AWS Certificate Manager (ACM)
- **Docs:** [ACM](https://docs.aws.amazon.com/acm/latest/userguide/acm-overview.html)
- **Example:** Deploy TLS certs to CloudFront and ALB.
- **Exam Tips:**
  - Automates cert renewals.
- **Summary:** Simplified certificate provisioning.

### AWS Secrets Manager
- **Docs:** [Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html)
- **Example:** Rotate DB credentials automatically.
- **Exam Tips:**
  - Integrates with RDS.
- **Summary:** Secure secret storage and rotation.

### AWS Systems Manager Parameter Store
- **Docs:** [Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html)
- **Example:** Store encrypted app config values.
- **Exam Tips:**
  - Can use KMS for encryption.
- **Summary:** Lightweight secrets/config management.

### Amazon S3 (Security Aspects)
- **Docs:** [S3 Security](https://docs.aws.amazon.com/AmazonS3/latest/userguide/security.html)
- **Example:** Block public access, enable Object Lock.
- **Exam Tips:**
  - TLS for API calls.
  - S3 Block Public Access.
- **Summary:** Core secure storage with encryption and access controls.

---

## Management & Governance

### AWS Organizations
- **Docs:** [Organizations](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_introduction.html)
- **Example:** Use SCPs to restrict root usage.
- **Exam Tips:**
  - Delegated admin.
  - Multi-account governance.
- **Summary:** Central multi-account management.

### AWS Control Tower
- **Docs:** [Control Tower](https://docs.aws.amazon.com/controltower/latest/userguide/what-is-control-tower.html)
- **Example:** Deploy secure landing zone with guardrails.
- **Exam Tips:**
  - Automates account provisioning.
- **Summary:** Simplified multi-account governance.

### AWS Audit Manager
- **Docs:** [Audit Manager](https://docs.aws.amazon.com/audit-manager/latest/userguide/what-is.html)
- **Example:** Collect evidence for PCI compliance.
- **Exam Tips:**
  - Evidence automation.
- **Summary:** Simplifies compliance audits.

### AWS Well-Architected Tool
- **Docs:** [Well-Architected Tool](https://docs.aws.amazon.com/wellarchitected/latest/userguide/intro.html)
- **Example:** Run security pillar checks on workloads.
- **Exam Tips:**
  - Use Security Pillar questions.
- **Summary:** Evaluate architecture against best practices.

### AWS Trusted Advisor
- **Docs:** [Trusted Advisor](https://docs.aws.amazon.com/awssupport/latest/user/TrustedAdvisor.html)
- **Example:** Identify unused resources or overly permissive IAM policies.
- **Exam Tips:**
  - Security checks available even in basic support tier.
- **Summary:** Cost optimization + security findings.

---

## Summary Table

| Service              | Primary Exam Domain                          |
|----------------------|-----------------------------------------------|
| IAM, IAM Identity Center, Cognito | Identity & Access Management          |
| GuardDuty, Inspector, Macie, Detective | Threat Detection & Monitoring    |
| CloudTrail, CloudWatch, Config    | Logging & Monitoring                  |
| VPC, Network Firewall, WAF, Shield | Infrastructure Security              |
| KMS, CloudHSM, ACM, Secrets Manager | Data Protection & Cryptography     |
| Organizations, Control Tower, Audit Manager | Governance & Compliance    |

---

## How to Use This Repo
- Clone and explore each service folder (future labs can be added under `/labs`).
- Review exam-focused notes before practicing labs.
- Record demos or write-ups as portfolio evidence.

---
*This repo is an unofficial study and portfolio resource for AWS Security Specialty exam prep.*
