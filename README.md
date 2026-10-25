# 🦉 OPamAudit

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCore-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OPamAudit** — Offline Linux PAM Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OPamAudit is an offline, read-only Linux PAM configuration auditor. It parses pam.d/pam.conf stacks, resolves includes, simulates fail-open auth bypass, and audits companion files (pwquality, faillock, login.defs, sssd, ldap). Findings map to CIS Linux and NIST SP 800-53 with CWE/MITRE mapping and multi-format export.

---

## ✨ Features

- Tolerant pam.d / pam.conf parser with continuations, optional types, bracketed controls, and include/substack resolution
- PAM state-machine simulator proving fail-open / authentication-bypass stacks
- 65+ rules: nullok, pam_permit/deny placement, weak hashing, faillock/tally2, pwquality/cracklib, pwhistory, pam_env, pam_exec
- Companion parsers for login.defs, pwquality.conf, faillock.conf, pwhistory, securetty, sssd, nslcd, ldap.conf
- Offline `--root` mode for collected filesystem trees; CIS & NIST mapping per finding
- Score/grade, TXT/MD/JSON/CSV/SARIF export, `--demo` self-test, and CI fail-on gates

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPamAudit --scan
./OPamAudit --root ./fs --service sshd --simulate sshd --json -o pam.json
./OPamAudit --demo --fail-on high
./OPamAudit --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
