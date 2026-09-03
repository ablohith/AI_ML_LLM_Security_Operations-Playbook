# 🛡️ AI / ML / LLM Security-Playbook


This document provides a structured overview of **AI Security**, **ML Security**, and **LLM Security**, along with operational practices (AISecOps, MLSecOps, LLMSecOps) and tools/frameworks for security testing.

-  Covering fundamentals, risks, and defenses.
-  Includes introductions to Basics, Security concepts, Walkthroughs, Top 10 vulnerabilities, Hands-on tools, and practical mitigation strategies.
-  Designed for researchers, developers, and security professionals working to secure AI systems.
-  This playbook introduces the growing field of **AI Security**.

---

## 📖 Table of Contents
1. AI Security
2. LLM Security
3. AIML Security Overview
4. AISecOps / MLSecOps / LLM_SecOps
5. Tools & Frameworks
6. Conclusion

---
# 🤖 AI Security

AI Security focuses on protecting artificial intelligence systems from threats such as:

- **Data poisoning** (malicious training data)
- **Model inversion** (extracting sensitive data from models)
- **Adversarial attacks** (inputs crafted to mislead AI)
- **Prompt injection** (manipulating LLM instructions)

---
## 📊 AIML Security Overview
Covers security across **AI and ML pipelines**:
- **Supervised Learning**: Risks from mislabeled or poisoned datasets
- **Unsupervised Learning**: Risks from clustering manipulation
- **Reinforcement Learning**: Risks from reward hacking
- **Deep Learning**: Vulnerabilities in neural networks (e.g., adversarial examples)
- OWASP ML Top 10 2023
  
---
# 🗣️ LLM Security

LLM Security addresses risks specific to **Large Language Models**:
- Inspired by OWASP Top 10, adapted for LLMs
- Includes Prompt Injection, Data Exfiltration, Model Misuse, Insecure Plugins, etc.
- **Prompt Injection** (Malicious input overriding system instructions), **Data Leakage** (Sensitive information revealed unintentionally), **Model Misuse** (Using LLMs for harmful or unintended purposes)
- **Categories** Direct and Indirect injection
- Real-world implications: data leakage, bypassing guardrails

## 🧪 Prompt Injection Lab Write‑Ups
### Objectives
- Understand prompt injection attacks
- Explore **LLM Top 10 risks**
- Practice bypassing model defenses
- Learn mitigation strategies

### Walkthrough
1. Reconnaissance — observe Gandalf’s restrictions
2. Simple injection attempts — direct override
3. Indirect prompting — role-play, translation
4. Advanced techniques — encoding, multi-step bypass
5. Success — document the injection that revealed the secret


---
##  📊 AIML Security Overview
Covers security across **AI and ML pipelines**:
- **Supervised Learning**: Risks from mislabeled or poisoned datasets
- **Unsupervised Learning**: Risks from clustering manipulation
- **Reinforcement Learning**: Risks from reward hacking
- **Deep Learning**: Vulnerabilities in neural networks (e.g., adversarial examples)

---

## ⚙️ AISecOps / MLSecOps / LLMSecOps
Operational practices for embedding security into AI/ML/LLM workflows:
- **AISecOps**: Security practices across AI systems
- **MLSecOps**: Secure ML lifecycle (data, training, deployment)
- **LLMSecOps**: Guardrails, monitoring, and defenses for LLMs
- Focus on **continuous monitoring**, **incident response**, and **secure deployment pipelines**

---

## 🛠️ Tools & Frameworks for Security Testing

### For AI Security
- **Adversarial Robustness Toolbox (ART)** — IBM framework for testing adversarial attacks
- **CleverHans** — Library for adversarial example generation
- **AI Fairness 360** — Bias detection and mitigation

### For ML Security
- **TensorFlow Privacy** — Differential privacy for ML models
- **MLflow Security Extensions** — Secure experiment tracking
- **SecureFlag Labs** — Hands-on ML vulnerability labs

