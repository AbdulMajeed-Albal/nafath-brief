Version: NAFATH-V3
Track: Cybersecurity
## Overview 
Launching a government AI chat assistant in a mobile app requires six IT fields to work together as one secure system. Software engineering uses semantic versioning to manage software releases without breaking features. Artificial intelligence uses Retrieval-Augmented Generation (RAG) to pull facts directly from official files, avoiding false information. Mobile development relies on App Transport Security (ATS) to force encrypted HTTPS traffic, while networking uses IPv6 to handle large volumes of connected devices smoothly. From a cybersecurity angle, the main goal is defending against prompt injection attacks that try to manipulate the model. Finally, data management uses anonymization and pseudonymization on chat logs to ensure compliance with data protection laws.
## Software
Under Semantic Versioning, the assistant's public API must increase its MAJOR version when introducing breaking changes that disrupt existing client integrations. A MINOR version increase is required when adding new features or endpoints in a backward-compatible manner. Finally, a PATCH version is used exclusively for backward-compatible bug fixes or minor performance patches.
Resource: Semantic Versioning 2.0.0 - https://semver.org/
## AI
Retrieval-Augmented Generation (RAG) is a technique that connects an AI model to an external, trusted database of official government documents. Instead of relying solely on pre-trained memory, RAG searches for relevant source material first and uses it to generate the response. This grounds the AI's answers in verified facts, drastically reducing hallucinated or incorrect information delivered to citizens.
Resource: Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks - https://arxiv.org/abs/2005.11401
## Mobile
iOS App Transport Security (ATS) enforces secure network connections by requiring all HTTP communications to use HTTPS with strong TLS protocols. If the mobile app attempts to connect to a plain, unencrypted HTTP endpoint, ATS blocks the request completely and returns an error. This default security measure prevents sensitive citizen data from being intercepted over public networks.
Resource: Preventing Insecure Network Connections - https://developer.apple.com/documentation/security/preventing_insecure_network_connections
## Networking
IPv6 differs from IPv4 primarily by expanding address length from 32 bits to 128 bits, using hexadecimal notation rather than decimal numbers. This change creates a virtually unlimited pool of unique IP addresses. As the count of connected devices grows, IPv6 is vital because it eliminates the shortage of IPv4 addresses. It allows every device to hold a direct connection without relying on network address translation, enabling smooth network expansion.
Resource: Internet Protocol, Version 6 (IPv6) Specification - https://datatracker.ietf.org/doc/html/rfc8200
## Cybersecurity
Prompt injection is a vulnerability where attackers manipulate an AI’s output using untrusted inputs. Direct injection occurs when a user enters malicious prompts directly into the chat interface. In contrast, indirect injection happens when the AI reads compromised external files or websites containing hidden malicious instructions. To lower these risks, organizations can implement strict input filtering and maintain a clear structural separation between system instructions and user inputs.
Resource: OWASP Top 10 for Large Language Model Applications - https://owasp.org/www-project-top-10-for-large-language-models/
## Data
Anonymization permanently alters personal data so an individual can never be identified again by any means. Pseudonymization, on the other hand, replaces personal identifiers with unique codes, meaning the original identity can still be restored using separately secured key data. Because anonymization makes data irreversibly non-personal, it is the only method that removes the information entirely from the scope of data protection laws, while pseudonymized data remains subject to regulations.
Resource: EDPB Guidelines on Anonymisation and Pseudonymisation Techniques - https://edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-042025-anonymisation-and-pseudonymisation_en
## Misconception in My Track
A common belief in cybersecurity is that prompt injection only happens through direct user text. Because of this, many people think that checking chat boxes for bad inputs makes the AI completely safe. However, indirect prompt injection can still happen when the AI reads outside files or websites that carry hidden bad commands. The OWASP Top 10 guide explains this under **LLM01: Prompt Injection**, showing that outside files can be just as dangerous to AI safety.
## Open Question
Next, I want to learn how to combine strong input safety checks with quick AI replies, so that security steps do not slow down the chat for users.
