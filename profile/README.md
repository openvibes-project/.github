<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/openvibes-project/openvibes-agent/main/docs/brand/openvibes-wordmark-dark.svg">
    <img src="https://raw.githubusercontent.com/openvibes-project/openvibes-agent/main/docs/brand/openvibes-wordmark-light.svg" alt="OpenVIBES" width="520">
  </picture>
</p>

<p align="center">
  <b>Open Vulnerability Inspection &amp; Baseline Evaluation System</b><br>
  A free, open-source, lightweight security tool for homelabs, small businesses and security enthusiasts.
</p>

<p align="center">
  <img alt="License: Apache 2.0" src="https://img.shields.io/badge/license-Apache%202.0-blue">
  <img alt="Written in Rust" src="https://img.shields.io/badge/written%20in-Rust-orange">
  <img alt="Self-hosted" src="https://img.shields.io/badge/self--hosted-no%20telemetry-green">
  <img alt="Status" src="https://img.shields.io/badge/status-early%20release%200.2.9-yellow">
</p>

---

> **AI disclosure:** OpenVIBES is built with the help of AI coding tools
> (Claude Code and Codex), and they will continue to be used. Every change
> still goes through a pull request and the full CI checks before it is
> merged. Each repository's `CONTRIBUTING.md` has the policy.

### What it does

A small, **read-only agent** on every host collects facts (packages, processes,
listening ports and services, hardening settings, operating system), evaluates
**signed rules** against them, raises **threat alarms** from program starts
(eBPF, kernel audit as the fallback) and reports over **mutual TLS 1.3**. The
**platform** enrolls agents, hands out rules, matches every host's packages
against security advisories and tells you **which hosts to patch first**, in
one fast web console with an optional AI assistant that runs on your own
platform. A keyboard-only admin menu on the platform host installs, updates,
backs up and repairs it.

**Where it stands:** release 0.2.9 is out (platform on Fedora 44; agents on
Fedora, AlmaLinux, Rocky, Debian, Ubuntu and Arch). Coming in 0.3: a rebuilt
admin menu, roles and permissions with host groups, Linux hardening checks
per host group, and new list and detail pages. Try the
[live demo](https://openvibes-project.github.io/openvibes-platform/) or
[get started](https://openvibes-project.github.io/).

### Why

| | |
|---|---|
| 🧭 **Interface first** | Fast, uncluttered screens that answer a question quickly. |
| 🪶 **Light agents** | A small Rust agent with a measured footprint budget. |
| 🛠️ **Customisable** | Your own rules, collectors, severities and views. |
| 🔕 **Quiet by default** | Alerts on what matters; everything else is tunable. |
| 🔒 **Secure by default** | mTLS everywhere, built-in CA, offline-signed rules, and it never changes your hosts. |
| 🏠 **Yours** | Self-hosted, no vendor cloud, no telemetry, no licence locks. Air-gapped hosts work too. |

### Repositories

| Repository | What it is |
|---|---|
| [**openvibes-agent**](https://github.com/openvibes-project/openvibes-agent) | The endpoint agent for Linux, Windows and macOS: collectors, signed-rule evaluation, a durable local queue, the mTLS client. |
| [**openvibes-platform**](https://github.com/openvibes-project/openvibes-platform) | The server side: ingest, rule distribution, vulnerability matching, the admin menu and CLI, built-in PKI, packaging, and the web console with its AI assistant. |
| [**openvibes-protocol**](https://github.com/openvibes-project/openvibes-protocol) | The contract between the two: spec, JSON Schemas and shared fixtures. Every change crossing the boundary lands here first. |
| [**openvibes-rules**](https://github.com/openvibes-project/openvibes-rules) | The project's signed rule sets: baseline, threat alarms and Linux hardening level 1. |
| [**openvibes-project.github.io**](https://github.com/openvibes-project/openvibes-project.github.io) | The website, the signed package repositories (RPM, apt, pacman) and `install.sh`. |

```
  host: openvibes-agent                         openvibes-platform
    collectors -> facts                           ingest        enroll, heartbeat,
    signed rules -> evaluate   --- mTLS 1.3 -->                 findings, alarms, inventory
    local queue -> send        <-- mTLS 1.3 ---  distribution  signed rule bundles
```

### Get involved

OpenVIBES is an early release, moving fast. Issues, ideas and pull requests are welcome;
start with the `CONTRIBUTING.md` in the repository you want to work on
(it asks you to disclose AI assistance). Found a security problem? Please use
**private vulnerability reporting** in the affected repository, not a public issue.