### For LLM Security
- **Bearer CLI** — Security scanning for AI/LLM applications  
  🔗 [Bearer CLI Rules](https://docs.bearer.com/reference/rules)
- **Guardrails AI** — Framework for safe LLM outputs
- **LangChain Security Modules** — Secure prompt and tool integration

### For MLSecOps / LLMSecOps / AISecOps
- **Nave Security FDA Checklist** — Documentation and compliance guidance  
  🔗 [FDA Documentation Checklist](https://resources.navesecurity.com/fda-documentation-checklist-641102)
- **SecureFlag Knowledge Base** — Vulnerability references (e.g., NoSQL Injection)  
  🔗 [NoSQL Injection Vulnerability](https://knowledge-base.secureflag.com/vulnerabilities/nosql_injection/nosql_injection_vulnerability.html)
- **OWASP AI Security Top 10** — Community-driven list of AI/ML/LLM risks
- **Custom Security Dashboards** — For monitoring scan results and compliance

---

## Certifications: 

### EC-Council’s Certified Ethical Hacker (C|EH) v13
- The Leading Ethical Hacking Course with AI Integration 
- Link: https://ethicalhacking.eccouncil.org/certified-ethical-hacker-ceh-v13-international
  
### The SecOps Group: Certified AI/ML Pentester (C-AI/MLPen)
- Preparation: Self study on the Labs in Writeups section - https://github.com/ablohith/AI-Security-Playbook/tree/main/Writeups/Gandalf
- Link: https://pentestingexams.com/certifications/professional/certified-ai-ml-pentester/

### The SecOps Group: Certified Agentic AI Pentester (C-AgAIPen)
- Preparation: Self study on the Labs in Writeups section - https://github.com/ablohith/AI-Security-Playbook/tree/main/Writeups/Gandalf
- Link: https://pentestingexams.com/certifications/professional/certified-agentic-ai-pentester/

### Certified LLM Security Expert (CLLMSE)
- Handbook: https://drive.google.com/file/d/1fLN1ZHq5HED2GtWp6LKFALaD9Hbk0tnG/view?usp=sharing
- Lab: https://github.com/Red-Team-Leaders/RTL-Labs/blob/main/cllmse-practice-lab.zip: 
- Link: https://courses.redteamleaders.com/exams/73c286aa-2944-4f26-82ba-0ca14a05a4b7

### Certified LLM Security Professional (CLLMSP)
- Handbook: https://drive.google.com/file/d/1fLN1ZHq5HED2GtWp6LKFALaD9Hbk0tnG/view?usp=sharing
- Lab: https://github.com/Red-Team-Leaders/RTL-Labs/blob/main/cllmse-practice-lab.zip
- Link: https://courses.redteamleaders.com/exams/21f669cb-8f17-4d18-8a7c-a34c055aee85

---

## Mitigation Strategies

| **Threat** | **Description** | **Mitigation Strategy** |
| --- | --- | --- |
| Prompt Injection | Malicious input overrides system instructions | Guardrails, input sanitization, external filters |
| Data Poisoning | Corrupted training data manipulates model behavior | Data validation, provenance tracking |
| Model Inversion | Extracting sensitive training data from models | Differential privacy, access controls |
| Adversarial Examples | Crafted inputs mislead ML/AI models | Adversarial training, robustness testing |
| Data Leakage | Sensitive info unintentionally revealed | Output filtering, redaction, monitoring |
| Reward Hacking (RL) | Exploiting reward signals in reinforcement learning | Secure reward design, simulation testing |
| Plugin/Tool Abuse (LLM) | Exploiting integrations with external systems | Sandboxing, strict allow-listing, monitoring |
| Privilege Escalation | Prompt injection modifies system configurations | Least privilege, config hardening, audit trails |

---

### Standards:
- https://owasp.org/www-project-top-10-for-large-language-model-applications/assets/PDF/OWASP-Top-10-for-LLMs-2023-v1_1.pdf
- **LLM01:2025 Prompt Injection** https://genai.owasp.org/llmrisk/llm01-prompt-injection/
- **LLM07:2025 System Prompt Leakage** https://genai.owasp.org/llmrisk/llm072025-system-prompt-leakage/
- **LLM Prompt Injection: Direct MITRE ATLAS** https://atlas.mitre.org/techniques/AML.T0051.000
- **LLM Prompt Injection: Indirect MITRE ATLAS** https://atlas.mitre.org/techniques/AML.T0051.001
- **LLM Jailbreak Injection: Direct MITRE ATLAS** https://atlas.mitre.org/techniques/AML.T0054

### References & Useful Links

- https://learnprompting.org/docs/prompt_hacking/injection 
- https://github.com/Cranot/chatbot-injections-exploits
- https://oza1r.medium.com/defeat-gandalf-the-powerful-ai-wizard-in-2-hours-writeup-fe8ee45be5a3
- https://news.ycombinator.com/item?id=36094426
- https://ctf.support/misc/prompt-injection/
- https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Prompt%20Injection/README.md#story-generation
- [Bearer CLI Rules](https://docs.bearer.com/reference/rules)  
- [FDA Documentation Checklist – Nave Security](https://resources.navesecurity.com/fda-documentation-checklist-641102)  
- [NoSQL Injection Vulnerability – SecureFlag](https://knowledge-base.secureflag.com/vulnerabilities/nosql_injection/nosql_injection_vulnerability.html)  
- [Unsafe Code Reference – Microsoft Learn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/unsafe-code)

---

## Conclusion
LLMs are powerful but vulnerable.  
By studying labs like Gandalf and applying defensive strategies, we can build **secure AI systems** that resist manipulation.

