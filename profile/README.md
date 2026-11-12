<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/openvibes-project/openvibes-agent/main/docs/brand/openvibes-wordmark-dark.svg">
    <img src="https://raw.githubusercontent.com/openvibes-project/openvibes-agent/main/docs/brand/openvibes-wordmark-light.svg" alt="OpenVIBES" width="520">
  </picture>
</p>

<p align="center">
  <b>Open Vulnerability Inspection &amp; Baseline Evaluation System</b><br>
  A free, open-source security tool for homelabs, small businesses and security enthusiasts.
</p>

<p align="center">
  <a href="https://openvibes-project.github.io/openvibes-platform/">Live demo</a> ·
  <a href="https://openvibes-project.github.io/">Install</a> ·
  <a href="https://github.com/openvibes-project/openvibes-platform/releases/latest">Latest release</a>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/openvibes-project/openvibes-platform/main/docs/images/console-dashboard-dark.png">
    <img src="https://raw.githubusercontent.com/openvibes-project/openvibes-platform/main/docs/images/console-dashboard-light.png" alt="The OpenVIBES console's dashboard, with demo data" width="900">
  </picture>
</p>

### What it is

You put a small agent on each of your hosts and run the platform on one
server of your own. The agents look at what is installed, what runs and
what listens, and report to the platform. The platform's web console then
tells you:

- **which vulnerabilities to patch first,** across all your hosts;
- **where a host is weakly set up,** from hardening and compliance checks;
- **when something suspicious runs,** as a threat alarm within seconds.

The platform runs on Fedora 44. Agents run on Fedora,
AlmaLinux, Rocky Linux, Debian, Ubuntu and Arch, and on Windows as a preview.

### Why

| | |
|---|---|
| 🧭 **Interface first** | Fast, uncluttered screens that answer a question quickly. |
| 🪶 **Light** | A small Rust agent with a measured footprint; the platform runs in 2 GB of RAM. |
| 🛠️ **Yours to shape** | Your own rules, host groups, roles, dashboards and views. |
| 🔕 **Quiet** | Alerts on what matters; everything else is tunable. |
| 🔒 **Secure by default** | Mutual TLS everywhere, a built-in CA, offline-signed rules, and it never changes your hosts. |
| 🏠 **Self-hosted** | No vendor cloud, no telemetry, no licence locks. Works without internet. |

### Repositories

| Repository | What it is |
|---|---|
| [**openvibes-platform**](https://github.com/openvibes-project/openvibes-platform) | The server: collects what agents find, matches vulnerabilities, the web console and the admin tool. |
| [**openvibes-agent**](https://github.com/openvibes-project/openvibes-agent) | The read-only agent for Linux and Windows. |
| [**openvibes-rules**](https://github.com/openvibes-project/openvibes-rules) | The signed rule sets every agent runs: baseline, threat alarms, Linux hardening. |
| [**openvibes-protocol**](https://github.com/openvibes-project/openvibes-protocol) | The contract between agent and platform. |
| [**openvibes-project.github.io**](https://github.com/openvibes-project/openvibes-project.github.io) | The website, the installer and the signed package repositories. |

### Get involved

OpenVIBES is young and moving fast. Issues, ideas and pull requests are
welcome; start with the `CONTRIBUTING.md` of the repository you want to work
on. Found a security problem? Please use **private vulnerability reporting**
in that repository, not a public issue.

**AI disclosure:** OpenVIBES is built with the help of AI coding tools
(Claude Code and Codex). Every change goes through a pull request and the
full CI before it is merged.
