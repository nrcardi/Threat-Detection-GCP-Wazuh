# `Wazuh SIEM & Linux Honeypot: Monitoring through Google Cloud Platform (GCP)`

This project involves the deployment of a live Linux Honeypot on GCP, monitored by a Wazuh (SIEM) manager. By intentionally exposing the instance to the public internet, I captured and analyzed real-time adversary behavior, mostly including brute force login attempts through ssh.

Threat Hunting Event Count Dashboard:
-
<img width="1855" height="961" alt="Screenshot from 2026-03-16 15-29-35" src="https://github.com/user-attachments/assets/5de64909-9625-4156-927e-a1ffd8f4151a" />

Key Metrics

    Timespan: 25 hours 
    
    Total Alerts: 1,809

    Authentication Failures: 1,514

    Authentication Successes: 0 (System remained secure)

    Top Alert: sshd: Attempt to login using a non-existent user

MITRE ATT&CK Framework Dashboard:
-
<img width="1855" height="961" alt="Screenshot from 2026-03-16 15-37-19" src="https://github.com/user-attachments/assets/35c566e8-0ee8-41bf-aa93-9a4d4bfa7125" />

blah blah blah

                              Source IP Address Visual Map
                                                      
Once the honeypot was live, it was targeted by automated scanners and botnets within minutes. The map below visualizes the geographic origin of these connection attempts.
-
Observation: A high volume of ingress traffic was observed originating from East Asia, North America, and Europe, highlighting the global nature of automated scanning bots.

<img width="1855" height="961" alt="Screenshot from 2026-03-16 15-35-16" src="https://github.com/user-attachments/assets/9e97e2d3-0519-4ce7-85d0-e58e61101ca4" />
