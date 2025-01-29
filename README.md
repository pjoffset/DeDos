DeDoS Framework

## Overview

The **Smart India Hackathon 2024** presented a challenge titled **"DDoS Protection System for Cloud: Architecture and Tool,"** under the theme of Blockchain and Cybersecurity. Our Team **Semi-Hyperbola** proposed a national-level DDoS protection framework called **DeDoS** to tackle this issue.

### Key Features of DeDoS
- **National Software Framework**: Designed to be deployed on dedicated servers across the country.
- **DDoS Attack Detection**: Utilizes algorithms to identify DDoS attacks.
- **Content Delivery Networks (CDNs)**: Leverages CDNs on central servers to mitigate attack intensity.

### Importance of DDoS Protection
DDoS attacks are prevalent, with approximately **36,000 attacks occurring daily worldwide**. These attacks can disrupt critical government services and real-time systems, necessitating robust protective measures.

## Technical Approach

### Automated Response Mechanisms
- **Rate Limiting**: Controls the number of requests from individual IP addresses.
- **Geo-Blocking**: Blocks traffic from specific geographic regions during an attack.

### Web Application Firewall
- Filters and monitors HTTP requests to block malicious traffic based on predefined rules.

### Traffic Scrubbing
- Filters out harmful traffic before it reaches the server infrastructure.

### Recovery Mechanisms
- Automatic backup servers ensure continuity during attacks or failures.
- CDNs enhance bandwidth availability to deflect strong DDoS attacks.

### Health Checks
- Regular monitoring of service status to redirect traffic if necessary.

### Firewalls and Intrusion Prevention Systems (IPS)
- Advanced firewalls and IPS detect and block malicious traffic using machine learning.

### Machine Learning Integration
- Employs machine learning algorithms to recognize and respond to unusual traffic patterns.

### Open-Source Tools
- Utilizes tools like **Fail2Ban** and **Snort** for basic protection and customization.

## Feasibility and Viability

The DeDoS framework's viability hinges on several factors:
- **Cost Efficiency**: Offers indigenous protection at a potentially lower cost than commercial solutions.
- **Indigenous Development**: Provides a dedicated server for government applications, enhancing security.
- **AI Implementation**: Requires investment in AI and machine learning infrastructure.
- **Automated Mitigation Strategies**: Integrates techniques like IP blocking and rate limiting for effective defense.

## Code Snippets

Below are code snippets that illustrate basic functionalities that could be part of the DeDoS framework:

### Rate Limiting Example (Python)
```python
from flask import Flask, request, jsonify
from time import time

app = Flask(__name__)
requests = {}

@app.route('/api', methods=['GET'])
def api():
    ip = request.remote_addr
    current_time = time()

    # Initialize request count for the IP if not present
    if ip not in requests:
        requests[ip] = []

    # Filter out old requests
    requests[ip] = [req for req in requests[ip] if current_time - req < 60]

    # Check if rate limit is exceeded (e.g., more than 100 requests in 60 seconds)
    if len(requests[ip]) > 100:
        return jsonify({"error": "Rate limit exceeded"}), 429

    # Log the request time
    requests[ip].append(current_time)
    return jsonify({"message": "Request successful!"})

if __name__ == '__main__':
    app.run()
```

### Geo-Blocking Example (JavaScript)
```javascript
const express = require('express');
const app = express();

const blockedRegions = ['192.168.1.0/24']; // Example blocked IP range

app.use((req, res, next) => {
    const clientIp = req.ip;
    
    // Check if the client's IP is in the blocked regions
    if (blockedRegions.includes(clientIp)) {
        return res.status(403).send('Access denied from your region.');
    }
    
    next();
});

app.get('/', (req, res) => {
    res.send('Welcome!');
});

app.listen(3000, () => {
    console.log('Server running on port 3000');
});
```

## Conclusion

The DeDoS framework represents a proactive approach to combat DDoS attacks by leveraging indigenous resources and advanced technology. Its implementation could significantly enhance the security posture of critical governmental infrastructure while providing a cost-effective alternative to existing commercial solutions.

Citations:
[1] https://pib.gov.in/PressReleseDetailm.aspx?PRID=2083566
[2] https://engineersplanet.com/sih-problem-statements-blockchain-and-cybersecurity/
[3] https://www.pmindia.gov.in/en/news_updates/pm-interacts-with-participants-of-smart-india-hackathon-2024/
[4] https://pib.gov.in/PressReleaseIframePage.aspx?PRID=2083360
[5] https://www.sih.gov.in
[6] https://www.driems.ac.in/wp-content/uploads/2024/08/SIH_2024_PS.pdf
[7] https://www.sih.gov.in/sih2024PS
[8] https://qasih.mic.gov.in/sih2024PS
