# systemd (systemd)

systemd is a suite of basic building blocks for a Linux system. It runs as PID 1 and is the system and service
manager that bootstraps the rest of the userspace, supervises long-running services, and exposes a coordinated
set of D-Bus and Varlink IPC interfaces for managing services (systemd1), users and sessions (logind),
network interfaces (networkd), name resolution (resolved), containers/VMs (machined), home directories
(homed), boot entries (boot1/sysupdate1), system hostname/locale/timedate, OOM protection (oomd), portable
services, and image imports. The project also publishes a stable command-line surface (systemctl,
journalctl, networkctl, resolvectl, loginctl, machinectl, hostnamectl, timedatectl, localectl, busctl,
varlinkctl, bootctl, homectl, coredumpctl, oomctl, portablectl, importctl, systemd-analyze and more).
systemd is dual-licensed (LGPL-2.1-or-later for libraries and most code, GPL-2.0-or-later for select tools)
and developed openly on GitHub at systemd/systemd.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/systemd/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/systemd/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Boot
- Cgroups
- Container
- D-Bus
- Init
- IPC
- Journal
- Linux
- Logging
- Network
- Open Source
- PID 1
- Service Manager
- System
- Systemd
- Varlink

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs

### systemd Manager (org.freedesktop.systemd1)

Core D-Bus API exposed by PID 1 on the system bus. The Manager object at /org/freedesktop/systemd1
enumerates and controls units (services, sockets, mounts, targets, timers, paths, slices, scopes, swaps,
devices), starts and stops jobs, loads/reloads configuration, manages cgroup-backed transient units, and
emits lifecycle signals (UnitNew, UnitRemoved, JobNew, JobRemoved, Reloading, StartupFinished). Per-unit
interfaces (Unit, Service, Socket, Mount, Slice, Scope, Path, Swap, Timer, Target) expose state,
properties, and operations on individual units.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.systemd1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.systemd1.html)
- **Base URL:** `dbus:org.freedesktop.systemd1`

#### Tags

- Cgroups
- D-Bus
- Service Manager
- Systemd
- Units

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.systemd1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.systemd1.xml)
- [OpenAPI](openapi/systemd1-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/systemd1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/systemd1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd-logind (org.freedesktop.login1)

D-Bus API of systemd-logind for tracking user logins, seats, sessions, and inhibitor locks. Manages
session creation, switching, idle hints, lock/unlock, power-button handling, lid-switch handling,
suspend/hibernate/reboot/power-off operations, and ACLs for hot-pluggable devices.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.login1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.login1.html)
- **Base URL:** `dbus:org.freedesktop.login1`

#### Tags

- D-Bus
- Logind
- Sessions
- Users

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.login1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.login1.xml)
- [OpenAPI](openapi/login1-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/login1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/login1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd-networkd (org.freedesktop.network1)

D-Bus API of systemd-networkd for managing network interfaces, link configuration, DHCP server state,
and netdev/network unit reload. Exposes Manager and per-Link interfaces with methods to set link
properties, reconfigure, force renew, and query link state.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.network1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.network1.html)
- **Base URL:** `dbus:org.freedesktop.network1`

#### Tags

- D-Bus
- DHCP
- Network
- Networkd

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.network1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.network1.xml)
- [OpenAPI](openapi/network1-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/network1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/network1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd-resolved (org.freedesktop.resolve1)

D-Bus API of systemd-resolved for DNS/mDNS/LLMNR resolution, DNSSEC validation, per-link DNS
configuration, search domain management, DNS-over-TLS settings, and cache flushing. Exposes
ResolveHostname, ResolveAddress, ResolveRecord, ResolveService and per-Link configuration methods.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.resolve1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.resolve1.html)
- **Base URL:** `dbus:org.freedesktop.resolve1`

#### Tags

- D-Bus
- DNS
- DNSSEC
- Resolved

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.resolve1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.resolve1.xml)
- [OpenAPI](openapi/resolve1-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/resolve1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/resolve1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd-machined (org.freedesktop.machine1)

D-Bus API of systemd-machined for tracking and managing local containers and virtual machines,
enumerating their associated images, opening shells/login sessions inside them, copying files in/out,
and binding mounts across container boundaries.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.machine1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.machine1.html)
- **Base URL:** `dbus:org.freedesktop.machine1`

#### Tags

- Containers
- D-Bus
- Machined
- VMs

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.machine1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.machine1.xml)
- [OpenAPI](openapi/machine1-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/machine1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/machine1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd-hostnamed (org.freedesktop.hostname1)

D-Bus API of systemd-hostnamed for getting and setting the system hostname (static, transient, pretty),
deployment/location/icon metadata, chassis type, and machine info.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.hostname1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.hostname1.html)
- **Base URL:** `dbus:org.freedesktop.hostname1`

#### Tags

