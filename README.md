# QEMU/Bochs VM Marker Removal Scripts

## Overview

Scripts used to disguise QEMU / KVM virtual machines from malware (or anticheats). These scripts are particularly useful for developers working with virtualization technologies who want to obfuscate the presence of virtual environments.

## Files

### 1. `find_trace_strings.sh`
This script searches for common VM or hypervisor references in the specified source directory.

**Usage:**
```bash
./find_trace_strings.sh [SOURCE_DIRECTORY]
```

If no source directory is provided, it defaults to the current directory.

**Search Patterns:**
- QEMU
- Bochs
- KVMKVMKVM
- KVM
- BXPC
- GenuineIntel
- AuthenticAMD
- QEMU HARDDISK
- QEMU DVD-ROM
- QEMU MICRODRIVE
- Bochs Pseudo

### 2. `remove-qemu-traces.sh`
This script replaces references to QEMU, Bochs, and related markers with custom strings. It's intended to be run in the QEMU source directory.

**Usage:**
```bash
./remove-qemu-traces.sh
```

**Replacement Patterns:**
- Replace CPU identifiers with custom CPU names
- Replace QEMU HARDDISK with custom hard disk names
- Replace QEMU DVD-ROM with custom DVD-ROM names
- Replace Bochs CPU identifiers with custom names
- Replace dates and manufacturer strings

## Contributing

Feel free to submit issues or pull requests if you have suggestions or improvements.

---
