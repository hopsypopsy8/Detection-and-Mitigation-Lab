# Detection-and-Mitigation-Lab

## Objective

Given that most defensive cybersecurity roles involve Security Information and Event Management (SIEM) systems and log analysis, I have decided to create a dedicated lab focused on these areas. The objective of the lab is to establish a controlled environment for simulating and detecting cyber attacks. The primary focus will be to ingest and analyze logs within a SIEM system, generating test telemetry to replicate real-world attack scenarios. This hands-on experience is intended to enhance my understanding of network security, attack methodologies, and defensive strategies, providing practical exposure to the tools and techniques commonly used in the field.

### Tools Used
- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Oracle Virtual Box, Associated Images for the Vulnerable Machine and Attacking Machine.

## Steps
From my initial assessment, I have two possible approaches for setting up my lab. The first option involves utalising Azure Sentinel to host a honeypot image with obviously very poor security exposed to the world. This would allow me to capture logs from external sources from practically anywhere. The second approach is more controlled and localized, where I would set up two virtual machines: one running Metasploitable2 and the other running Kali Linux. The Kali machine would be used to simulate attacks on the Metasploitable2 VM, with all actions and attempts being logged for analysis.

At this stage, I plan on pursuing both options, starting with the internal approach. Mostly because relying on external traffic to test specific attacks is not possible, which is why the setup where i attack myself is preferable (for now) . Also I'm not 100% sure ill get $200 worth of Azure use yet out of this lab so i'm going to save that (also for now).

I'm running the lab with two devices my offensive machine the "Threat Actor" running kali linux and the defensive machine running metasploitable2. 

If you're experiencing kernel panic while downloading the VM, check out this fix: https://medium.com/@dangerhulk26022022/how-to-solve-kernel-panic-not-syncing-io-apic-timer-doesnt-work-bfffe323a1f5 

### Metasploit and Splunk workaround
After setting up the two VMs i kind of realised how outdated metasploit is and accepted it wont be able to run Splunk (my SIEM of choice here), so im just going to send all the logs to Splunk running on my kali linux (LOL) 
