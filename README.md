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

OPgX is an offline, read-only auditor for PostgreSQL configuration and host-based authentication. It parses postgresql.conf, pg_hba.conf, pg_ident.conf and ALTER SYSTEM overrides, resolving effective settings with correct last-wins and include semantics. Findings are mapped to CIS, CWE and MITRE ATT&CK references.

---

## ✨ Features

- Faithful postgresql.conf parser with units, includes and last-wins semantics
- pg_hba.conf and pg_ident.conf parsing, including PG16 include directives
- Rule engine for TLS, authentication methods, listen addresses and replication exposure
- postgresql.auto.conf override handling and data-directory permission hints
- CIS PostgreSQL Benchmark, CWE and MITRE ATT&CK mapping
- Export formats (json/sarif/md/csv), rule catalogue and hardened template output

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPgX -c /etc/postgresql/16/main/postgresql.conf --hba /etc/postgresql/16/main/pg_hba.conf
./OPgX --scan --root /mnt/collected --json -o report.json
./OPgX -c postgresql.conf --fail-on high
./OPgX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled.s.Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
