<p align="center">
  <a href="https://opsaido.io"><img src="https://raw.githubusercontent.com/opsaido-io/.github/main/profile/banner.png" alt="Opsaido: Your tech, expertly handled." width="100%"></a>
</p>

<h3 align="center">Every system. One conversation. Nothing changes without you.</h3>

<p align="center">
  <a href="https://opsaido.io">Website</a> ·
  <a href="https://opsaido.io/docs">Documentation</a> ·
  <a href="https://opsaido.io/integrations.html">Integrations</a> ·
  <a href="https://opsaido.io/pricing.html">Pricing</a> ·
  <a href="https://opsaido.io/changelog">What's new</a>
</p>

<p align="center"><a href="https://github.com/Opsaido-io/.github/blob/main/profile/opsaido-tour.mp4">▶ Watch the product tour (34 min, every area in the app)</a></p>

**Opsaido** is an operator for your servers, network, apps and smart home. Ask in plain English: it plans the work, shows you a **dry run**, waits for your **approval** and can **roll it back**. It also monitors everything live, and it comes with its own management tools that **work without AI**: use the assistant, or don't, and everything is still managed from one place.

Homelab, small to medium business or enterprise: it scales with you, from one server to thousands.

### What it does

| | |
|---|---|
| **Operate** | Virtualization, containers and Kubernetes, databases, and remote desktop and SSH in the browser. Details below. |
| **Assist** | Ask in plain English, in the web app or your favourite chat app, or by voice. Details below. |
| **Automate** | Scheduled jobs, workflows, quick actions, guided builds, self-healing alerts and patching with a snapshot or backup first. |
| **Secure** | Vulnerability scans ranked by real risk, security baselines, certificate management and an encrypted vault for secrets. |
| **Monitor** | Every host, VM and container live, alerts that escalate, checks, a status page, network topology and central log search. |
| **Recover** | Backups graded by proof: restores are tested for real, for machines and databases. Power-cut protection and config backups for your network gear. |
| **Document and track** | Finished PDF documentation written from what is really there, IP address management, asset lifecycle and software inventory. |

#### Virtualization

- **Proxmox VE, in full.** Clusters, nodes, VMs and containers in one explorer (folder, cluster, storage, network and backup views), read live from Proxmox. Right-click anything for its actions.
  - *Machines:* create VMs (UEFI, TPM for Windows 11, VirtIO, installer ISO) and containers; clone, migrate, snapshot, roll back, back up and restore (as a new machine or over the original); change hardware (CPU, memory and ballooning, disks grow, move, add or detach, CD/DVD, boot order, network adapters with VLAN, firewall and rate limit); history for the last hour to a year; the machine's console in the browser.
  - *Nodes:* performance, disks with health and wear (LVM, LVM-Thin, directories, ZFS), updates, services, DNS and time, firewall, replication, a root shell in the page.
  - *Storage and networks:* add NFS, SMB/CIFS, Proxmox Backup Server, directory, LVM, LVM-Thin or ZFS storage; edit, remove, download an ISO from a URL straight onto it; see which machine uses which storage, VLAN and bridge.
  - *Balance (DRS):* a cluster load overview, balancing recommendations in Manual, Partial or Automatic mode, affinity rules (keep together, keep apart, pin to nodes) and node maintenance mode that moves guests away first.
  - *Governance:* firewall rules at cluster, node and guest level, High Availability, users, groups, roles and API tokens, scheduled backup jobs (and the guests no job covers), and drift tracking of every configuration change, including ones made outside Opsaido.
- **Proxmox Backup Server and Veeam.** Backups, jobs, verify, garbage collection, prune by retention (dry run first), protected snapshots, sync jobs, and Veeam restore points.
- **VMware, Hyper-V, XCP-ng and KVM** in the same explorer: power actions, hardware, snapshots and history; on vCenter also move a VM, maintenance mode, and add or grow disks and network adapters.
- **Wizards for the big jobs:** backup, restore, clone, migrate, create VM, export and import, templates (deploy, convert to and from a template), and scheduled maintenance (backup, snapshot, and snapshot or backup clean-up with a storage fit check).
- **Patching wizard** for Proxmox and VMware hosts, Hyper-V, Linux and Windows servers, Kubernetes nodes and Docker hosts: it moves VMs away, patches, reboots, checks health and puts everything back, one host at a time.

#### Containers

