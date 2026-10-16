# 🦉 OPgX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OPgX** — Offline PostgreSQL Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline PostgreSQL configuration & pg_hba auditor

---

## ✨ Features

- Faithful postgresql.conf grammar — `name = value`, quoted values with '' escapes, units, include, include_if_exists, include_dir, last-wins semantics
- postgresql.auto.conf (ALTER SYSTEM) override layer
- pg_hba.conf parser — quoted tokens, @file lists, CIDR + netmask, hostssl/hostnossl/hostgssenc, options, line continuation, PG16 include directives
- pg_ident.conf parser — regex & wildcard mappings
- Rule engine: listen_addresses vs TLS, ssl off, weak ssl_min_protocol_version / ciphers, md5 password_encryption, trust/password/md5 remote, 0.0.0.0/0 & ::/0, replication without scram+hostssl, local trust, shadowed rules, logging & pgAudit gaps
- Data directory / key / config permission hints
- CIS PostgreSQL Benchmark + CWE + MITRE ATT&CK map
- Weighted A+…F grade, severity filters, --fail-on
- Exports TXT / MD / JSON / CSV / SARIF 2.1.0
- Offline --root mode for mounted images / backups
- Built-in self-test demo (exit 3 on missed rule)

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPgX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
