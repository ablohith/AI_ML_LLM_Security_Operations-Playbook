# 🛡️ LLM Injection Mitigation Strategies

No one has found a **foolproof way** to fully address prompt injection vulnerabilities.  
While techniques like **Retrieval Augmented Generation (RAG)** and **fine-tuning** aim to make LLM outputs more relevant and accurate, research shows they do not completely mitigate these risks.

---

## 1. Constrain Model Behavior
- Provide specific instructions about the model’s role, capabilities, and limitations within the **system prompt**.  
- Enforce strict context adherence.  
- Limit responses to specific tasks or topics.  
- Instruct the model to ignore attempts to modify core instructions.

---

## 2. Define and Validate Expected Output Formats
- Specify clear output formats (e.g., JSON, structured text).  
- Request detailed reasoning and source citations.  
- Use deterministic code to validate adherence to these formats.

---

## 3. Implement Input and Output Filtering
- Define sensitive categories and construct rules for identifying and handling such content.  
- Apply **semantic filters** and use string-checking to scan for non-allowed content.  
- Evaluate responses using the **RAG Triad**:
  - Context relevance  
  - Groundedness  
  - Question/answer relevance  

---

## 4. Enforce Privilege Control and Least Privilege Access
- Provide the application with its own API tokens for extensible functionality.  
- Handle privileged functions in **code**, not via the model.  
- Restrict the model’s access privileges to the **minimum necessary** for its intended operations.

---

## 5. Require Human Approval for High-Risk Actions
- Implement **human-in-the-loop controls** for privileged operations.  
- Prevent unauthorized or unsafe actions by requiring manual approval.

---

## 6. Segregate and Identify External Content
- Separate and clearly denote **untrusted content**.  
- Limit its influence on user prompts and downstream outputs.

---

## 7. Conduct Adversarial Testing and Attack Simulations
- Perform regular **penetration testing** and breach simulations.  
- Treat the model as an **untrusted user** to test the effectiveness of trust boundaries and access controls.  

---

## ➕ Additional Mitigations Often Missed

### 8. Rate Limiting & Monitoring
- Limit the number of queries per user/session to reduce exposure.  
- Monitor for suspicious patterns (e.g., repeated jailbreak attempts).

### 9. Response Randomization & Diversity
- Avoid deterministic responses that attackers can exploit.  
- Introduce controlled randomness to reduce predictability.

### 10. Secure Logging & Audit Trails
- Log all interactions securely.  
- Use audit trails to detect and investigate injection attempts.

### 11. Continuous Model Updates
- Regularly retrain and patch models against newly discovered injection techniques.  
- Incorporate adversarial datasets during fine-tuning.

### 12. Defense-in-Depth Architecture
- Combine multiple layers of defense:  
  - Input validation  
  - Output filtering  
  - Privilege separation  
  - Monitoring & alerts  

---

## 📌 References
- [Nave Security FDA Checklist](https://resources.navesecurity.com/fda-documentation-checklist-641102)  
- [Bearer CLI Rules](https://docs.bearer.com/reference/rules)  
- [SecureFlag Knowledge Base](https://knowledge-base.secureflag.com/vulnerabilities/nosql_injection/nosql_injection_vulnerability.html)  
- [Microsoft Learn – Unsafe Code](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/unsafe-code)
