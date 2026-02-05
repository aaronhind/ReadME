# Incident Report – SSH Brute Force Attempt

Date: 2026-02-05  
Analyst: Aaron Hind

---

## Summary
Multiple failed SSH login attempts detected from external IP address indicating brute-force behavior.

---

## Timeline
10:12 – First failed login attempt  
10:13 – 25 rapid authentication failures  
10:14 – Alert triggered in SIEM

---

## Evidence
Log entries from /var/log/auth.log showing repeated failures:

Failed password for invalid user root from 192.168.1.25

---

## Analysis
Pattern indicates automated brute-force attempt. No successful login detected.

---

## Severity
Medium  
Attack unsuccessful but persistent.

---

## Recommended Action
- Block source IP
- Monitor for repeated attempts
- Enforce stronger authentication policies

---

## Lessons Learned
Early detection prevents account compromise. SIEM alerting worked as expected.