- D-Bus
- Hostname
- Hostnamed

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.hostname1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.hostname1.xml)
- [OpenAPI](openapi/hostname1-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hostname1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hostname1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd-localed (org.freedesktop.locale1)

D-Bus API of systemd-localed for getting and setting the system locale, X11 keymap, and console keymap.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.locale1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.locale1.html)
- **Base URL:** `dbus:org.freedesktop.locale1`

#### Tags

- D-Bus
- Locale
- Localed

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.locale1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.locale1.xml)
- [Postman Collection](collections/hostname1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hostname1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/login1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/login1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/machine1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/machine1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/network1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/network1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/resolve1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/resolve1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/systemd1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/systemd1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/varlink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/varlink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd-timedated (org.freedesktop.timedate1)

D-Bus API of systemd-timedated for getting and setting the system time, timezone, NTP enablement, and
RTC-in-local-time policy.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.timedate1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.timedate1.html)
- **Base URL:** `dbus:org.freedesktop.timedate1`

#### Tags

- D-Bus
- NTP
- Time
- Timedated

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.timedate1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.timedate1.xml)
- [Postman Collection](collections/hostname1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hostname1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/login1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/login1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/machine1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/machine1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/network1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/network1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/resolve1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/resolve1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/systemd1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/systemd1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/varlink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/varlink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd-timesyncd (org.freedesktop.timesync1)

D-Bus API of systemd-timesyncd exposing the current NTP server, peers, root delay/dispersion, and
synchronization status.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.timesync1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.timesync1.html)
- **Base URL:** `dbus:org.freedesktop.timesync1`

#### Tags

- D-Bus
- NTP
- SNTP
- Timesyncd

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.timesync1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.timesync1.xml)
- [Postman Collection](collections/hostname1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hostname1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/login1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/login1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/machine1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/machine1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/network1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/network1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/resolve1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/resolve1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/systemd1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/systemd1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/varlink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/varlink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd-homed (org.freedesktop.home1)

D-Bus API of systemd-homed for managing portable, encrypted user home directories (LUKS, btrfs subvol,
fscrypt, CIFS, directory) including create/remove/update/list operations, activation, authentication,
and rebalancing.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.home1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.home1.html)
- **Base URL:** `dbus:org.freedesktop.home1`

#### Tags

- D-Bus
- Home Directories
- Homed
- LUKS

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.home1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.home1.xml)
- [Postman Collection](collections/hostname1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hostname1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/login1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/login1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/machine1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/machine1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/network1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/network1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/resolve1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/resolve1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/systemd1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/systemd1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/varlink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/varlink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd-importd (org.freedesktop.import1)

D-Bus API of systemd-importd for importing, exporting, downloading, listing, and removing container/VM
machine images (tar, raw, dkr/OCI, qcow2) used by machined and portable services.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.import1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.import1.html)
- **Base URL:** `dbus:org.freedesktop.import1`

#### Tags

- Containers
- D-Bus
- Images
- Importd

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.import1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.import1.xml)
- [Postman Collection](collections/hostname1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hostname1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/login1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/login1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/machine1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/machine1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/network1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/network1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/resolve1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/resolve1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/systemd1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/systemd1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/varlink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/varlink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd-oomd (org.freedesktop.oom1)

D-Bus API of systemd-oomd, the userspace out-of-memory killer that uses cgroup v2 PSI signals to kill
cgroups under memory or swap pressure. Exposes per-slice/cgroup state and policy.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.oom1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.oom1.html)
- **Base URL:** `dbus:org.freedesktop.oom1`

#### Tags

- Cgroups
- D-Bus
- OOM
- Oomd
- PSI

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.oom1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.oom1.xml)
- [Postman Collection](collections/hostname1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hostname1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/login1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/login1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/machine1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/machine1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/network1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/network1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/resolve1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/resolve1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/systemd1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/systemd1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/varlink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/varlink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd-portabled (org.freedesktop.portable1)

D-Bus API of systemd-portabled for attaching/detaching portable service images, listing attached
images, inspecting them, and managing their lifecycle on the host.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.portable1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.portable1.html)
- **Base URL:** `dbus:org.freedesktop.portable1`

#### Tags

- D-Bus
- Portable Services
- Portabled

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.portable1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.portable1.xml)
- [Postman Collection](collections/hostname1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hostname1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/login1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/login1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/machine1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/machine1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/network1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/network1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/resolve1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/resolve1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/systemd1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/systemd1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/varlink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/varlink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd-sysupdated (org.freedesktop.sysupdate1)

D-Bus API of systemd-sysupdated for transactional A/B updates of system/host/portable/container images
using systemd-sysupdate transfers, including target enumeration, version listing, and update jobs.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.sysupdate1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.sysupdate1.html)
- **Base URL:** `dbus:org.freedesktop.sysupdate1`

