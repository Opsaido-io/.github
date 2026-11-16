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

https://github.com/user-attachments/assets/bce99300-2833-48f2-afbd-4da837486a0d

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

#### Remote access

- **RDP and SSH in the browser, with nothing to install.** Open a Windows desktop or a Linux shell from the Remote access page, a connector, or a machine's right-click menu.
- **Proxmox VM and container consoles.** The screen of any VM or container in the browser, in its own window, with power (start, shut down, stop), fit to window, Ctrl+Alt+Del, function keys, paste, fullscreen and reconnect. Proxmox's login stays on the server; the browser only receives a one-time ticket for that console.
- **A root shell on a node**, in the page or in its own window, and a **terminal and file browser inside any container**, and a shell in any Kubernetes pod.
- **Built for real sessions.** A floating toolbar (Ctrl+Alt+Del, clipboard, special keys) you can drag anywhere, pop a session out into its own window and resize it, and RDP settings for all connections or for one.
- **Networks you can't reach directly.** Use the built-in remote desktop service (guacd) or your own, and add more of them for other zones such as a DMZ or another site. Tag a service (for example `dmz`) and hosts with that tag use it automatically; a connection can pick its own; an optional fallback to the default; and every service is health-checked, with a dashboard warning if one in use stops answering.
- **Governed like everything else.** Remote access has its own permissions for SSH, RDP and settings, uses the logins you already saved once as credentials, and the session log records which remote desktop service was used.
- **Prefer a desktop client?** Open the connection in the Remote Desktop app with an .rdp file instead.

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

#### IPAM and asset lifecycle

- **IPAM:** every address Opsaido knows about, per subnet: DHCP leases, devices seen on the network, monitored servers and DNS records, with free ranges, conflicts, device history per address and alerts for new devices. It reads, and changes nothing on your DHCP or DNS servers. Scheduled reports by email or chat.
- **Asset lifecycle:** warranties, support contracts, subscriptions and end-of-life dates, with reminders before they lapse.

#### Security posture

- **Baselines on every host.** Linux (Ubuntu, Debian, RHEL family) and Windows Server are checked against built-in CIS-aligned baselines, agentless and read-only over the login Opsaido already has; nothing is installed. Docker hosts and containers are checked against Docker best practice, Kubernetes with kube-bench, and a full OpenSCAP scan runs on request.
- **Your own standard.** Bring your tech spec as Excel, CSV, Word or PDF and it becomes checks that run on top of the baseline; accept a failing check with a reason; download a compliance report in Excel.
- **A score per host and for the fleet**, the most common failures, history per host, and a *security drift* notification when something that passed now fails. Scans repeat every 7 days.
- **Fix it with approval.** "Fix…" on a check shows exactly what will change, waits for you, keeps the old values so it can be rolled back, and scans again straight after.
- **Vulnerabilities ranked by real risk.** Linux packages (checked against OSV.dev), missing Windows security updates and container images (Trivy), ordered by known exploited (CISA), exploit likelihood (EPSS), severity and whether it is exposed to the network. "Patch first" and "patch soon" lists, one-click patching with approval, a PDF per scan and an Excel fleet report.

#### Vault

- **Every stored secret is encrypted.** Each secret has its own AES-256-GCM key, wrapped by a master key kept outside the database, so a stolen database holds nothing usable. If the keys are missing the vault stays sealed rather than inventing new ones, and a passphrase-protected recovery bundle restores it.
- **Credentials and SSH keys, reused.** Save a login once and use it on many connectors. Generate an SSH key pair (the private key never leaves Opsaido), install it on hosts, test it, switch the connectors over and rotate it later.
- **Use the vault you already have.** HashiCorp Vault or OpenBao, Bitwarden Secrets Manager, Infisical, Azure Key Vault, AWS Secrets Manager and 1Password Connect can hold your secrets and variables, referenced by path instead of copied; used in connectors, generated Compose, Terraform and Ansible files and scheduled jobs.
- **Never shown to the AI.** Secrets stay out of the chat: a new token's secret is saved as a credential, not displayed.

#### Recoverability

