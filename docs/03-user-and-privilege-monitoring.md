# User Creation and Privilege Escalation Monitoring

## Objective

Validate that Wazuh is able to detect user management activities and privilege escalation events on a Linux server.

---

## Environment

| Component | Version |
|-----------|----------|
| Operating System | Ubuntu Server 24.04 LTS |
| SIEM | Wazuh 4.12 |
| Agent | Local Agent |
| Attack Machine | Kali Linux (not used in this scenario) |

---

## Scenario

As part of the SOC homelab validation process, administrative actions were performed on the monitored Ubuntu server.

The goal was to verify whether Wazuh successfully collected and indexed security events related to user management and privilege escalation.

---

## Actions Performed

### 1. Created a new Linux user

```bash
sudo adduser socuser
```

### 2. Switched to the root account

```bash
sudo su
```

---

## Detection

Wazuh successfully generated security events related to:

- User creation
- User management
- Privilege escalation
- sudo execution
- Authentication events

The generated alerts were available through the Wazuh Dashboard.

---

## Investigation

During the analysis it was possible to identify:

- Timestamp of the event
- Username that executed the command
- Hostname
- Executed process
- Event description
- Rule level
- Related Linux logs

---

## Security Impact

Privilege escalation events are extremely important because they may indicate:

- Legitimate administrative activity
- Unauthorized privilege escalation
- Compromised credentials
- Insider threats

Continuous monitoring of these events is essential for Security Operations Centers (SOC).

---

## Evidence

Screenshots available in:

```

screenshots/

```

Example:

- user-created.png
- sudo-su-alert.png

---

## Lessons Learned

This exercise demonstrated that Wazuh is capable of:

- Monitoring Linux authentication events
- Detecting administrative actions
- Logging privilege escalation attempts
- Providing centralized visibility through the dashboard

This validation confirms that the SIEM is correctly ingesting and analyzing Linux security events.

---

## Skills Demonstrated

- Linux Administration
- Wazuh SIEM
- Security Monitoring
- Log Analysis
- Privilege Escalation Detection
- Security Event Investigation
- Ubuntu Server