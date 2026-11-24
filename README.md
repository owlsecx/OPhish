# 🦉 OPhish

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OReconnaissance-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OPhish** — Analyses URLs, SMS and email content to detect phishing, domain reputation and brand impersonation

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OPhish is a detection engine for phishing, smishing, QRishing and email-based threats. It analyses individual URLs, bulk URL lists, SMS messages, .eml emails and QR-code images, scoring them with heuristic analysis and optional threat-intelligence APIs. Results can be exported as JSON, TXT or HTML.

---

## ✨ Features

- Analyses single URLs, bulk URL files, SMS messages, .eml emails and QR images
- Heuristic risk scoring with typosquatting, IDN/punycode homoglyph and entropy analysis
- Optional VirusTotal, Google Safe Browsing and AbuseIPDB integrations with graceful fallback
- Async/threaded bulk scanning with a configurable thread count and minimum-score filter
- STDIN pipeline mode and a fast offline mode that skips network checks
- CSV/JSON/HTML export and an offline self-test

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPhish -u https://example.com
./OPhish -f urls.txt --threads 10 --min-score 50
./OPhish -e message.eml -o report.html
./OPhish --help
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
sudo strace -f -e trace=network ./OPhish --help   # watch every network call
firejail --net=none ./OPhish --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
