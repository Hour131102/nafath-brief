Version: NAFATH-V4
Track: Networking

Overview
A software supply chain encompasses the software, libraries, tools, AI models, mobile applications, network infrastructure, and data utilized for creating and delivering digital services. If any part of this chain is compromised, attackers can jeopardize the security, reliability, and privacy of the entire service. For a telecommunications service provider, safeguarding this supply chain is crucial, as customers rely on secure connectivity and trustworthy digital systems. This exploration delves into six interconnected domains: Software, AI, Mobile, Networking, Cybersecurity, and Data. Each domain highlights significant risks, practical security measures, and dependable resources for further exploration. Collectively, these subjects emphasize the importance of considering security throughout the development, deployment, and upkeep of technology. The Networking section emphasizes BGP route hijacking and illustrates how Resource Public Key Infrastructure (RPKI) aids in validating route origins.

Software
The twelve-factor approach to applications emphasizes the importance of treating logs as flowing data sources, not as locally stored text files. It recommends that the application simply pump all events and logs into the standard output, leaving the task of collecting, routing, or archiving them to the operating environment or external tools. This approach prevents the application from worrying about log file management or size inflation, facilitating efficient and secure system monitoring and error analysis across centralized analysis platforms.
Resource: The Twelve-Factor App - Config - https://12factor.net/config

AI
AI security encompasses threats known as "adversarial machine learning"—a category of attacks that exploit vulnerabilities inherent in intelligent models. The National Institute of Standards and Technology (NIST) classifies these attacks into two primary types: evasion attacks, which involve modifying inputs to mislead the system and elicit an incorrect prediction; and poisoning attacks, which target training data by injecting misleading information to manipulate the model's behavior. Consequently, guidelines urge organizations to assess these risks throughout the various stages of the AI ​​lifecycle and implement appropriate safeguards to mitigate their impact.
Resource: AI 100-2 E2025, Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - https://csrc.nist.gov/pubs/ai/100/2/e2025/final

Mobile
The OWASP Mobile Application Security Verification Standard (MASVS) provides the security controls necessary to protect mobile applications across various domains, including secure storage, cryptography, authentication, network communication security, platform interaction, code quality, system resilience, and privacy protection. Development teams and security testers use these controls as a primary reference for security assessment, while also relying on the organization’s "Mobile Application Security Testing Guide" (MASTG) for the practical methods and steps required to effectively verify that these standards are implemented.
https://mas.owasp.org/MASVS/

Networking

Cybersecurity

Data

Misconception in My Track
