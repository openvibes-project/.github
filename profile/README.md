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
  <img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-blue">
  <img alt="Written in Rust" src="https://img.shields.io/badge/written%20in-Rust-orange">
  <img alt="Self-hosted" src="https://img.shields.io/badge/self--hosted-no%20telemetry-green">
  <img alt="Status" src="https://img.shields.io/badge/status-early%20development-yellow">
</p>

---

### What it does

A small, **read-only agent** on every host collects facts (packages, processes,
listening ports, operating system), evaluates **signed audit rules** against them
and reports over **mutual TLS 1.3**. The **platform** enrolls agents, hands out
rules, matches every host's packages against security advisories and tells you
**which hosts to patch first**.

### Why

| | |
|---|---|
| 🧭 **Interface first** | Fast, uncluttered screens that answer a question quickly. |
| 🪶 **Light agents** | About 17 MB of memory and a fraction of a second of CPU per scan. |
| 🛠️ **Customisable** | Your own rules, collectors, severities and views. |
| 🔕 **Quiet by default** | Alerts on what matters; everything else is tunable. |
| 🔒 **Secure by default** | mTLS everywhere, built-in CA, offline-signed rules, and it never changes your hosts. |
| 🏠 **Yours** | Self-hosted, no vendor cloud, no telemetry, no licence locks. Air-gapped hosts work too. |

### Repositories

| Repository | What it is |
|---|---|
| [**openvibes-agent**](https://github.com/openvibes-project/openvibes-agent) | The endpoint agent for Linux, Windows and macOS: collectors, signed-rule evaluation, a durable local queue, the mTLS client. |
| [**openvibes-platform**](https://github.com/openvibes-project/openvibes-platform) | The server side: ingest, rule distribution, vulnerability matching, admin tools, built-in PKI, packaging and the web console. |
| [**openvibes-protocol**](https://github.com/openvibes-project/openvibes-protocol) | The contract between the two: spec, JSON Schemas and shared fixtures. Every change crossing the boundary lands here first. |

```
  host: openvibes-agent                         openvibes-platform
    collectors -> facts                           ingest        enroll, heartbeat,
    signed rules -> evaluate   --- mTLS 1.3 -->                 findings, inventory
    local queue -> send        <-- mTLS 1.3 ---  distribution  signed rule bundles
```

### Get involved

OpenVIBES is in early development. Issues, ideas and pull requests are welcome;
start with the `CONTRIBUTING.md` in the repository you want to work on
(it asks you to disclose AI assistance). Found a security problem? Please use
**private vulnerability reporting** in the affected repository, not a public issue.
