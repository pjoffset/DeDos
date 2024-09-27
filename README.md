## Summary

The Smart India Hackathon 2024 presented a problem statement titled "DDoS Protection System for Cloud: Architecture and Tool" under the theme of Blockchain and Cybersecurity. Team Semi-Hyperbola, with ID 4, proposed a national-level DDoS protection framework called DeDoS to address this challenge.

DeDoS is designed as a software framework that can be set up on dedicated servers nationwide. It employs an algorithm for detecting DDoS attacks and leverages content delivery networks (CDNs) on central servers across the nation to reduce the intensity of attacks.

DDoS attacks are a significant problem, with around 36,000 such attacks taking place worldwide every day. State-sponsored hacktivist groups may target critical government websites or real-time systems. While commercial players like Cloudflare, Akamai, and Azure offer DDoS protection solutions, the proposed DeDoS framework allows the government to implement an indigenous server dedicated to handling DDoS traffic, which can be used by all government web applications as well as private business applications.

The technical approach for DeDoS includes automated response mechanisms like rate limiting, geo-blocking, and web application firewalls. It also incorporates traffic scrubbing, recovery mechanisms, health checks, firewalls, intrusion prevention systems, and machine learning algorithms to identify and mitigate unusual traffic patterns. Open-source DDoS mitigation tools and technologies will be utilized to provide basic protection and customization for specific needs.

The feasibility and viability of DeDoS lie in its ability to provide indigenous DDoS protection for all critical government infrastructure, saving money compared to outsourcing to commercial solutions. However, developing an in-house solution requires a dedicated and expensive setup, especially for handling large data with AI and machine learning algorithms. Automated mitigation strategies like IP blocking and rate limiting can be integrated to address these challenges.

## Technical Details

### DDoS Attacks and Their Impact

A DDoS (distributed denial-of-service) attack is a method of disrupting the normal functioning of a target network or server by overwhelming it with large volumes of internet traffic. These attacks are conducted remotely by an attacker using networks of devices infected with malware, known as bots or botnets. During an attack, each bot submits requests to the target's IP address, aiming to overwhelm the target with requests and lead to denial-of-service for legitimate traffic[1].

DDoS attacks have a significant impact on web applications and services. Worldwide, around 36,000 DDoS attacks take place every day, and any state-sponsored hacktivist group may target critical government websites or real-time systems[1]. These attacks can lead to downtime, data breaches, and financial losses for the affected organizations.

### Existing DDoS Protection Solutions

Several commercial players offer DDoS protection solutions, including Cloudflare, Akamai, Azure, and others. These solutions typically provide services such as traffic scrubbing, content delivery networks (CDNs), and machine learning algorithms to identify and mitigate unusual traffic patterns[1].

However, the proposed DeDoS framework aims to provide an indigenous solution for the government of India, allowing them to implement a dedicated server for handling DDoS traffic. This server can be used by all government web applications as well as private business applications, potentially saving money compared to outsourcing to commercial solutions[1].

### Technical Approach for DeDoS

The DeDoS framework incorporates several features and techniques to detect, mitigate, and recover from DDoS attacks:

#### Automated Response Mechanisms
- **Rate Limiting**: Automatically limit the rate of incoming requests from individual IP addresses or IP ranges or redirect them to CAPTCHA or interstitial pages[1].
- **Geo-Blocking**: Block traffic from specific geographic regions if the attack originates from those areas[1].

#### Web Application Firewall
- Deploy a Web Application Firewall to filter and monitor HTTP requests, blocking malicious traffic based on predefined rules and patterns[1].

#### Traffic Scrubbing
- Deploy scrubbing services that filter malicious traffic before it reaches the infrastructure[1].

#### Recovery Mechanisms
- Implement automatic backup servers or regions in the event of an attack or infrastructure failure[1].
- Deploy CDNs to increase the availability of bandwidth to deflect the strongest DDoS attacks[1].

#### Health Checks
- Use health checks to monitor the status of services and automatically redirect traffic if a service becomes unresponsive[1].

#### Firewalls and Intrusion Prevention Systems
- Deploy advanced firewalls and IPS to detect and block malicious traffic with the help of machine learning[1].

#### Machine Learning
- Utilize machine learning algorithms to identify and mitigate unusual traffic patterns[1].

#### Open-Source Tools
- Utilize open-source DDoS mitigation tools and technologies, such as Fail2Ban and Snort, which can provide basic protection and be customized for specific needs[1].

### Feasibility and Viability Considerations

The feasibility and viability of the DeDoS framework depend on several factors:

- **Cost**: Operating the framework on a dedicated national DDoS management server capable of handling high throughput can drive up costs[1].
- **Indigenous Protection**: Once implemented, the DeDoS framework can provide indigenous DDoS protection for all critical government infrastructure[1].
- **Cost Savings**: Developing an in-house DDoS protection solution instead of outsourcing to commercial solutions can save money in the long run[1].
- **AI and Machine Learning**: Implementing AI and machine learning algorithms requires a dedicated and expensive setup, especially when handling large amounts of data[1].
- **Automated Mitigation**: Strategies like IP blocking and rate limiting can be integrated into the DeDoS framework to provide automated mitigation capabilities[1].

### Research and Reference Articles

1. Wikipedia article on DDoS mitigation: https://en.wikipedia.org/wiki/DDoS_mitigation
2. Cloudflare's guide on what is a DDoS attack: https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/
3. AWS Shield: DDoS attack protection: https://aws.amazon.com/shield/ddos-attack-protection/
4. Research paper by Rashmi V. Deshmukh and Kailas K. Devadkar: https://www.sciencedirect.com/science/article/pii/S1877050915007541
5. Research paper by Anshuman Singh and Brij B. Gupta: https://www.researchgate.net/publication/363114413_Distributed_Denial-of-Service_DDoS_Attacks_and_Defense_Mechanisms_in_Various_Web-Enabled_Computing_Platforms_Issues_Challenges_and_Future_Research_Directions

Citations:
[1] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/33761817/33b7ddef-11c5-4c24-a744-93421f0804f5/DDOS_SIH_v1-2.pptx
