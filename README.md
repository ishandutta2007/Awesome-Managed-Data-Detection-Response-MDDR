# Awesome-Managed-Data-Detection-Response-MDDR

# Awesome Managed Data Detection & Response (MDDR)

> A curated list of top Managed Data Detection and Response (MDDR) and Managed Detection and Response (MDR) platforms — both SaaS/Hosted commercial solutions and open-source alternatives for 24/7 threat monitoring, investigation, and response.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Druva Managed Data Detection and Response](#druva-managed-data-detection-and-response)
  - [CrowdStrike Falcon Complete](#crowdstrike-falcon-complete)
  - [SentinelOne Vigilance Respond](#sentinelone-vigilance-respond)
  - [Arctic Wolf Aurora MDR](#arctic-wolf-aurora-mdr)
  - [Rapid7 Managed Threat Complete](#rapid7-managed-threat-complete)
  - [Expel MDR](#expel-mdr)
  - [ReliaQuest GreyMatter](#reliaquest-greymatter)
- [Open-Source Software](#-open-source-software)
  - [Wazuh](#wazuh)
  - [TheHive & Cortex](#thehive--cortex)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted MDDR and MDR platforms. These are not open-source but are included as reference points for feature comparison.

### Druva Managed Data Detection and Response
**Type:** 24/7 backup data monitoring with managed incident response
Druva's MDDR is a managed service built directly into the Druva Cloud Platform, providing round-the-clock monitoring, detection, and response specifically for **backup environments** [citation:1]. It monitors key threat indicators including snapshot deletion, backup set deletion, admin deletion of devices or users, and suspicious activity across workloads like Microsoft 365, Google Workspace, Azure, AWS, and NAS [citation:1]. When an alert fires, Druva's Incident Response team triages and validates it, contacts administrators to verify whether the event was planned, and executes predefined playbooks for response [citation:1]. **Important:** MDDR is available only to Druva customers at no additional charge, and it is not available for GovCloud and SFDC customers [citation:1][citation:14].  
**Best for:** Druva customers wanting an expert extension to their IR team focused specifically on backup integrity and data protection threats.

### CrowdStrike Falcon Complete
**Type:** Agentic MDR with human oversight and 1-minute containment
Falcon Complete is an agentic MDR service that combines deterministic automation, adaptive AI agents, and 24/7 human expert oversight [citation:2]. It correlates telemetry across endpoint, identity, cloud, SaaS, and third-party data to expose full attack campaigns rather than isolated alerts, and it can contain threats at machine speed [citation:2]. Reported metrics include a **median time to containment (MTTC) of 1 minute**, a **75% reduction in mean time to response (MTTR)**, and **2.7 million remediated detections per month** [citation:2]. It includes Falcon Shield for 24/7 SaaS application protection and Falcon Guardian runtime telemetry for AI agent behavior visibility [citation:2].  
**Best for:** Organizations wanting the fastest containment times and deep correlation across a broad telemetry estate with strong AI governance.

### SentinelOne Vigilance Respond
**Type:** Tiered MDR with forensic reporting and IR retainer
SentinelOne's Vigilance Respond and Respond Pro are MDR services layered on top of its Singularity platform [citation:3]. Respond provides 24/7 monitoring, investigation, and documentation of every console threat, forwarding only urgent issues to the customer [citation:3]. **Respond Pro** adds digital forensic reporting, malware reverse engineering, memory analysis, direct access to forensic experts, and an **IR retainer** with prepaid hours for active containment and eradication [citation:3]. Standard SLA offers investigation within 2-4 hours, while Pro offers 1-2 hours [citation:3].  
**Best for:** Organizations wanting tiered MDR options with the option to add forensic depth and an IR retainer as needs escalate.

### Arctic Wolf Aurora MDR
**Type:** Concierge-led proactive MDR with agentic SOC
Arctic Wolf's Aurora MDR emphasizes a **Concierge Experience** where security experts learn the organization's specific environment, priorities, and risks to reduce attack frequency and severity, not just respond to alerts [citation:4]. The Aurora Agentic SOC uses AI for speed and scale while human experts guide decisions, with **200+ integrations** across attack surfaces [citation:4]. Reported outcomes include reducing the frequency of a successful attack by up to **90%** and decreasing impact by up to **90%** (Forrester TEI) [citation:4]. It also provides proactive Security Posture Reviews (SPiDRs) to harden environments [citation:4].  
**Best for:** Organizations wanting a hands-on, proactive partner that focuses on risk reduction and posture improvement alongside detection and response.

### Rapid7 Managed Threat Complete
**Type:** MXDR with unlimited vulnerability management and IR
Managed Threat Complete bundles always-on MXDR with **unlimited vulnerability risk management** in a single subscription [citation:5]. A key differentiator is that it includes **unlimited incident response** at the same level as an IR retainer, with DFIR professionals embedded on the team—rather than handing off to a third-party IR firm after a breach [citation:5]. Forrester TEI found **5.5x ROI over 3 years**, **<3 month payback**, and a **90% reduction in breach likelihood** [citation:5]. Customers also get full access to the underlying cloud-native XDR technology and detections library for their own investigations [citation:5].  
**Best for:** Teams wanting to consolidate MDR and vulnerability management while retaining full visibility and control over the underlying detection technology.

### Expel MDR
**Type:** Transparent, AI-accelerated MDR with 14-minute MTTR
Expel MDR connects to the customer's existing security stack (160+ integrations including CrowdStrike, Elastic, Azure, Google Workspace, and Okta) with no agents to deploy or rip-and-replace [citation:6]. Its AI engine **Ruxie** triages millions of events, gathers evidence, enriches alerts, and matches patterns in seconds, while human analysts make the critical calls [citation:6]. Reported **MTTR is 14 minutes**, with automated remediation executing targeted containment actions and generating plain-language audit trails [citation:6]. The platform emphasizes **no black boxes**—customers see exactly what Expel sees in the Workbench, and every investigation and response is visible in real time [citation:6].  
**Best for:** Organizations wanting a transparent MDR partner that works with their existing tools and provides full visibility into investigations and response actions.

### ReliaQuest GreyMatter
**Type:** Agentic AI SecOps platform with 4.48-minute containment
ReliaQuest GreyMatter is an agentic AI security operations platform with six "Teammate" personas (IR Analyst, Detection Engineer, Threat Hunter, Threat Intel Analyst, IT Engineer, OT Engineer) that use 200+ agent skills and 400+ AI tools to work toward objectives rather than just executing tasks [citation:11]. Reported metrics include **mean time to detect <5 seconds**, **investigate 22 minutes**, **contain 4.48 minutes**, and **resolve 48 minutes** [citation:11]. The IR Analyst autonomously investigates and responds to **100% of alerts across 300+ technologies with 99.4% accuracy**, handling **78M alerts per year** [citation:11].  
**Best for:** Organizations wanting an agentic AI platform that automates the full investigation and response lifecycle across a broad technology estate.

---

## 🟩 Open-Source Software

Self-hosted, community-driven tools for building MDDR/MDR capabilities. The open-source ecosystem provides the **detection, investigation, and response foundation** rather than a fully managed 24/7 human service.

### Wazuh
**Stack:** C++ / OpenSearch | **License:** GPL-2.0 (open source) 
Wazuh is a unified open-source XDR and SIEM platform that provides the technical foundation for managed detection and response [citation:12]. Key capabilities relevant to MDDR include:
- **File Integrity Monitoring (FIM)** tracking file additions, modifications, and deletions with real-time alerts, helping detect ransomware or tampering with critical data [citation:12]
- **Malware detection** monitoring files, system logs, Windows Registry, and system calls, with threat intelligence integration and anomaly detection [citation:12]
- **Vulnerability Detection** correlating software inventory against CVE data from the Wazuh CTI platform [citation:12]
- **Threat hunting** with rules, decoders, and MITRE ATT&CK mapping [citation:12]
- **Active response** for automated actions like removing malicious files or isolating endpoints [citation:12]

While Wazuh does not provide the 24/7 human analyst service of commercial MDDR, it delivers the detection and response automation that a SOC or MSP can build a managed offering around.  
**Best for:** Organizations and MSPs wanting to build their own detection and response capability with full control over data and no per-agent licensing.

### TheHive & Cortex
**Stack:** Scala / Elasticsearch / Python | **License:** AGPL-3.0
TheHive is an open-source Security Incident Response Platform for case management and collaboration, while Cortex provides automated enrichment and analysis of observables (IOCs) through analyzers like VirusTotal, AbuseIPDB, and MISP [from previous context]. Together they operationalize the **response and investigation** side of MDDR: alerts can be converted into cases, observables automatically enriched, and response actions tracked. They integrate with MISP for threat intelligence sharing and with SIEMs for alert ingestion.  
**Best for:** SOC and CSIRT teams building an open-source investigation and case management layer to complement detection tools like Wazuh.

---

## 📊 Comparison at a Glance

| Software | License | Type | MTTC / Response | IR Retainer | Self-Hosted | Best For |
|----------|---------|------|-----------------|-------------|-------------|----------|
| **Druva MDDR** | Proprietary | Backup data MDDR | (Playbook-based) | (Included for Druva) | ❌ | Backup integrity threats |
| **CrowdStrike Falcon Complete** | Proprietary | Agentic MDR | 1 min MTTC | (Managed remediation) | ❌ | Fastest containment + AI governance |
| **SentinelOne Vigilance** | Proprietary | Tiered MDR | 1-4 hr investigation | ✅ Respond Pro | ❌ | Tiered options + forensics |
| **Arctic Wolf Aurora** | Proprietary | Proactive MDR | (Guided) | (Concierge) | ❌ | Risk reduction + posture |
| **Rapid7 Managed Threat** | Proprietary | MXDR + VRM | (Check) | ✅ Unlimited IR | ❌ | Consolidated MDR + VM |
| **Expel MDR** | Proprietary | Transparent MDR | 14 min MTTR | (Human-executed) | ❌ | Transparency + existing stack |
| **ReliaQuest GreyMatter** | Proprietary | Agentic AI SecOps | 4.48 min contain | (AI + human) | ❌ | Full agentic lifecycle |
| **Wazuh** | GPL-2.0 | SIEM/XDR | (Configurable) | ❌ (DIY) | ✅ | Build your own foundation |
| **TheHive & Cortex** | AGPL-3.0 | Case mgmt + enrichment | (Workflow) | ❌ (DIY) | ✅ | Investigation + enrichment |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source tool that provides MDDR/MDR capabilities or a commercial platform that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** The open-source landscape for **fully managed detection and response** is **essentially nonexistent**—MDDR/MDR is fundamentally a human service (24/7 analysts) combined with technology, which open-source projects cannot provide as a turnkey offering. The available open-source tools provide the **technical foundation**: **Wazuh** delivers the detection, FIM, vulnerability management, and active response capabilities that a SOC needs , while **TheHive & Cortex** provide the case management and automated enrichment layer [from previous context]. Organizations wanting an open-source MDDR approach must combine these tools with their own staff or an MSP to deliver the managed service component. On the commercial side, **Druva MDDR** is uniquely focused on **backup data threats** (snapshot deletion, backup set deletion) rather than general endpoint/identity threats [citation:1], while **CrowdStrike Falcon Complete** and **ReliaQuest GreyMatter** lead on autonomous/agentic response speed [citation:2][citation:11], and **Expel** differentiates on transparency with its existing-stack approach [citation:6].

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
