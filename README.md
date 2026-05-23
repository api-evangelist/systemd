# systemd

API and integration profile for **systemd**, the Linux init system, service manager, and the
freedesktop.org suite of system daemons that ship under the same project umbrella (logind,
networkd, resolved, machined, homed, hostnamed, oomd, sysupdated, portabled, importd, ...).

- Project: [systemd.io](https://systemd.io)
- GitHub: [github.com/systemd/systemd](https://github.com/systemd/systemd) (GPL-2.0 / LGPL-2.1)
- Latest stable: **v260.1** (released 2026-03-23)
- License: dual — LGPL-2.1-or-later (libraries and most code) and GPL-2.0-or-later (selected tools)
- Discussion: [systemd-devel mailing list](https://lists.freedesktop.org/mailman/listinfo/systemd-devel)

## What's documented

This repository catalogs the **IPC surface** of systemd — the D-Bus and Varlink interfaces that
applications, container runtimes, control planes, and admin tools use to drive the init system and
its sister daemons.

### D-Bus interfaces (15)

All exposed on the **system** bus. Object paths live under `/org/freedesktop/{interface}/`.

| Interface | Daemon | Purpose |
|---|---|---|
| `org.freedesktop.systemd1` | PID 1 (systemd) | Unit lifecycle, jobs, config reload, transient units |
| `org.freedesktop.login1` | systemd-logind | Sessions, users, seats, inhibitors, power |
| `org.freedesktop.network1` | systemd-networkd | Link enumeration and reconfiguration |
| `org.freedesktop.resolve1` | systemd-resolved | DNS/mDNS/LLMNR resolution, DNSSEC, per-link DNS |
| `org.freedesktop.machine1` | systemd-machined | Containers, VMs, machine images |
| `org.freedesktop.hostname1` | systemd-hostnamed | Hostname, chassis, deployment, location |
| `org.freedesktop.locale1` | systemd-localed | System locale and keymap |
| `org.freedesktop.timedate1` | systemd-timedated | Time, timezone, NTP enablement |
| `org.freedesktop.timesync1` | systemd-timesyncd | SNTP sync state |
| `org.freedesktop.home1` | systemd-homed | Portable encrypted home directories |
| `org.freedesktop.import1` | systemd-importd | Container/VM image import/export |
| `org.freedesktop.oom1` | systemd-oomd | Userspace OOM killer (PSI-driven) |
| `org.freedesktop.portable1` | systemd-portabled | Portable services |
| `org.freedesktop.sysupdate1` | systemd-sysupdated | Transactional A/B image updates |
| `org.freedesktop.LogControl1` | (multiple) | Runtime log level / target control |

### Varlink interfaces (~39, `io.systemd.*`)

The modern, JSON-line IPC surface (single FD, self-describing via `org.varlink.service`). Exposed
through AF_UNIX sockets typically under `/run/systemd/io.systemd.*`. Inspect with
[`varlinkctl`](https://www.freedesktop.org/software/systemd/man/latest/varlinkctl.html).

`io.systemd.Manager`, `io.systemd.Unit`, `io.systemd.Job`, `io.systemd.Login`, `io.systemd.Machine`,
`io.systemd.MachineImage`, `io.systemd.MachineInstance`, `io.systemd.VirtualMachineInstance`,
`io.systemd.Network`, `io.systemd.Network.Link`, `io.systemd.Resolve`, `io.systemd.Resolve.Hook`,
`io.systemd.Resolve.Monitor`, `io.systemd.Journal`, `io.systemd.JournalAccess`,
`io.systemd.Hostname`, `io.systemd.BootControl`, `io.systemd.Credentials`,
`io.systemd.FactoryReset`, `io.systemd.Import`, `io.systemd.InstanceMetadata`,
`io.systemd.AskPassword`, `io.systemd.Metrics`, `io.systemd.ManagedOOM`,
`io.systemd.MountFileSystem`, `io.systemd.MuteConsole`, `io.systemd.NamespaceResource`,
`io.systemd.PCRExtend`, `io.systemd.PCRLock`, `io.systemd.Repart`, `io.systemd.Shutdown`,
`io.systemd.StorageProvider`, `io.systemd.Udev`, `io.systemd.UserDatabase`, `io.systemd.oom`,
`io.systemd.oom.Prekill`, `io.systemd.service`, `io.systemd.sysext`.

### Command-line surface

`systemctl`, `journalctl`, `networkctl`, `resolvectl`, `loginctl`, `machinectl`, `hostnamectl`,
`timedatectl`, `localectl`, `busctl`, `varlinkctl`, `bootctl`, `homectl`, `coredumpctl`,
`oomctl`, `portablectl`, `importctl`, `systemd-analyze`, `systemd-run`, `systemd-id128`,
`systemd-path`, `systemd-cgls`, `systemd-cgtop`, `systemd-firstboot`, `systemd-mount`,
`systemd-notify`, `systemd-socket-activate`, `systemd-tmpfiles`, `systemd-sysusers`,
`udevadm`, and more.

Per the upstream stability policy, **the D-Bus and Varlink interfaces are stable**; the CLI
tools are stable but their human-formatted output is not — use `systemctl show`, `--output=json`,
or Varlink calls for machine consumption.

## Repository layout

```
systemd/
├── apis.yml                  # apis.yml network entry
├── README.md                 # this file
├── openapi/                  # OpenAPI 3.1 contracts modeling each interface family
│   ├── systemd1-openapi.yml
│   ├── login1-openapi.yml
│   ├── network1-openapi.yml
│   ├── resolve1-openapi.yml
│   ├── machine1-openapi.yml
│   ├── hostname1-openapi.yml
│   └── varlink-openapi.yml
├── capabilities/             # Naftiko capability compositions
│   ├── systemd1-units.yaml
│   ├── systemd1-jobs.yaml
│   ├── systemd1-manager.yaml
│   ├── login1-sessions.yaml
│   ├── network1-links.yaml
│   ├── resolve1-dns.yaml
│   ├── machine1-machines.yaml
│   ├── varlink-manager.yaml
│   └── varlink-userdb.yaml
├── json-schema/              # JSON Schemas for key entities
│   ├── systemd1-unit-schema.json
│   ├── systemd1-job-schema.json
│   ├── login1-session-schema.json
│   ├── network1-link-schema.json
│   ├── machine1-machine-schema.json
│   └── varlink-user-record-schema.json
├── json-structure/
│   └── systemd-structure.json
├── json-ld/
│   └── systemd-context.jsonld
├── examples/                 # Request/response payloads
│   ├── systemd1-listunits-example.json
│   ├── systemd1-startunit-example.json
│   ├── systemd1-starttransient-example.json
│   ├── login1-listsessions-example.json
│   ├── login1-inhibit-example.json
│   ├── resolve1-resolvehostname-example.json
│   ├── network1-listlinks-example.json
│   ├── machine1-listmachines-example.json
│   ├── varlink-userdb-getuser-example.json
│   └── varlink-credentials-encrypt-example.json
├── rules/
│   └── systemd-rules.yml
└── vocabulary/
    └── systemd-vocabulary.yml
```

## Notes on modeling D-Bus / Varlink in OpenAPI

OpenAPI was built for HTTP, but the structural shape — operations with typed inputs/outputs,
hierarchical paths, status codes — maps cleanly onto D-Bus method calls and Varlink calls if
you treat:

- the **bus name** as the server host (`dbus://system/<bus.name>`),
- the **object path / interface** as the URL path (`/units/{name}`),
- the **method name** as the `operationId`,
- the **method arguments** as the request body, and
- the **return value** as the response body.

The OpenAPI documents in `openapi/` are documentation contracts, not HTTP services. Calls are
issued with `busctl`, `varlinkctl`, `dbus-send`, `sd-bus`, `sd-varlink`, or any language binding.
