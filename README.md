# wipechain

wipechain is a cross-platform external-drive wiping toolkit designed for
**intentional, controlled, and auditable destructive operations**.

It provides OS-specific scripts for securely wiping **external storage devices**
while prioritizing operator awareness and minimizing the risk of accidental data loss.

> ⚠️ WARNING: These scripts permanently erase data. Use only on drives you explicitly intend to wipe.

---

## What’s Included

- `wipe_external_arch.sh` — Arch-based Linux
- `wipe_external_deb.sh` — Debian/Ubuntu-based Linux
- `wipe_external_rhel.sh` — RHEL/Fedora-based Linux
- `wipe_external_macos.sh` — macOS
- `wipe_external_windows.ps1` — Windows (PowerShell)

Each script is written specifically for its target OS and tooling.

---

## Design Principles

- **External-drive only scope** (no system disk automation)
- **Explicit device identification**
- **Operator confirmation gates**
- **Predictable, transparent behavior**
- **No hidden automation**

The operator remains in control at all times.

---

## Safety Model

Before running any script:
1. Disconnect all non-target external drives
2. Identify the target device by size, model, and interface
3. Confirm the device is not the system disk
4. Unmount/eject the target drive if required by the OS

---

## Usage

Scripts are executed directly on their target OS.

Examples:

### Linux
```bash
bash wipe_external_deb.sh
macOS
bash wipe_external_macos.sh
Windows
Run PowerShell as Administrator:

.\wipe_external_windows.ps1
Refer to the header comments in each script for OS-specific details.

Status
Core scripts: implemented

Cross-platform coverage: complete

Documentation: ongoing

Planned improvements:

unified wrapper script

standardized logging output

optional dry-run mode where supported

License
This project is licensed under the terms in the LICENSE file.