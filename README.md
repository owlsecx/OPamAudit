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

Offline Linux PAM configuration auditor (pam.d, pwquality, faillock, login.defs)

---

## ✨ Features

- Tolerant pam.d / pam.conf parser — line continuations, comments, '-' optional types, bracketed [value=action ...] controls, bracketed module arguments, legacy /etc/pam.conf format
- Include resolver — include / substack / @include with loop detection and missing-target reporting
- PAM state-machine simulator — evaluates auth and account stacks under "all credentials fail" to prove fail-open / authentication-bypass stacks
- 65+ audit rules — nullok, pam_permit/pam_deny placement, weak hashing, faillock / tally2, pwquality / cracklib, pwhistory / remember, pam_env user_readenv, pam_exec / pam_python, LDAP / SSSD TLS, pam_wheel, debug leakage, services skipping common-* includes, rogue modules
- Companion parsers — login.defs, pwquality.conf (+ .d), faillock.conf, pwhistory.conf, securetty, sssd.conf, nslcd.conf, ldap.conf, pam_env.conf
- CIS Linux Benchmark & NIST SP 800-53 mapping, CWE + MITRE ATT&CK per finding
- Offline --root mode for collected filesystem trees
- Score / grade, TXT / MD / JSON / CSV / SARIF export
- --demo self-test with synthetic vulnerable tree
- Rich interactive menu + full CLI (CI gating)

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPamAudit
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