- **One score for "can we really get it back?"** Every protected thing is graded by proof: no usable backup, backed up, verified (integrity checked), or restore-tested (restored somewhere harmless and shown to work). The score averages them and lists what would raise it.
- **Real restore tests.** Opsaido restores a Proxmox backup as a new, isolated machine with its network cards and passthrough devices removed, watches it boot and then destroys it. It never restores over an existing machine. Databases get the same: a test restore of a verified backup.
- **Covers what you use:** machines (including backups kept outside Proxmox Backup Server), databases, Veeam jobs and Opsaido's own backup.
- **Reports and rehearsal.** A backup report showing what's protected and what isn't, site recovery plan tests, and power-cut protection that shuts everything down in order and starts it back in reverse.
- **Restore wizards** for VMs and containers (as a new machine or over the original), single-item restore of Opsaido's own configuration, and config backups for network gear with what changed between copies.

#### Certificates

- **Request from any authority.** Let's Encrypt or any ACME CA (with DNS validation), Microsoft AD Certificate Services, HashiCorp Vault PKI, EJBCA, DigiCert CertCentral, Sectigo Certificate Manager and AWS Private CA. Opsaido makes the key and the CA signs the request, so the key never leaves Opsaido. Public CAs that validate first stay *pending*, and the assistant shows which domains still need validating.
- **Never miss an expiry.** Every certificate with its expiry date in one list, including ones already installed on your Windows and Linux servers and the ones your reverse proxies serve, so you see them coming.
- **Expiry reminders by email.** Schedule a reminder at the days left you choose (for example 60, 30, 14, 7 and 1). The email carries each certificate's details in the message itself: names, type, who issued it, serial number, expiry date, where it is used and whether it renews by itself. Watch the certificates Opsaido manages, the ones on your servers and the private CA's certificates and CAs. Each certificate is reported once per threshold, a renewed one starts again, it can stay quiet when nothing is due, extra addresses can be added, and Telegram, Slack and Teams get the headline and a link.
- **Renewed and redeployed automatically.** A renewed certificate is pushed again wherever it was deployed.
- **Put it where it's needed.** Push to Windows servers, push to or pull from Azure Key Vault (for App Service or Application Gateway, with automatic renewal), or download as PFX or PEM.

#### Private CA

Run your own certificate authority, separate from the certificates above: an **offline root** and an **online issuing CA**.

- **Two ways to start.** *Build the whole chain here*: Opsaido makes the root and the issuing CA, and the root key is given to you once as a passphrase-protected file and is **not kept**; only the issuing CA stays online, with its key encrypted by the vault. Or *bring your own offline root*: Opsaido makes the issuing CA's key and a signing request, you sign it on your root and upload the result, and Opsaido checks that it is for that key, is a CA, is in date and that the chain holds together.
- **Issues what you need.** Server (TLS) certificates with DNS names and addresses, and client / user certificates, made here (key kept encrypted) or signed from a request a device made itself, whose key never comes to Opsaido. A certificate never outlives its CA.
- **Revoke and publish.** Revoking puts a certificate on the CA's revocation list. The CA certificate and the CRL are published on your public address without sign-in and written into every certificate it issues, and a Trust file puts the CA on the machines that should trust it.
- **Take it away.** Download in PEM, full chain, DER, PKCS#7, key or PFX; downloads with a key are audited. Renew the issuing CA with the root key file when it nears its end.
- **Watched like the rest.** The private CA's certificates and the CAs themselves are covered by the expiry reminders.

#### Topology

- **Your estate drawn from what is really there.** An automatic diagram grouped by site and role, with the problems highlighted.
- **A live map of how systems connect.** Hypervisors, VMs, switches and the services talking to each other, down to the switch port: click a node for its connections, ports and the switch port it sits on.
- **A world map of traffic.** Where connections go, looked up locally so nothing is sent out.
- **A hierarchy view.** Clusters, hosts, VMs and containers as a tree.
- **Part of the same picture.** Every switch port live with speed, VLANs and traffic (any vendor over SNMP, Omada and UniFi), and all your firewalls in one view with live blocked and allowed traffic, so the map and the detail agree.

#### Database backups

- **PostgreSQL, MySQL / MariaDB and SQL Server**, on a schedule or by hand, kept on a folder, an SMB share, NFS or S3 (SQL Server writes its own files on the server). Database passwords are stored encrypted and never shown again.
- **Verified.** Every backup is integrity-checked and recorded, so the history and "last proven restorable" survive restarts.
- **Restore safely.** Restore as a new database, so the original is never touched.
- **Proven by a test restore.** Opsaido restores a verified backup somewhere harmless and shows it works, which counts toward your Recoverability score.
- **Runs as the organisation**, not as the person who set it up, so jobs keep running when people change roles.

