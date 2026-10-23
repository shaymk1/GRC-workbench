
# Ubuntu Mining (Pty) Ltd

## GRC Portfolio Project

**Prepared by:** Mamosebetsi Kekae, Junior GRC Analyst
**Date:** October 2026
**Status:** Draft for Management Review

> **Note from the author:** This is my first major GRC project. I've built this portfolio to show how a mid-sized mining company can pull its risks, compliance obligations, and cybersecurity into one structured system. I used ISO 31000 for risk, ISO 27001 for security, and the NIST CSF for cybersecurity. Because Ubuntu Mining is a fictional company (a 500-person coal and processing operation), all the risks and gaps below are scenarios I created to practice the methodology. I've flagged areas where I made assumptions or where a senior reviewer needs to step in.

---

## Part 1: Company Profile & Governance Structure

### 1.1 The Business Context

Ubuntu Mining operates an open-pit mine, processing plant, and maintenance facilities. They rely heavily on heavy machinery, Operational Technology (OT/ICS) for physical processing, and standard Corporate IT. They also use a lot of contractors.

Because of this, the biggest risks aren't just financial; they are safety, environmental, and operational. A cyberattack on a corporate laptop is bad, but a cyberattack on a blast furnace control system is a safety hazard.

### 1.2 Business Objectives (What we are trying to protect)

- **OBJ-01:** Keep employees and contractors safe (Zero harm).
- **OBJ-02:** Keep the plant running efficiently (no unplanned downtime).
- **OBJ-03:** Stay compliant with mining and environmental laws.
- **OBJ-04:** Protect sensitive data (employee records, production secrets).
- **OBJ-05:** Secure our IT and OT systems.

### 1.3 Proposed Governance (Who does what)

> **Junior Note:** In a real company, you can't just assign titles. But for this project, I've mapped out a logical structure. The Board sets the risk appetite, Executive Management (ExCo) allocates resources, and specific Managers own the risks.

- **Board of Directors:** Approves the risk strategy.
- **Executive Management (ExCo):** Approves risk treatment plans and budgets.
- **GRC Function (Me, in this scenario):** Coordinates the registers, tracks actions, and challenges the business on their evidence.
- **Risk Owners:** The actual managers (e.g., Mine Manager, IT Manager). They are accountable for the risk.
- **Control Owners:** The people operating the controls (e.g., the IT Admin doing access reviews).

---

## Part 2: Risk Assessment Methodology (The Rules)

> **Junior Note:** You can't just guess if a risk is "high" or "low." I set up a standard 5x5 matrix.

**Formula:** Risk Score = Likelihood (1-5) × Impact (1-5)

- **1–4:** Low (Monitor)
- **5–9:** Moderate (Assign an owner)
- **10–16:** High (Needs a treatment plan)
- **17–25:** Critical (Escalate to ExCo immediately)

**Important Rule I learned:** A risk score should never override common sense. If there is a credible threat to life, it gets escalated *immediately*, even if the math says it's a "Medium" risk.

**Inherent vs. Residual Risk:**

- *Inherent* is the risk before we do anything.
  
- *Residual* is the risk *after* our controls.
  
> **Junior Note:** I struggled with this. Just because a policy exists doesn't mean the risk is lower. I've made a rule for myself: I won't lower a risk score until I've actually seen the evidence that the control is working (e.g., I saw the access review logs, not just the policy).

---

## Part 3: Enterprise Risk Register

Here are the top 12 risks I identified for Ubuntu Mining.

| Risk ID | Risk Scenario | Category | Inherent Score | Proposed Risk Owner | Main Existing Controls | Evidence Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **R01** | **OT Cyber Compromise:** Unauthorized access to ICS/SCADA causing production halt or unsafe conditions. | OT Security | 20 (Critical) | OT Manager | Network segmentation, firewalls, remote access controls. | *Not assessed yet* |
| **R02** | **Contractor Safety Failure:** Inadequate induction leads to a serious injury or fatality. | Safety | 20 (Critical) | HSE Manager | Contractor onboarding, permit-to-work systems. | *Not assessed yet* |
| **R03** | **Critical Equipment Failure:** Mill or haul truck breaks down, halting production. | Operational | 16 (High) | Maintenance Manager | Preventive maintenance schedule, critical spares inventory. | *Not assessed yet* |
| **R04** | **Backup & Recovery Failure:** Ransomware hits corporate IT and backups are corrupted, stopping finance and payroll. | IT Security | 15 (High) | IT Manager | Daily backups, offsite storage, endpoint protection. | *Not assessed yet* |
| **R05** | **Environmental Incident:** Tailings dam leak or chemical spill. | Environmental | 15 (High) | Environmental Manager | Dam monitoring, spill kits, environmental inspections. | *Not assessed yet* |
| **R06** | **Compliance Gap:** Missed permit renewals or failure to report an incident in time. | Compliance | 12 (High) | Compliance Lead | Compliance calendar, legal register. | *Not assessed yet* |
| **R07** | **Supplier Disruption:** Key contractor or reagent supplier goes bankrupt or delays delivery. | Third-Party | 12 (High) | Procurement Mgr | Dual sourcing, SLAs. | *Not assessed yet* |
| **R08** | **Weak Access Control:** Old user accounts not deleted, leading to unauthorized access. | IT Security | 16 (High) | IT Manager | AD groups, password policies. | *Not assessed yet* |