- **Docker hosts and Compose stacks** in one explorer. Per container: live CPU, memory, network and disk, logs (filter, follow, download), a terminal and a file browser inside the container, processes, configuration, ports, volumes and networks.
  - *Stacks:* edit the compose file and `.env` in the app, validate, deploy, pull from or push to Git, start a new stack from a repository; files on the host, Portainer or Dockhand.
  - *Updates:* check the registry for a newer image and update with rollback if the new one doesn't start.
  - *Security:* 13 hardening checks with the fix for each, image vulnerability scans (Trivy), and "fix with the assistant" with approval.
  - *Housekeeping:* start, stop, restart, pause, kill, remove, and clean up unused images, containers, volumes and networks.
- **Podman**, the same management: rootless or rootful, pods, Quadlets, Kubernetes YAML, secrets and auto-update.
- **Kubernetes and k3s:** nodes, namespaces, workloads, pods, services, ingresses, config and storage. Logs, a shell in any pod, scale, rolling restart, roll back, cordon and drain, run a CronJob now, edit and apply YAML, warnings, security checks and image scans.
- **Databases:** backup, restore and test restore.

#### The assistant

- **Ask in plain English** and get answers from live data across everything you've connected: servers, VMs, containers, networks, firewalls, storage, backups, cloud and smart home. 1,000+ things it can do, across 100+ integrations.
- **Plan and change, safely.** Anything that changes a system shows the exact command or API call first and waits for your approval. Ask for a **dry run** to rehearse a whole job, then say "go ahead" to approve the plan once. Second approvals for risky actions. Every change is recorded and can be rolled back, one change or a whole job.
- **Diagnose.** Find the cause of an alert, correlate hosts, logs and recent changes, and fix it with approval. Alerts can start a fix on their own (self-heal) within the limits you set.
- **Make things.** Compose files, Traefik rules, scripts, Excel, CSV and PDF reports, and step-by-step builds such as a new Active Directory domain, VMs from a template or a private AI server.
- **Your choice of AI.** A cloud model (Anthropic Claude, OpenAI) or a local one (Ollama, LM Studio, any OpenAI-compatible server), or no AI at all: everything also has its own screen. Credentials are encrypted and never sent to the AI.
- **It remembers the conversation**, and "Ask the assistant" buttons on every page start a chat about what you're looking at.

#### Chat apps and voice

- Talk to the assistant from **Telegram, Slack, Microsoft Teams, Discord, Matrix or WhatsApp**, linked to your account with a one-time code. Approvers can decide straight from Telegram.
- Alerts, approval requests and failed actions go to email, Telegram, Slack, Discord or any webhook, and you choose which events go where.
- **Voice:** a microphone button in chat, spoken answers, Home Assistant voice satellites and phones, and a voice PIN to approve changes. Speech can be local (Whisper, Kokoro) or a cloud service.

#### Scheduling, workflows and quick actions

- **Scheduled jobs:** run any request daily, weekly, monthly or on a cron schedule, and get the result by email, Telegram or Teams. One list for every kind of job, with its last and next run.
- **Workflows and templates** for repeatable work, and **guided builds** with sensible defaults.
- **Quick actions:** save a request as a one-click button with keyboard shortcuts 1 to 9, and share it with your team.
- **Self-heal:** alerts can start a fix on their own, within the limits you set.

#### IPAM, assets and software inventory

- **IPAM:** every address Opsaido knows about, per subnet: DHCP leases, devices seen on the network, monitored servers and DNS records, with free ranges, conflicts, device history per address and alerts for new devices. It reads, and changes nothing on your DHCP or DNS servers. Scheduled reports by email or chat.
- **Asset lifecycle:** warranties, support contracts, subscriptions and end-of-life dates, with reminders before they lapse.
- **Software inventory:** every app and package on your Linux and Windows servers, per-user and Store apps included, plus the container images your Docker hosts run. See each app once with the hosts and versions, what changed since last time, which versions are old, vulnerable or unwanted, and export to Excel or CSV for a licence audit.

100+ integrations and 1,000+ things it can do, in plain language. [See them all](https://opsaido.io/integrations.html).

### Get started

Install with Docker in about five minutes: one container, on your own hardware. Every install starts with a **free 30-day trial of every feature**, with no sign-up or payment required.

→ [Getting started](https://opsaido.io/docs/getting-started)

### Safe by design

Reads run freely. Anything that changes a system waits for your approval and shows the exact command first. Every change is recorded and can be rolled back. [How it works](https://opsaido.io/docs/security-model)

### Contact

Questions, ideas or a problem? [hello@opsaido.io](mailto:hello@opsaido.io) · [Support](https://github.com/opsaido-io/.github/blob/main/SUPPORT.md) · [Security](https://github.com/opsaido-io/.github/blob/main/SECURITY.md)
