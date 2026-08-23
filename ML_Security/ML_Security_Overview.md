#  📊 ML Security 


Covers security across **AI and ML pipelines**:
- **Supervised Learning**: Risks from mislabeled or poisoned datasets
- **Unsupervised Learning**: Risks from clustering manipulation
- **Reinforcement Learning**: Risks from reward hacking
- **Deep Learning**: Vulnerabilities in neural networks (e.g., adversarial examples)

---

This section outlines the **OWASP Top 10 ML security risks** for AI, ML, and LLM systems, with examples, mitigations, and references for further reading.

## 📊 Summary Table

| **ID**  | **Vulnerability**            | **Description**                                                                 | **Example**                                                   | **Mitigation**                                   | **Reference** |
|---------|-------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------|-------------------------------------------------|---------------|
| ML01    | Input Manipulation Attack     | Attackers modify input data to cause incorrect or malicious model outputs.       | Adversarial images misclassify objects                        | Adversarial training, input validation           | [IBM ART](https://github.com/Trusted-AI/adversarial-robustness-toolbox) |
| ML02    | Data Poisoning Attack         | Malicious data injected into training datasets compromises model performance.    | Poisoned spam filter training data                            | Data validation, provenance tracking             | [SecureFlag Labs](https://knowledge-base.secureflag.com/vulnerabilities/nosql_injection/nosql_injection_vulnerability.html) |
| ML03    | Model Inversion Attack        | Outputs are exploited to reconstruct sensitive training inputs.                   | Reconstructing patient records from outputs                   | Differential privacy, restricted query access    | [TensorFlow Privacy](https://www.tensorflow.org/privacy) |
| ML04    | Membership Inference Attack   | Model behavior reveals whether specific data was in training.                     | Detecting if a record was in training data                    | Regularization, privacy-preserving training      | [AI Fairness 360](https://aif360.mybluemix.net/) |
| ML05    | Model Theft                   | Attackers replicate a model by repeated queries.                                 | Replicating LLM via repeated queries                          | Rate limiting, watermarking, API monitoring      | [OWASP AI Security Top 10](https://resources.navesecurity.com/fda-documentation-checklist-641102) |
| ML06    | AI Supply Chain Attacks       | Vulnerabilities exploited in ML supply chain components.                         | Compromised pre-trained models from repositories              | Integrity checks, signed models, secure repos    | [Bearer CLI Rules](https://docs.bearer.com/reference/rules) |
| ML07    | Transfer Learning Attack      | Manipulated baseline models introduce bias/backdoors when fine-tuned.            | Injecting bias/backdoors into baseline NLP models             | Vetting pre-trained models, secure fine-tuning   | [Microsoft Learn Unsafe Code](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/unsafe-code) |
| ML08    | Model Skewing                 | Training data manipulated to skew model behavior.                                | Manipulating recommender systems to promote harmful content   | Balanced datasets, anomaly detection             | [OWASP AI Security Top 10](https://resources.navesecurity.com/fda-documentation-checklist-641102) |
| ML09    | Output Integrity Attack       | Model outputs intercepted and altered before use.                                | Altering chatbot responses in transit                         | Secure channels, cryptographic integrity checks  | [SecureFlag Knowledge Base](https://knowledge-base.secureflag.com/vulnerabilities/nosql_injection/nosql_injection_vulnerability.html) |
| ML10    | Model Poisoning               | Model weights manipulated to degrade performance or add backdoors.               | Manipulating neural network weights to force misclassification | Secure training pipelines, integrity monitoring  | [Nave Security FDA Checklist](https://resources.navesecurity.com/fda-documentation-checklist-641102) |

---
