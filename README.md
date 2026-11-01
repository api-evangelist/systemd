# systemd

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

systemd is a suite of basic building blocks for a Linux system. It runs as PID 1 and is the system and service manager that bootstraps the rest of the userspace, supervises long-running services, and exposes a coordinated set of D-Bus and Varlink IPC interfaces for managing services (systemd1), users and sessions (logind), network interfaces (networkd), name resolution (resolved), containers/VMs (machined), home directories (homed), boot entries (boot1/sysupdate1), system hostname/locale/timedate, OOM protection (oomd), portable services, and image imports. The project also publishes a stable command-line surface (systemctl, journalctl, networkctl, resolvectl, loginctl, machinectl, hostnamectl, timedatectl, localectl, busctl, varlinkctl, bootctl, homectl, coredumpctl, oomctl, portablectl, importctl, systemd-analyze and more). systemd is dual-licensed (LGPL-2.1-or-later for libraries and most code, GPL-2.0-or-later for select tools) and developed openly on GitHub at systemd/systemd.

**Areas:** Boot · Cgroups · Containers · D-Bus · Init · IPC · Journals · Linux · Logging · Networks · Open Source · PID 1

## systemd on APIs.io

Everything profiled for systemd is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/systemd/](https://apis.io/providers/systemd/)** — or go straight to one of the APIs or properties below.

### APIs (34)

- [systemd-localed (org.freedesktop.locale1)](https://apis.io/apis/systemd/org-freedesktop-locale1/) — D-Bus API of systemd-localed for getting and setting the system locale, X11 keymap, and console keymap.
- [systemd-timedated (org.freedesktop.timedate1)](https://apis.io/apis/systemd/org-freedesktop-timedate1/) — D-Bus API of systemd-timedated for getting and setting the system time, timezone, NTP enablement, and RTC-in-local-time policy.
- [systemd-timesyncd (org.freedesktop.timesync1)](https://apis.io/apis/systemd/org-freedesktop-timesync1/) — D-Bus API of systemd-timesyncd exposing the current NTP server, peers, root delay/dispersion, and synchronization status.
- [systemd-homed (org.freedesktop.home1)](https://apis.io/apis/systemd/org-freedesktop-home1/) — D-Bus API of systemd-homed for managing portable, encrypted user home directories (LUKS, btrfs subvol, fscrypt, CIFS, directory) including…
- [systemd-importd (org.freedesktop.import1)](https://apis.io/apis/systemd/org-freedesktop-import1/) — D-Bus API of systemd-importd for importing, exporting, downloading, listing, and removing container/VM machine images (tar, raw, dkr/OCI, qcow2) used by…
- [systemd-oomd (org.freedesktop.oom1)](https://apis.io/apis/systemd/org-freedesktop-oom1/) — D-Bus API of systemd-oomd, the userspace out-of-memory killer that uses cgroup v2 PSI signals to kill cgroups under memory or swap pressure. Exposes…
- [systemd-portabled (org.freedesktop.portable1)](https://apis.io/apis/systemd/org-freedesktop-portable1/) — D-Bus API of systemd-portabled for attaching/detaching portable service images, listing attached images, inspecting them, and managing their lifecycle on…
- [systemd-sysupdated (org.freedesktop.sysupdate1)](https://apis.io/apis/systemd/org-freedesktop-sysupdate1/) — D-Bus API of systemd-sysupdated for transactional A/B updates of system/host/portable/container images using systemd-sysupdate transfers, including target…
- [LogControl1 (org.freedesktop.LogControl1)](https://apis.io/apis/systemd/org-freedesktop-logcontrol1/) — Generic D-Bus interface that systemd daemons (and other services) implement to expose runtime log level and log target configuration. Allows tools like…
- [systemd Boot API](https://apis.io/apis/systemd/systemd-boot-api/) — The Boot API from systemd — 1 operation(s) for boot.
- [systemd Cache API](https://apis.io/apis/systemd/systemd-cache-api/) — The Cache API from systemd — 2 operation(s) for cache.
- [systemd Cgroups API](https://apis.io/apis/systemd/systemd-cgroups-api/) — Transient unit creation and cgroup-backed resource control.
- [systemd Configuration API](https://apis.io/apis/systemd/systemd-configuration-api/) — The Configuration API from systemd — 11 operation(s) for configuration.
- [systemd Credentials API](https://apis.io/apis/systemd/systemd-credentials-api/) — The Credentials API from systemd — 2 operation(s) for credentials.
- [systemd Hostname API](https://apis.io/apis/systemd/systemd-hostname-api/) — The Hostname API from systemd — 3 operation(s) for hostname.
- [systemd Image API](https://apis.io/apis/systemd/systemd-image-api/) — The Image API from systemd — 1 operation(s) for image.
- [systemd Images API](https://apis.io/apis/systemd/systemd-images-api/) — The Images API from systemd — 4 operation(s) for images.
- [systemd Inhibitors API](https://apis.io/apis/systemd/systemd-inhibitors-api/) — The Inhibitors API from systemd — 1 operation(s) for inhibitors.
- [systemd Jobs API](https://apis.io/apis/systemd/systemd-jobs-api/) — Pending and active jobs scheduled by the Manager.
- [systemd Links API](https://apis.io/apis/systemd/systemd-links-api/) — The Links API from systemd — 7 operation(s) for links.
- [systemd Machine Info API](https://apis.io/apis/systemd/systemd-machine-info-api/) — The Machine Info API from systemd — 4 operation(s) for machine info.
- [systemd Machines API](https://apis.io/apis/systemd/systemd-machines-api/) — The Machines API from systemd — 7 operation(s) for machines.
- [systemd Manager API](https://apis.io/apis/systemd/systemd-manager-api/) — The Manager API from systemd — 12 operation(s) for manager.
- [systemd PCR API](https://apis.io/apis/systemd/systemd-pcr-api/) — The PCR API from systemd — 1 operation(s) for pcr.
- [systemd Power API](https://apis.io/apis/systemd/systemd-power-api/) — The Power API from systemd — 5 operation(s) for power.
- [systemd Resolution API](https://apis.io/apis/systemd/systemd-resolution-api/) — The Resolution API from systemd — 4 operation(s) for resolution.
- [systemd Resolve API](https://apis.io/apis/systemd/systemd-resolve-api/) — The Resolve API from systemd — 1 operation(s) for resolve.
- [systemd Seats API](https://apis.io/apis/systemd/systemd-seats-api/) — The Seats API from systemd — 1 operation(s) for seats.
- [systemd Sessions API](https://apis.io/apis/systemd/systemd-sessions-api/) — The Sessions API from systemd — 5 operation(s) for sessions.
- [systemd Snapshots API](https://apis.io/apis/systemd/systemd-snapshots-api/) — System state introspection.
- [systemd Unit API](https://apis.io/apis/systemd/systemd-unit-api/) — The Unit API from systemd — 2 operation(s) for unit.
- [systemd Units API](https://apis.io/apis/systemd/systemd-units-api/) — Unit lifecycle and enumeration.
- [systemd UserDatabase API](https://apis.io/apis/systemd/systemd-userdatabase-api/) — The UserDatabase API from systemd — 3 operation(s) for userdatabase.
- [systemd Users API](https://apis.io/apis/systemd/systemd-users-api/) — The Users API from systemd — 3 operation(s) for users.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Systemd Agentic Access](https://apis.io/agentic-access/systemd/systemd-agentic-access/)

#### JSON Schema (6)

The data models the API reads and writes.

- [logind Session](https://apis.io/schemas/systemd/login1-session/)
- [machined Machine](https://apis.io/schemas/systemd/machine1-machine/)
- [networkd Link](https://apis.io/schemas/systemd/network1-link/)
- [systemd Job](https://apis.io/schemas/systemd/systemd1-job/)
- [systemd Unit](https://apis.io/schemas/systemd/systemd1-unit/)
- [systemd JSON User Record (partial)](https://apis.io/schemas/systemd/varlink-user-record/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Systemd Structure](https://apis.io/json-structure/systemd/systemd-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Systemd Context](https://apis.io/jsonld/systemd/systemd-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [systemd Vocabulary](https://apis.io/vocabularies/systemd/systemd-vocabulary/)

#### Examples (10)

Example requests and responses.

- [Login1 Inhibit Example](https://apis.io/examples/systemd/login1-inhibit-example/)
- [Login1 Listsessions Example](https://apis.io/examples/systemd/login1-listsessions-example/)
- [Machine1 Listmachines Example](https://apis.io/examples/systemd/machine1-listmachines-example/)
- [Network1 Listlinks Example](https://apis.io/examples/systemd/network1-listlinks-example/)
- [Resolve1 Resolvehostname Example](https://apis.io/examples/systemd/resolve1-resolvehostname-example/)
- [Systemd1 Listunits Example](https://apis.io/examples/systemd/systemd1-listunits-example/)
- [Systemd1 Starttransient Example](https://apis.io/examples/systemd/systemd1-starttransient-example/)
- [Systemd1 Startunit Example](https://apis.io/examples/systemd/systemd1-startunit-example/)
- [Varlink Credentials Encrypt Example](https://apis.io/examples/systemd/varlink-credentials-encrypt-example/)
- [Varlink Userdb Getuser Example](https://apis.io/examples/systemd/varlink-userdb-getuser-example/)

#### Collections (32)

Postman and Open Collection request collections.

- [systemd-hostnamed (org.freedesktop.hostname1)](https://apis.io/collections/systemd/open-hostname1/)
- [systemd-logind (org.freedesktop.login1)](https://apis.io/collections/systemd/open-login1/)
- [systemd-machined (org.freedesktop.machine1)](https://apis.io/collections/systemd/open-machine1/)
- [systemd-networkd (org.freedesktop.network1)](https://apis.io/collections/systemd/open-network1/)
- [systemd-resolved (org.freedesktop.resolve1)](https://apis.io/collections/systemd/open-resolve1/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot API](https://apis.io/collections/systemd/open-systemd-boot-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Cache API](https://apis.io/collections/systemd/open-systemd-cache-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Cgroups API](https://apis.io/collections/systemd/open-systemd-cgroups-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Configuration API](https://apis.io/collections/systemd/open-systemd-configuration-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Credentials API](https://apis.io/collections/systemd/open-systemd-credentials-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Hostname API](https://apis.io/collections/systemd/open-systemd-hostname-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Image API](https://apis.io/collections/systemd/open-systemd-image-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Images API](https://apis.io/collections/systemd/open-systemd-images-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Inhibitors API](https://apis.io/collections/systemd/open-systemd-inhibitors-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Jobs API](https://apis.io/collections/systemd/open-systemd-jobs-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Links API](https://apis.io/collections/systemd/open-systemd-links-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Machine Info API](https://apis.io/collections/systemd/open-systemd-machine-info-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Machines API](https://apis.io/collections/systemd/open-systemd-machines-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Manager API](https://apis.io/collections/systemd/open-systemd-manager-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot PCR API](https://apis.io/collections/systemd/open-systemd-pcr-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Power API](https://apis.io/collections/systemd/open-systemd-power-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Resolution API](https://apis.io/collections/systemd/open-systemd-resolution-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Resolve API](https://apis.io/collections/systemd/open-systemd-resolve-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Seats API](https://apis.io/collections/systemd/open-systemd-seats-api/)
- [systemd-hostnamed (org.freedesktop.hostname1) Boot Sessions API](https://apis.io/collections/systemd/open-systemd-sessions-api/)
- …and 7 more published on APIs.io

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [systemd — jsonschema rules](https://apis.io/rules/systemd/systemd-jsonschema-spectral-rules/)
- [systemd API Rules](https://apis.io/rules/systemd/systemd-rules/)

#### Security (1)

Authentication, trust centre, and vulnerability disclosure.

- [Systemd Domain Security](https://apis.io/security/systemd/systemd-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://systemd.io)
- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/)
- [Changelog](https://github.com/systemd/systemd/blob/main/NEWS)
- [GitHub](https://github.com/systemd)

## API Evangelist rating

**Kin Score 30.2** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 45.0 |
| Contract governance | 27.3 |
| Operational transparency | 18.4 |
| Developer ergonomics | 21.4 |
| Access clarity | 0.0 |

**Agent readiness 16.5** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | — |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 10.8** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/systemd/](https://apis.io/providers/systemd/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for systemd: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/systemd/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
