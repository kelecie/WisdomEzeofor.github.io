# Home Security Lab - Splunk SIEM Deployment

## Project Overview

**Objective:** Deploy a functional SIEM environment using Splunk Enterprise to collect, analyze, and visualize security events from a Windows 11 system.

**Date Started:** January 22, 2025  
**Status:** 🟡 In Progress  
**Estimated Completion:** January 24, 2025

---

## Project Scope

This project demonstrates:
- ✅ SIEM deployment and configuration
- ✅ Log collection architecture design
- ✅ Windows security event monitoring
- ✅ Security event analysis and correlation
- ✅ Dashboard creation for security operations
- ✅ Technical documentation skills

---

## Lab Architecture

### Components
- **SIEM Platform:** Splunk Enterprise 9.1.2 (Free License - 500MB/day)
- **SIEM Server OS:** Ubuntu Server 22.04 LTS (VirtualBox VM)
- **Log Source:** Windows 11 Professional (Host Machine)
- **Log Forwarder:** Splunk Universal Forwarder 9.1.2
- **Virtualization:** Oracle VirtualBox 7.0
- **Host System:** 
  - OS: Windows 11
  - RAM: [Your RAM amount]
  - Processor: [Your CPU]

### Network Architecture
```
Windows 11 Host (192.168.x.x)
    │
    ├─► Splunk Universal Forwarder (Port 9997)
    │   └─► Collects: Windows Security Logs, Application Logs, System Logs
    │
    └─► VirtualBox
        └─► Ubuntu VM (192.168.x.x)
            └─► Splunk Enterprise (Port 8000 - Web, Port 9997 - Receiver)
```

### Data Flow
1. Windows 11 generates security events (logins, file access, process creation)
2. Splunk Universal Forwarder captures event logs
3. Forwarder sends logs to Splunk Enterprise (port 9997)
4. Splunk indexes and makes logs searchable
5. Security analyst (you) analyzes events via web dashboard

---

## Learning Objectives

By completing this project, I will demonstrate:

**Technical Skills:**
- [x] Deploy enterprise SIEM software
- [ ] Configure log collection and forwarding
- [ ] Understand Windows security event IDs
- [ ] Create SPL (Search Processing Language) queries
- [ ] Build security monitoring dashboards
- [ ] Set up real-time alerts
- [ ] Perform security event analysis

**Professional Skills:**
- [ ] Document technical projects clearly
- [ ] Create architecture diagrams
- [ ] Troubleshoot complex systems
- [ ] Follow security best practices

---

## Implementation Timeline

### Day 1 - Planning & Environment Setup ✅
- [x] Defined lab architecture
- [x] Installed VirtualBox
- [x] Downloaded Ubuntu Server ISO
- [x] Created project documentation
- [x] Documented objectives and scope

**Time Invested:** 45 minutes  
**Challenges:** None

### Day 2 - SIEM Server Deployment 🟡
- [ ] Create Ubuntu Server VM
- [ ] Install and configure Ubuntu
- [ ] Install Splunk Enterprise
- [ ] Configure Splunk to receive logs
- [ ] Verify web interface accessibility

**Target Time:** 60 minutes

### Day 3 - Log Collection Setup 🔲
- [ ] Install Splunk Universal Forwarder on Windows 11
- [ ] Configure forwarder to send to SIEM
- [ ] Enable Windows Security logging
- [ ] Generate test security events
- [ ] Verify log ingestion in Splunk

**Target Time:** 60 minutes

---

## Day 1 - Detailed Progress

### Environment Verification
- **Virtualization Status:** [Enabled/Disabled]
- **Available RAM:** [Your amount]
- **Free Disk Space:** [Your amount]
- **VirtualBox Version:** [Version installed]

### Downloads Completed
- ✅ VirtualBox 7.0.x
- ✅ Ubuntu Server 22.04 LTS ISO

### Documentation Created
- ✅ GitHub project structure
- ✅ README with architecture
- ✅ Implementation timeline

---

## Resources & References

### Official Documentation
- [Splunk Enterprise Documentation](https://docs.splunk.com/Documentation/Splunk/latest/Installation)
- [Splunk Universal Forwarder Guide](https://docs.splunk.com/Documentation/Forwarder/latest/Forwarder/Abouttheuniversalforwarder)
- [Ubuntu Server Guide](https://ubuntu.com/server/docs)

### Key Splunk Concepts
- **Indexer:** Stores and indexes data (our Ubuntu VM)
- **Forwarder:** Collects and forwards data (our Windows 11 host)
- **Search Head:** Interface for searching data (also our Ubuntu VM)

### Important Windows Event IDs to Monitor
- **4624:** Successful logon
- **4625:** Failed logon attempt
- **4672:** Special privileges assigned to new logon
- **4688:** New process created
- **4698:** Scheduled task created
- **4720:** User account created
- **4738:** User account changed

---

## Screenshots & Evidence

*Screenshots will be added as the project progresses*

### Planned Screenshots
- [ ] VirtualBox with Ubuntu VM running
- [ ] Splunk Enterprise login page
- [ ] Splunk Enterprise dashboard
- [ ] Forwarder configuration
- [ ] Log ingestion verification
- [ ] Security events in Splunk
- [ ] Custom dashboard

---

## Challenges & Solutions

*Will be documented as encountered*

---

## Key Takeaways

*To be completed at project end*

---

## Next Steps After This Project

- Create security monitoring dashboard
- Write blog post: "Setting Up Your First SIEM Lab"
- Build on this lab for Week 3 threat analysis project
- Add alerting rules for suspicious activities

---

## Project Files
```
projects/siem-lab/
├── README.md (this file)
├── screenshots/
│   └── (screenshots will go here)
├── configs/
│   ├── inputs.conf (Splunk forwarder config)
│   └── outputs.conf (Splunk forwarder config)
└── architecture/
    └── lab-diagram.png
```

---

*Last Updated: January 22, 2025*  
*Author: Wisdom Ezeofor*  
*GitHub: kelecie*
