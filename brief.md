Version: NAFATH-V4
Track: Networking

Overview
A software supply chain encompasses the software, libraries, tools, AI models, mobile applications, network infrastructure, and data utilized for creating and delivering digital services. If any part of this chain is compromised, attackers can jeopardize the security, reliability, and privacy of the entire service. For a telecommunications service provider, safeguarding this supply chain is crucial, as customers rely on secure connectivity and trustworthy digital systems. This exploration delves into six interconnected domains: Software, AI, Mobile, Networking, Cybersecurity, and Data. Each domain highlights significant risks, practical security measures, and dependable resources for further exploration. Collectively, these subjects emphasize the importance of considering security throughout the development, deployment, and upkeep of technology.For the Networking track, understanding BGP route hijacking and the safeguards that reduce the risk of unauthorized traffic redirection is essential to protecting national telecommunications services.

Software
The Twelve-Factor App recommends storing configuration in environment variables rather than hard-coding it in application code. Configuration includes deployment-specific values such as database credentials and external service settings. Separating configuration from code allows the same application to run in different environments without code changes. It also reduces the risk of accidentally committing secrets to version control. Sensitive credentials should be managed with appropriate access controls and should never be embedded directly in source code.
Resource: The Twelve-Factor App - Config - https://12factor.net/config

AI
AI security encompasses threats known as "adversarial machine learning"—a category of attacks that exploit vulnerabilities inherent in intelligent models. The National Institute of Standards and Technology (NIST) classifies these attacks into two primary types: evasion attacks, which involve modifying inputs to mislead the system and elicit an incorrect prediction; and poisoning attacks, which target training data by injecting misleading information to manipulate the model's behavior. Consequently, guidelines urge organizations to assess these risks throughout the various stages of the AI ​​lifecycle and implement appropriate safeguards to mitigate their impact.
Resource: AI 100-2 E2025, Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - https://csrc.nist.gov/pubs/ai/100/2/e2025/final

Mobile
The OWASP Mobile Application Security Verification Standard (MASVS) provides the security controls necessary to protect mobile applications across various domains, including secure storage, cryptography, authentication, network communication security, platform interaction, code quality, system resilience, and privacy protection. Development teams and security testers use these controls as a primary reference for security assessment, while also relying on the organization’s "Mobile Application Security Testing Guide" (MASTG) for the practical methods and steps required to effectively verify that these standards are implemented.
https://mas.owasp.org/MASVS/

Networking
The Border Gateway Protocol (BGP) allows networks to exchange routing information over the internet, but it is vulnerable to "route hijacking" incidents. In these incidents, an independent system falsely claims an IP address range that it does not own, causing data traffic to be diverted through unintended routes. To counter this, the "BGP Domain Origin Verification" feature aims to ensure that the claiming system is legitimately using that domain. Therefore, network operators are advised to verify route origins and monitor for any suspicious claims. While this measure reduces the risk, it does not completely prevent all routing attacks.
Resource: RFC 6811: BGP Prefix Origin Validation - https://www.rfc-editor.org/rfc/rfc6811.html

Cybersecurity
Log4Shell, classified as CVE-2021-44228, is a critical vulnerability that affects select versions of the widely used Java event logging library, Apache Log4j 2. Under compromised circumstances, log messages controlled by third parties can trigger JNDI lookups, leading to remote code execution. To address this, organizations must identify affected applications and dependencies, upgrade to secure versions compatible with their Java environment, and ensure that vulnerable components are completely removed; Maintaining a comprehensive inventory of software dependencies helps teams discover exposure points and address them efficiently.
Resource: Security - Apache Logging Services - https://logging.apache.org/security.html

Data
A Software Bill of Materials (SBOM) is a structured inventory of software components and their relationships. It helps organizations identify dependencies, investigate newly disclosed vulnerabilities, and determine which products may be affected. NTIA's minimum elements include the supplier name, component name, component version, other unique identifiers, dependency relationships, SBOM author, and timestamp. An SBOM improves visibility into the software supply chain, but it does not by itself prove that software is secure or free of vulnerabilities.
Resource: The Minimum Elements For a Software Bill of Materials (SBOM) - https://www.ntia.gov/report/2021/minimum-elements-software-bill-materials-sbom

Misconception in My Track
A common misconception is that RPKI-based BGP origin validation completely prevents route hijacking. In fact, RFC 6811 explains that this mechanism checks the authorized origin of a route but does not validate the complete network path. It also provides only limited protection against a determined attacker. Network operators should therefore combine origin validation with routing policies, monitoring, and incident response. Origin validation is an important safeguard, but it is not a complete defense against every BGP attack.

Supporting section: RFC 6811, Section 6, "Security Considerations."

Supporting sentence from the source: "This mechanism does not protect against "AS-in-the-middle attacks" or provide any path validation."

Open Question

How can a national telecommunications provider combine RPKI-based route origin validation, routing policy, and real-time monitoring to detect and respond to BGP hijacking while minimizing the risk of blocking legitimate routes?
