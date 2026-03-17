# `Wazuh SIEM & Linux Honeypot: Monitoring through Google Cloud Platform (GCP)`

This project involves the deployment of a live Linux Honeypot on GCP, monitored by a Wazuh (SIEM) manager. By intentionally exposing the instance to the public internet, I captured and analyzed real-time adversary behavior, mostly including brute force login attempts through ssh.
-

---

## Threat Hunting: Event Count Dashboard

<img width="1855" height="961" alt="Screenshot from 2026-03-16 15-29-35" src="https://github.com/user-attachments/assets/5de64909-9625-4156-927e-a1ffd8f4151a" />

---

Once the honeypot was live, it was targeted by botnets within minutes. Hundreds of login attempts occuring every hour. 

Key Metrics

    Timespan: 25 hours 
    
    Total Alerts: 1,809

    Authentication Failures: 1,514

    Authentication Successes: 0 (System remained secure)

    Top Alert: sshd: Attempt to login using a non-existent user

---

## MITRE ATT&CK Framework: Event Count Dashboard

A feature of Wazuh is incorporating the MITRE ATT&CK Framework to analyze the types of tactics and techniques adversaries are employing to try and break into the systems. The top tactics included credential access and lateral movement, employed by password guessing ssh login credentials. 

---

<img width="1855" height="961" alt="Screenshot from 2026-03-16 15-37-19" src="https://github.com/user-attachments/assets/35c566e8-0ee8-41bf-aa93-9a4d4bfa7125" />

---

## Source IP Address Visual Map

Another feature of Wazuh includes creating visualization maps.  The map below visualizes the geographic origin of these connection attempts.

Observation: 

    Ingress of traffic orginated from Africa, Asia, Europe, North America, South America, and Oceania.
    Source ip addresses encompass the globe for automated scanning bots.

<img width="1855" height="961" alt="Screenshot from 2026-03-16 15-35-16" src="https://github.com/user-attachments/assets/9e97e2d3-0519-4ce7-85d0-e58e61101ca4" />

--- 

## Conclusion
This project highlights the necessity of active monitoring in cloud environments. 

**Key Takeaway:** SIEM tools like Wazuh provide the visibility needed for actionable security intelligence.

**Next Steps:** Implement active responses to automatically block malicious IPs after a threshold of failed login attempts.

---

### Technical Appendix: Screenshot Gallery

Screenshots of further detailed alerts can be found in the [**/images**](./images) folder of this repository, along with the incorporated firewall setting for the linux honeypot, and google cloud console showing the two vm instances.