#### Tags

- A/B Updates
- D-Bus
- Sysupdated
- System Updates

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.sysupdate1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.sysupdate1.xml)
- [Postman Collection](collections/hostname1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hostname1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/login1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/login1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/machine1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/machine1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/network1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/network1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/resolve1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/resolve1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/systemd1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/systemd1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/varlink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/varlink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### LogControl1 (org.freedesktop.LogControl1)

Generic D-Bus interface that systemd daemons (and other services) implement to expose runtime log
level and log target configuration. Allows tools like systemd-analyze to change verbosity without
restart.

- **Human URL:** [https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.LogControl1.html](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.LogControl1.html)
- **Base URL:** `dbus:org.freedesktop.LogControl1`

#### Tags

- D-Bus
- Logging
- Observability

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/org.freedesktop.LogControl1.html)
- [Interface Definition](https://github.com/systemd/systemd/blob/main/man/org.freedesktop.LogControl1.xml)
- [Postman Collection](collections/hostname1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hostname1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/login1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/login1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/machine1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/machine1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/network1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/network1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/resolve1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/resolve1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/systemd1.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/systemd1.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/varlink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/varlink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### systemd Varlink Interfaces (io.systemd.*)

Modern JSON-line IPC surface exposed by systemd daemons via Varlink (single-fd, self-describing,
discoverable through `varlinkctl`). Covers ~39 interfaces including io.systemd.Manager, io.systemd.Unit,
io.systemd.Job, io.systemd.Login, io.systemd.Machine, io.systemd.Machine.Image,
io.systemd.MachineInstance, io.systemd.VirtualMachineInstance, io.systemd.Network,
io.systemd.Network.Link, io.systemd.Resolve, io.systemd.Resolve.Hook, io.systemd.Resolve.Monitor,
io.systemd.Journal, io.systemd.JournalAccess, io.systemd.Hostname, io.systemd.BootControl,
io.systemd.Credentials, io.systemd.FactoryReset, io.systemd.Import, io.systemd.InstanceMetadata,
io.systemd.AskPassword, io.systemd.Metrics, io.systemd.ManagedOOM, io.systemd.MountFileSystem,
io.systemd.MuteConsole, io.systemd.NamespaceResource, io.systemd.PCRExtend, io.systemd.PCRLock,
io.systemd.Repart, io.systemd.Shutdown, io.systemd.StorageProvider, io.systemd.Udev,
io.systemd.UserDatabase, io.systemd.oom, io.systemd.oom.Prekill, io.systemd.service, io.systemd.sysext.

- **Human URL:** [https://systemd.io/USER_GROUP_API/](https://systemd.io/USER_GROUP_API/)
- **Base URL:** `varlink:io.systemd`

#### Tags

- IPC
- JSON
- Varlink

#### Properties

- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/varlinkctl.html)
- [Source Code](https://github.com/systemd/systemd/tree/main/src)
- [OpenAPI](openapi/varlink-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/varlink.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/varlink.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://systemd.io)
- [Documentation](https://www.freedesktop.org/software/systemd/man/latest/)
- [GitHub Organization](https://github.com/systemd)
- [GitHub Repository](https://github.com/systemd/systemd)
- [Source Code](https://github.com/systemd/systemd)
- [License](https://github.com/systemd/systemd/blob/main/LICENSES/LGPL-2.1-or-later.txt)
- [License](https://github.com/systemd/systemd/blob/main/LICENSES/GPL-2.0-or-later.txt)
- [Release Notes](https://github.com/systemd/systemd/releases)
- [Changelog](https://github.com/systemd/systemd/blob/main/NEWS)
- [Issue Tracker](https://github.com/systemd/systemd/issues)
- [Pull Requests](https://github.com/systemd/systemd/pulls)
- [Mailing List](https://lists.freedesktop.org/mailman/listinfo/systemd-devel)
- [Mastodon](https://mastodon.social/@pid_eins)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/systemctl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/journalctl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/networkctl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/resolvectl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/loginctl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/machinectl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/hostnamectl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/timedatectl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/localectl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/busctl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/varlinkctl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/bootctl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/homectl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/coredumpctl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/oomctl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/portablectl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/importctl.html)
- [Tool](https://www.freedesktop.org/software/systemd/man/latest/systemd-analyze.html)
- [SDK](https://www.freedesktop.org/software/systemd/man/latest/sd-bus.html)
- [SDK](https://www.freedesktop.org/software/systemd/man/latest/sd-varlink.html)
- [SDK](https://www.freedesktop.org/software/systemd/man/latest/sd-journal.html)
- [SDK](https://www.freedesktop.org/software/systemd/man/latest/sd-event.html)
- [Vocabulary](vocabulary/systemd-vocabulary.yml)
- [JSON-LD](json-ld/systemd-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
