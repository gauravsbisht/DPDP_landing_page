# ConsentAxis — Product Demo Video Script
## For AI Video Generation (Napkin / Synthesia / HeyGen)

---

## SLIDE 1 — THE PROBLEM

### India's Data Privacy Law Is Here. Are You Ready?

**The DPDP Act 2023** is India's first comprehensive data privacy law.

Every company that processes personal data of Indian citizens must:
- ✅ Obtain **explicit consent** before collecting data
- ✅ Allow users to **withdraw consent** at any time
- ✅ Respond to **Data Subject Access Requests** (DSAR) within 72 hours
- ✅ Maintain a **tamper-proof audit trail** of every consent transaction
- ✅ Issue **privacy notices** before data collection

**Penalty for non-compliance: ₹250 Crore (≈ $30 Million)**

> 🔴 Most companies today manage consent through scattered boolean columns, emails, and spreadsheets. That won't survive an audit.

---

## SLIDE 2 — INTRODUCING CONSENTAXIS

### One Platform. Complete Consent Lifecycle.

**ConsentAxis** is a purpose-built DPDP compliance platform that manages the entire consent lifecycle — from notice to withdrawal to audit.

**Core Modules:**

| Module | What It Does |
|--------|-------------|
| 🔔 **Notice Engine** | Create, version, and deliver privacy notices with legally compliant templates |
| ✅ **Consent Ledger** | Immutable, chain-hashed record of every consent grant/withdrawal |
| 📋 **DSAR Portal** | Self-service portal for data subjects — access, correct, erase, port |
| 🔍 **Audit Trail** | Every action logged, timestamped, tamper-evident — regulator-ready |
| 👤 **Multi-Tenant** | One deployment serves multiple organizations with full data isolation |

---

## SLIDE 3 — HOW IT WORKS

### The Consent Lifecycle in ConsentAxis

```
Step 1: NOTICE
Organization creates a privacy notice
→ Specifies purposes (marketing, analytics, KYC)
→ Notice versioned and stored immutably

Step 2: CONSENT CAPTURE
Data subject receives notice
→ Grants or denies consent per purpose
→ Consent recorded in the ledger with chain hash

Step 3: ONGOING MANAGEMENT
Subject can withdraw consent anytime
→ Status updates propagated
→ Full history preserved

Step 4: DSAR PROCESSING
Subject requests access/erasure
→ System locates all PII across tables
→ Action executed + audit logged

Step 5: AUDIT
Regulator requests proof
→ Export complete consent trail
→ Chain hashes verify integrity
```

---

## SLIDE 4 — THE CONSENT LEDGER

### Immutable. Chain-Hashed. Regulator-Ready.

Every consent transaction is stored as a record with:

| Field | Purpose |
|-------|---------|
| `tenant_id` | Multi-org isolation |
| `subject_id` | Who gave consent |
| `purpose` | What they consented to |
| `status` | granted / withdrawn / expired |
| `notice_id` + `notice_version` | Which notice was shown |
| `notice_snapshot` | Frozen copy of the notice text |
| `chain_hash` | SHA-256 linking to previous record |
| `ip_address` | Where consent was given |
| `granted_at` / `withdrawn_at` | When |

> 🔐 The chain hash creates a blockchain-like audit trail. Any tampering breaks the chain and is immediately detectable.

---

## SLIDE 5 — DSAR PROCESSING

### Respond to Data Subject Requests in Minutes, Not Weeks

**Supported request types:**
- 📥 **Access** — "Show me all my data"
- ✏️ **Correction** — "Fix my address"
- 🗑️ **Erasure** — "Delete my data" (Right to be Forgotten)
- 📦 **Portability** — "Give me my data in machine-readable format"
- ❌ **Objection** — "Stop processing my data for marketing"

**Workflow:**
1. Subject submits request via self-service portal
2. Request logged with unique tracking ID
3. System identifies all PII locations
4. Action executed (access / anonymize / delete)
5. Confirmation sent to subject
6. Full audit trail preserved

---

## SLIDE 6 — NOTICE ENGINE

### Create Legally Compliant Privacy Notices in Minutes

- 📝 **Template Library** — Pre-built templates for common purposes
- 🔄 **Version Control** — Every edit creates a new version
- 📸 **Snapshot Freeze** — Notice text frozen at time of consent
- 🌐 **Multi-language** — Support for Indian languages
- ⚖️ **Legal Review Workflow** — Approve before publishing

---

## SLIDE 7 — ARCHITECTURE

### Built for Scale. Built for Security.

```
┌─────────────────────────────────────┐
│         ConsentAxis Platform        │
├─────────┬──────────┬────────────────┤
│ Notice  │ Consent  │    DSAR        │
│ Engine  │ Ledger   │    Portal      │
├─────────┴──────────┴────────────────┤
│         FastAPI Backend             │
│         PostgreSQL + Supabase       │
│         Row-Level Security          │
├─────────────────────────────────────┤
│      React Frontend (Privacy Portal)│
│      Multi-tenant Dashboard         │
└─────────────────────────────────────┘
```

**Tech Stack:** Python · FastAPI · PostgreSQL · React · Supabase · Azure

---

## SLIDE 8 — WHY CONSENTAXIS

### Vs. Building In-House

| Aspect | DIY | ConsentAxis |
|--------|-----|-------------|
| Time to compliance | 6-12 months | Days |
| Consent audit trail | Manual logging | Automatic + chain-hashed |
| DSAR response time | Weeks | Minutes |
| Notice versioning | None | Built-in |
| Multi-regulation | Custom per law | DPDP + GDPR ready |
| Cost | 3-5 engineers full-time | SaaS subscription |

---

## SLIDE 9 — INTEGRATION WITH DATACEREBRIUM

### Discover → Fix → Comply

ConsentAxis pairs with **DataCerebrium** (our data discovery engine):

1. **DataCerebrium scans** your existing database
2. **Finds PII** columns and consent fields automatically
3. **Generates a migration script** to move legacy consent into ConsentAxis
4. **ConsentAxis manages** the consent lifecycle going forward

> 🎯 From "we don't know what PII we have" to "fully compliant" in one workflow.

---

## SLIDE 10 — CALL TO ACTION

### Start Your DPDP Compliance Journey Today

- 🌐 **Website:** consentaxis.com
- 🚀 **Free assessment** of your current compliance posture
- 📞 **Book a demo** — see ConsentAxis in action on your own database

**ConsentAxis** — Consent Management. Simplified. Compliant.

---
