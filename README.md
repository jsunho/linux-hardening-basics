# linux-hardening-basics
A practical roadmap and hands-on exercises to learn Linux hardening basics.

# Linux Hardening Lab

This project documents a reproducible Linux hardening lab built on a macOS M1 host using UTM virtualization.
The goal of this environment is to learn and demonstrate practical system-hardening techniques applied to a Linux server—covering system security, access control, auditing, service minimization, and secure configuration.

This repository is designed to show hands-on security skills relevant for IT administration, system integration, and entry-level cybersecurity roles.

## Summary

This lab simulates a real-world scenario where a newly installed Linux system must be hardened according to best practices.
It includes documentation, configuration examples, analysis of insecure defaults, and before/after comparisons.

**Skills Demonstrated**

* Secure Linux installation
* User & permission hardening
* SSH hardening
* Firewall configuration
* System service reduction
* Logging & auditing (auditd)
* Basic intrusion detection setup
* Security benchmarking (Lynis)

---

## 1. Lab Architecture Overview

The environment consists of:

* **1× macOS Host** (Apple Silicon)
* **1× Linux VM** (Ubuntu Server ARM64 or Debian ARM64)
* **UTM virtualization**, configured with:

  * Virtual network (NAT)
  * Shared folder (optional)
  * Snapshot checkpoints for hardening stages

The VM acts as a sandbox where hardening steps can be applied safely and documented thoroughly—mirroring how administrators secure production systems.

---

## 2. System Overview

The hardened VM includes the following components:

* Linux OS (fresh installation)
* SSH server for remote access
* UFW or nftables firewall
* auditd for event logging
* Lynis for security auditing
* Optional:

  * Fail2ban
  * AppArmor profile adjustments

A baseline system snapshot is kept for comparison with the final hardened state.

---

## 3. Hardening Scope

The project focuses on essential hardening tasks useful in enterprise environments:

### Access Control

* Enforced password rules
* Removal of default accounts
* Principle of least privilege
* Use of sudo with logging

### Network & Remote Access

* SSH hardening (key-based auth, disabled root login, limited users)
* Firewall policies
* Port restriction and service minimization

### System Integrity & Monitoring

* auditd rules
* Log rotation and protection
* File integrity checking (optional)

### Service Hardening

* Disabling unnecessary daemons
* Securing systemd services
* Correcting file permissions

### Security Assessment

* Running **Lynis** before/after hardening
* Documenting findings and remediations

---

## 4. Repository Structure

```
├── README.md
├── docs/
│   ├── 01_intro.md
│   ├── 02_vm_setup.md
│   ├── 03_baseline_scan.md
│   ├── 04_hardening_steps.md
│   ├── 05_firewall_config.md
│   ├── 06_auditd_config.md
│   ├── 07_security_scan_results.md
│   └── screenshots/
└── scripts/
    ├── auditd_rules.sh
    ├── harden_ssh.sh
    └── install_tools.sh
```

Each file documents a specific part of the process so the entire hardening procedure is reproducible.

---

## 5. Current Status

* [ ] VM created on UTM
* [ ] Fresh Linux installation completed
* [ ] Baseline system scan performed (Lynis)
* [ ] User & permission hardening
* [ ] SSH hardening and key-based auth
* [ ] Firewall configured
* [ ] auditd installed and rules applied
* [ ] Post-hardening scan completed
* [ ] Final documentation polishing

---

## 6. Key Learnings

During the project I worked with:

* Virtualization on Apple Silicon
* Secure configuration of Linux systems
* Concepts like least privilege, minimization, and defense-in-depth
* SSH security fundamentals
* System auditing and event analysis
* Writing reproducible technical documentation
* Identifying real-world misconfigurations and fixing them

This project reflects practical skills used in IT infrastructure, system administration, and cybersecurity operations.

---

## Goals of the Project

* Build a repeatable Linux-hardening lab
* Apply real security best practices
* Learn to audit and evaluate system security
* Document the entire process for recruiters and peers
* Provide a portfolio-ready example of hands-on skills

---

## License

MIT License

---

## Notes

Apple Silicon requires ARM64 Linux distributions for native performance.
Snapshots are recommended between hardening stages for rollback and comparison.

---

