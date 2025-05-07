# 🔐 ACE – Security & Data Retention

## Overview

At Digital Expression, security, privacy, and responsible data handling are foundational principles behind ACE. This document outlines how ACE manages data, ensures compliance, and protects sensitive information in enterprise environments.

---

## 🔒 Security Principles

* **Privacy by Design**: ACE is built to minimize exposure of source code and sensitive data.
* **Least Privilege Access**: All services and data flows operate under minimal permissions.
* **Zero Trust Model**: Every interaction and component is validated and scoped.
* **No Self-Hosting**: Ensures continuous updates, vulnerability patches, and LLM improvements by maintaining a single, secured cloud infrastructure.
* **System Sandboxing**: ACE runs commands within secure OS-level sandboxes:
  * 🖥️ On macOS: using App Sandbox
  * 🐧 On Linux: using Landlock LSM
  * 🔐 File system access is restricted to the current working directory only
---

## 🧾 Data Handling

### Source Code

* Code analysis is performed **locally** by default.
* Only metadata, context embeddings, or summaries may be sent remotely.
* No raw source code is uploaded without explicit developer consent.

### Embeddings

* Embeddings are generated from local context to enable Retrieval-Augmented Generation (RAG).
* Stored in an **encrypted database** with industry-standard encryption (AES-256).
* Data is segmented by project and client to prevent cross-access.

### Database Architecture

* **Document DB**: For structured project and metadata
* **Vector DB**: For fast, semantic retrieval and similarity search
* **Graph DB**: For mapping relationships across modules and knowledge entries

### Retention Policy

* Embeddings and context are retained only as long as needed to support developer workflows.
* Data can be automatically expired or purged upon request.
* Temporary memory-based caching can be disabled for strict runtime-only usage.

---

## 🛡 Compliance & Certifications

### Company Certifications

* ✅ **ISO 9001:2015** – Quality Management
* ✅ **ISO 20000-1:2018** – IT Service Management
* ✅ **ISO/IEC 27001:2022** – Information Security

### Vendor Certifications

* ✅ All vendors used are **ISO/IEC 27001** or **SOC 2 Type 2** certified
* ✅ Fully **GDPR compliant** infrastructure and processes

---

## 🕵️‍♂️ Audit & Monitoring

* **Audit Logs**: Optionally record access, queries, and code context usage
* **Integration**: Logs can be sent to your internal monitoring or SIEM platform
* **Audit Availability**: Full audit trail can be made available on request

---

## ⚠️ Data Sharing Controls

* Developers and teams control what data is included in context and embedding generation
* Filters and exclusion rules can be set in `.aceconfig` or CLI
* No external transmission happens without developer or admin-level opt-in

---

## 📞 Questions or Concerns?

For detailed security review, audits, or custom data retention policies, please contact:

📧 **[info@digitalexpression.ro](mailto:info@digitalexpression.ro)**
🌐 **[https://digitalexpression.ro](https://digitalexpression.ro)**
