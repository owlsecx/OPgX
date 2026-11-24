# 🦉 OPgX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
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

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OPgX --help   # watch every network call
firejail --net=none ./OPgX --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
