<div align="center">
  <img src="assets/banner-2.0.jpg" width="100%" alt="Maelstrom 2.0" />
  <br/>
  <img src="assets/maelstrom.png" width="120" alt="Maelstrom" />
  <h1>Maelstrom 2.0</h1>
  <p><em>Kernel C2. Post-quantum TLS. Full EDR evasion guarantee. An AI agent runs the stack through mop.</em></p>
  <p>
    <img src="https://img.shields.io/badge/KERNEL-LPE%20%7C%20BYOVD%20%7C%20UNKILL-2ee6d6?style=flat-square&labelColor=071018" alt="KERNEL"/>
    <img src="https://img.shields.io/badge/C2-ML--KEM--1024%20CNSA%202.0-7c5cff?style=flat-square&labelColor=071018" alt="ML-KEM-1024"/>
    <img src="https://img.shields.io/badge/UET%202.0-FULL%20EDR%20EVASION%20GUARANTEE-e8d9b8?style=flat-square&labelColor=071018" alt="UET 2.0"/>
    <img src="https://img.shields.io/badge/mop-AI%20operator-2ee6d6?style=flat-square&labelColor=071018" alt="AI mop"/>
  </p>
  <p>
    Public product page · source is private · annual subscription<br/>
    <a href="#contact">Contact / license</a>
    ·
    <a href="LICENSE">Maelstrom Software License 2.0</a>
  </p>
</div>

<p align="center">
  <img src="assets/pillars.jpg" width="100%" alt="UET guarantee, kernel, post-quantum TLS, AI operator" />
</p>

This repository is the **public front** of Maelstrom 2.0 — demo images and the feature list. The teamserver, Qt GUI, mop API, implants, builders, and kernel modules ship to licensed operators. Possession of this page is not a license.

Authorized red team and laboratory use. Annual license — [contact](#contact).

---

## Full EDR evasion guarantee

<p align="center">
  <img src="assets/uet-guarantee.jpg" width="92%" alt="Full EDR evasion guarantee" />
</p>

**UET 2.0** is the full EDR evasion guarantee for licensed operators:

WaitCrypt · SecMap (`MEM_MAPPED` PIC) · SignerQuiet (`SEC_IMAGE` on a Microsoft System32 image) · syscall match · APC · per-build API hashes.

Lab-proven next to Sysmon / Wazuh. Each implant build has its own hash class.

---

## vs Cobalt Strike

<p align="center">
  <img src="assets/vs-cs.jpg" width="100%" alt="Maelstrom 2.0 vs Cobalt Strike" />
</p>

| | Cobalt Strike | **Maelstrom 2.0** |
|---|---|---|
| Implant ID | Public Beacon YARA | **Per-build HASH_KEY / HASH_MUL** |
| Ring | User-mode Beacon | **Kernel LPE + BYOVD + Unkill PPL** |
| C2 crypto | Classic TLS | **TLS 1.3 hybrid ML-KEM-768 / ML-KEM-1024 (CNSA 2.0)** |
| Sleep | Sleepmask | **WaitCrypt + DeathSleep NX + SecMap** |
| Loader | Reflective / classic RWX | **SignerQuiet — SEC_IMAGE System32** |
| Linux / macOS | SSH beacon | **Native ELF + Mach-O** |
| Operator API | Aggressor | **mop JSON + unix + HTTP /v1** |
| AI operator | Human console | **Full C2 through mop — AI runs the stack** |
| Process armor | — | **7-star checkin (PPL / PP / kamikaze)** |
| License | Per-team commercial | **Annual operator subscription** |

---

## AI operator — full C2 through mop

<p align="center">
  <img src="assets/mop-ai.jpg" width="100%" alt="AI operator on mop" />
</p>

mop is a first-class operator seat, built for an AI agent. JSON in, JSON out. The Qt GUI stays logged in.

The agent drives sessions, Generate, listeners, BOF modules, and the kernel kit (`lpe` / `unkill` / `byovd`). Unhealthy sessions return 409. Destructive tasks need an explicit confirm.

<p align="center">
  <img src="assets/screenshots/mop-cli.png" width="92%" alt="mop CLI JSON" />
</p>

---

## Post-quantum C2

<p align="center">
  <img src="assets/pq-c2.jpg" width="92%" alt="Post-quantum C2" />
</p>

HTTPS 443 is TLS 1.3 with hybrid ML-KEM on the **key exchange** (harvest-now, decrypt-later).

| Group | Suite |
|-------|--------|
| `X25519MLKEM768` | IANA 0x11EC |
| `SecP384r1MLKEM1024` | CNSA 2.0 / IANA 0x11ED — ML-KEM-1024 + P-384 |
| Leaf | ECDSA **P-384** |
| MinVersion | TLS 1.3 |

Classical X25519 / P-384 stay as fallback for older Schannel.

---

## Kernel stack

<p align="center">
  <img src="assets/kernel-stack.jpg" width="92%" alt="Kernel stack" />
</p>

Ring 0 is a first-class Generate path.

| Module | Job |
|--------|-----|
| **Kernel LPE** | DirectIo + MSR. Token steal. Windows 10 / 11 24H2+ |
| **BYOVD** | Leftover-signed driver load, Generate-linked |
| **Unkill** | Fileless DKOM — PPL WinSystem, process armor |
| **NOFILTER** | Kernel print-spooler LPE |
| **KDU / DSE** | DSE play via the kernel operator kit |

---

## Architecture

<p align="center">
  <img src="assets/architecture-2.0.jpg" width="92%" alt="Operator, teamserver, implant" />
</p>

| Seat | Role |
|------|------|
| Qt GUI | Human operator, WSS |
| **mop** | AI operator — JSON, unix socket, loopback HTTP |
| Teamserver | Listeners + implants |
| Implant | Windows / Linux / macOS / Kernel PE |

Listeners: HTTP(S), DNS, SMB, TCP, P2P. Generate in-process: exe, dll, svc, shellcode, .NET, droppers, STG1.

<p align="center">
  <img src="assets/screenshots/generate.jpg" width="92%" alt="Generate" />
</p>

---

## License

Maelstrom 2.0 is proprietary commercial software. One annual subscription covers a named operator (or named team, if the order says so) for twelve months.

GUI payment gate after Unkill GA. Until then, DonMorpheus activates subscribers by hand.

Full terms: [LICENSE](LICENSE).

---

## Contact

| | |
|---|---|
| **GitHub Issues** | [Open a license / demo request](https://github.com/DonMorpheus/maelstrom-c2/issues/new?template=demo.md) |
| **Email** | [morpheusdon5@gmail.com](mailto:morpheusdon5@gmail.com) |
| **GitHub** | [DonMorpheus](https://github.com/DonMorpheus) |

Issues stay on this public repo. Email is for a briefing, a demo, or an annual seat. Authorized red-team and owned-lab scope only.

---

<div align="center">
  <p><strong>FULL EDR EVASION GUARANTEE</strong> · UET 2.0 · ML-KEM-1024 · KERNEL · AI MOP</p>
  <p><strong>Maelstrom Software License 2.0</strong> · © 2026 DonMorpheus · annual subscription</p>
  <p>Authorized red-team and laboratory use. This page is not the source tree.</p>
</div>