> **Junior Note:** I purposefully rated the OT Cyber Risk and Contractor Safety as "Critical." In mining, these are the two areas that can literally kill someone or shut the mine down for months. The other risks are high, but more manageable.

---

## Part 4: Compliance Register (The Legal Stuff)

> **Junior Note:** I don't have a law degree, so I listed the obligations as *"Potentially Applicable - Verification Required"* until Legal confirms them.

| ID | Obligation Area | Applicability | What we need to do | Owner | Evidence Needed |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **C01** | Mining Safety Laws (e.g., MHSA) | Verify | Maintain safe working environments, report incidents. | HSE Manager | Risk assessments, incident logs |
| **C02** | Environmental Permits | Verify | Monitor water/air quality, prevent spills. | Env. Manager | Monitoring reports, permits |
| **C03** | Data Privacy (POPIA/GDPR) | Verify | Protect employee and contractor personal data. | HR / Legal | Privacy policy, access logs |
| **C04** | ISO 27001 (Internal Goal) | Internal | Align our security program to an international standard. | ISMS Lead | SoA (See Part 6) |

---

## Part 5: ISO 27001:2022 Gap Assessment & Statement of Applicability (SoA)

> **Junior Note:** This was the hardest part. ISO 27001 has a lot of clauses. I did a gap assessment to see where we are falling short. Because this is a fictional company, I marked almost everything as "Not Assessed" or "Evidence Not Provided" because I can't invent fake documents.

**The 4 Big Clauses:**

- **Clause 4-6 (Planning):** We have a methodology, but we haven't formally approved an ISMS Scope yet. (Gap).
- **Clause 7 (Support):** We don't have a formal training/competence matrix for security. (Gap).
- **Clause 8-10 (Operation & Improvement):** We don't have internal audits or management reviews happening yet. (Gap).

### Statement of Applicability (SoA) Summary

ISO 27001 Annex A has 93 controls. I reviewed all of them.

- **Proposed Applicable:** 82 controls. (e.g., Access Control, Asset Management, Incident Response).
- **Conditional:** 11 controls. (e.g., Source Code security—we don't know if we have developers yet).
- **Not Applicable:** 0 controls. (I couldn't justify excluding any yet).
- **Implementation Status:** 93 "Not Assessed."

> **Junior Note:** A senior auditor would say this SoA is "empty." But I think the important thing is that I built the framework. I linked all 93 controls to my enterprise risks (like R01, R08) so we know exactly *why* we need them.

---

## Part 6: Risk Treatment Plan & Remediation Tracker

We can't fix everything at once. Here is my proposed action plan for the next 90 days, focusing on the highest risks first.

| Action ID | What we need to do | Related Risk / Control | Owner | Priority | Target Date | How we prove it's done (Evidence) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **A01** | Define and approve the ISMS Scope (what systems are in, what are out). | ISO 27001 Cl. 4 | ISMS Lead | High | Day 30 | Approved Scope document |
| **A02** | Create a complete inventory of all OT/ICS assets. | Risk R01 / Control A.5.9 | OT Manager | Critical | Day 45 | Excel/System inventory report |
| **A03** | Review privileged user accounts and remove old/inactive users. | Risk R08 / Control A.8.2 | IT Manager | High | Day 60 | Before/After access review logs |
| **A04** | Perform a real backup restoration test for critical systems. | Risk R04 / Control A.8.13 | IT Ops | Critical | Day 30 | Test report showing successful restore |
| **A05** | Build a Compliance Register and confirm legal applicability with Legal. | Risk R06 / Compliance | Compliance | High | Day 60 | Signed-off legal register |
| **A06** | Test the Incident Response Plan with a tabletop exercise. | Risk R01, R04 | Security Lead | Moderate | Day 90 | Exercise report / Lessons Learned |

> **Junior Note on Closure:** I added a rule to the tracker. An action cannot be closed just because the owner says "it's done." I have to see the evidence (e.g., a screenshot of the access list, or a successful backup test log). If they don't give me evidence, it stays "Open."

---

## Part 7: Management Reporting (The Dashboard)

If I were presenting this to the CEO or Board, I wouldn't give them this whole document. I'd give them a one-page dashboard.

**Proposed Monthly Dashboard Metrics:**

- **Critical Risks Open:** 2 (OT Cyber, Contractor Safety).
- **Overdue Actions:** [Number]
- **Actions Awaiting My Review (Evidence needed):** [Number]
- **Upcoming Compliance Deadlines:** [Number]
- **Backup Recovery Test Status:** [Pass / Fail]

---

## Part 8: Conclusion & Limitations

> **Junior Note:** I want to be totally honest about this project.

1. **It's a simulation:** Ubuntu Mining is fake. The risks are realistic based on my research into the mining sector, but they are not real incidents.
2. **Evidence is missing:** I didn't lower any risk scores (residual risk) because I haven't actually seen the control evidence yet. I left them as "Not Assessed."
3. **Next steps:** If I were hired to do this for a real mining company, the next step would be to sit down with the OT Manager and the Maintenance Manager, interview them, look at their systems, and turn this framework into a living, breathing register.