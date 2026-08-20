# Fileless Tool

Fileless Tool is a local Windows forensic application for authorized screenshare sessions and system integrity reviews. It combines live system analysis, offline evidence parsing, and optional physical memory inspection in a single interface.

> This repository distributes the compiled `Fileless Tool.exe` executable only. Source code, internal detection logic, signatures, filtering criteria, scoring rules, and analysis methods are not included.

## Features

- Live analysis of the current Windows system and available historical information
- Offline, read-only analysis of supported evidence files
- Optional acquisition and analysis of physical memory
- Clear findings with severity and evidence levels
- Coverage and availability information for each stage of a scan
- Detailed views for reviewing individual results
- Local processing without requiring evidence uploads

## Analysis Modes

### System Scanner

Reviews information available on the current Windows system and presents relevant findings in a structured report. Administrator privileges are recommended for the most complete coverage.

### Offline Evidence Parser

Analyzes supported text, binary, and Windows dump files selected by the user. Files are processed locally in read-only mode and are never executed as applications.

### RAM Check

Acquires and analyzes physical memory or processes an existing RAW memory image. This mode is intended for advanced post-mortem investigation and may reveal information that is no longer available through regular system inspection.

RAM Check may temporarily use significant CPU, memory, disk space, and disk bandwidth. A modern, well-equipped computer is recommended.

## Requirements

- 64-bit Windows
- .NET 8 Desktop Runtime x64
- Microsoft Edge WebView2 Runtime
- Administrator privileges for complete system inspection and RAM acquisition
- Sufficient free disk space when using RAM Check

The Offline Evidence Parser can be used without performing a live system scan or acquiring physical memory.

## Installation

1. Open the repository's **Releases** page.
2. Download `Fileless Tool.exe`.
3. Place the executable in a directory of your choice.
4. Run it normally for offline analysis or as Administrator for a complete system review.

No installation wizard is required.

## Usage

1. Launch `Fileless Tool.exe`.
2. Select **Scanner**, **Dump**, or **RAM Check**.
3. Follow the instructions displayed in the application.
4. Wait for the selected operation to complete.
5. Review the findings, evidence levels, coverage information, and reported limitations.

## Privacy and Safety

Fileless Tool is designed around local and controlled analysis:

- Selected evidence is processed on the inspected computer.
- Selected files are not executed.
- Evidence does not need to be uploaded to an external service.
- Inspection is designed to avoid modifying the evidence being reviewed.
- Operations can be cancelled from the interface.
- Temporary RAM acquisition data is removed after analysis unless the user explicitly chooses to retain it.

Physical memory images may contain sensitive information. Store, transfer, and delete them responsibly.

## Understanding the Results

A finding represents technical evidence that should be reviewed in context. It does not automatically prove cheating, malicious activity, execution, or ownership by a particular process.

A scan with no findings does not guarantee that a system is clean. Relevant information may be unavailable, disabled, expired, overwritten, inaccessible, or outside the available inspection window.

Fileless Tool reports unavailable, incomplete, denied, or timed-out analysis stages instead of treating them as successful clean results.

## Responsible Use

Fileless Tool is intended for authorized forensic reviews, screenshare sessions, security research, and educational purposes.

Use it only on systems you own or have explicit permission to inspect. You are responsible for complying with applicable laws, privacy requirements, and platform policies.

Fileless Tool is an investigative aid, not an automatic verdict system. Final conclusions should always consider the complete context and be reviewed by a qualified person.

## Support

For support or questions, contact `@d4rk2` on Discord.
