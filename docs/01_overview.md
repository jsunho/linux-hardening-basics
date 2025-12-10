# Overview

This project explores the fundamentals of Linux system hardening using a structured, beginner-friendly workflow. The goal is to demonstrate how to create a measurable security baseline, apply targeted hardening steps, and verify the results with repeatable scans and logs. The repository is part learning exercise, part practical showcase of technical documentation and security methodology.

# Purpose of the Project

The project focuses on reducing the attack surface of a Linux system through configuration hardening, service minimization, logging improvements, and audit mechanisms. Instead of applying changes blindly, the workflow emphasizes conscious, verifiable steps that reflect realistic IT security practices.

# What This Repository Provides

* A reproducible Linux hardening workflow from initial setup to final verification
* Documentation for each stage: baseline scan, hardening actions, firewall configuration, auditd setup, and security scan results
* Simple automation scripts for common hardening tasks
* Before/after comparisons to demonstrate the impact of each change
* A clear learning path for newcomers to system security
  
# Intended Audience

This documentation is designed for learners, technical reviewers, recruiters, and training staff who want to evaluate or understand foundational Linux hardening techniques.

# Scope of the Project

The hardening focuses on practical, widely used areas, including:

* SSH configuration and access control
* Firewall policies
* System logging and monitoring
* auditd rules and event tracking
* Disabling unnecessary services
* Basic system parameter tuning (sysctl)
* Advanced or enterprise-grade topics—such as SELinux policies, kernel recompilation, or full compliance hardening—are intentionally out of scope to keep the project focused and accessible.

# Methodology

The workflow follows a simple, realistic sequence:

* Establish a baseline using security scanning tools
* Apply incremental hardening steps
* Re-scan and compare results
* Document findings with logs, configuration files, and screenshots

This mirrors how system hardening is performed in actual IT environments: measure, change, verify.

# Tools Used

The project relies on common and beginner-friendly tools, such as:

* Lynis for system auditing
* OpenSCAP (optional) for compliance-based scans
* Shell scripts for automating configurations
* UFW or basic iptables/nftables rules depending on the environment

# Repository Structure (High-Level)

* Documentation for each project phase
* Scripts for installation, scanning, and hardening
* Screenshots and logs for transparency and verification