#### Documentator

- **Complete documentation as a finished PDF**, written from what is really there, for any server, VM, Proxmox node, firewall, DNS service, domain controller or your whole infrastructure. It explains the findings in plain words.
- **Read-only.** It collects everything in one pass: inside the operating system (Linux over SSH, Windows over WinRM) the identity, hardware, storage, network, roles and features, services, listening ports, users, groups and administrators, shares and permissions, scheduled tasks, firewall and remote-access settings; the VM around it (every setting, disk, adapter, snapshot, HA and firewall); and what Opsaido already knows: installed software, baseline score, vulnerabilities, certificates, pending updates, recent alerts and metrics.
- **Generate whenever you need it**, and push the documentation to a Git repository.
- **Audit-ready.** The finished PDF is something you can hand to an auditor or a new colleague.

#### Software inventory

- **Every app and package on every server**, with the OS and hardware: Linux and Windows, including per-user installs and Microsoft Store apps, refreshed every 12 hours. The container images your Docker hosts run are in the same list.
- **By app:** each app once, how many hosts have it and which versions. Filter by type (apps, packages, Store apps, per-user apps, container images), by OS or by flag, and click an app to see every host and version.
- **By host:** everything installed on a server, with operating systems past or near end of support flagged.
- **Flags that matter:** older versions than the newest in your fleet, vulnerable (from the latest scans) and unwanted software from your own list, with a notification when something new appears on a server.
- **What changed:** what was installed, removed or updated on each server since its last inventory, kept for a year by default.
- **Excel and CSV** of every app with its install count, every install per host, and the hosts: ready for a licence audit.

#### Reporting, delivered to your mailbox

- **Reports for managers and auditors**, as finished PDFs and Excel files:
  - *Security:* a PDF per host and scan with the score, failures by severity and exactly what needs fixing, plus an Excel compliance report against the built-in baselines or your own tech spec.
  - *Vulnerabilities:* a PDF per scan (patch first, patch soon, everything else) and an Excel report of every finding across the fleet.
  - *Backups:* a PDF with the coverage ring, what needs attention, every backup and Proxmox Backup Server job, and each machine's latest backup, with an HTML email carrying the headline numbers and the PDF attached.
  - *Patching:* ask the assistant for a patch report (pending updates across Linux, Windows, Proxmox and containers) and schedule it, for example every Monday.
  - *Documentation, recoverability, IPAM, software and assets:* the Documentator PDFs, the Recoverability report, the new-device and conflict report, and the software and licence exports.
- **Scheduled delivery.** Send any report daily, weekly, monthly or on a cron schedule, to a mailbox, Telegram, Teams and other channels (the IPAM report can be sent only when something is new). The last and next run of every schedule are in one list under Workflows → Jobs, and you can run one now.
- **Set it up in chat**: any request, such as a patch or backup check, can run on a schedule and send you the result.

100+ integrations and 1,000+ things it can do, in plain language. [See them all](https://opsaido.io/integrations.html).

### Get started

Install with Docker in about five minutes: one container, on your own hardware. Every install starts with a **free 30-day trial of every feature**, with no sign-up or payment required.

→ [Getting started](https://opsaido.io/docs/getting-started)

### Safe by design

Reads run freely. Anything that changes a system waits for your approval and shows the exact command first. Every change is recorded and can be rolled back. [How it works](https://opsaido.io/docs/security-model)

### No telemetry

Opsaido doesn't report on you: no usage data, no analytics, no trackers, and never your host names, IP addresses, logs, chats, commands, results or credentials. The only call home is licensing (licence ID, installation ID, version and the *number* of machines), and **offline licences never call home**, for air-gapped and regulated sites. Your questions go only to the AI provider you choose, or nowhere at all with a local model. [What leaves your network](https://opsaido.io/docs/security-model)

### Contact

Questions, ideas or a problem? [hello@opsaido.io](mailto:hello@opsaido.io) · [Support](https://github.com/opsaido-io/.github/blob/main/SUPPORT.md) · [Security](https://github.com/opsaido-io/.github/blob/main/SECURITY.md)
