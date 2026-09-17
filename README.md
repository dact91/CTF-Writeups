# CTF & Offensive Security Writeups

Writeups documenting my hands-on offensive security practice — enumeration, exploitation, and privilege escalation across Linux, Windows AD, and multi-host AD environments, each written up the way I'd report it on a real engagement.

---

## Navigation

<details>
<summary><strong>Linux</strong></summary>

- [Orion](Linux/Orion_HTB/orion.md) — HTB, Easy
- [SysAdmins](Linux/SysAdmins_HackSmarter/sysadmins.md) — HackSmarter, Medium
- [Walnut](Linux/Walnut_HackSmarter/walnut.md) — HackSmarter, Easy
- [Casino](Linux/Casino_HackSmarter/casino.md) — HackSmarter, Medium

</details>

<details>
<summary><strong>Windows AD</strong></summary>

- [ShadowGate 2](WindowsAD/ShadowGate2_HackSmarter/shadowgate-2.md) — HackSmarter, Medium
- [404 Bank](WindowsAD/404bank_HackSmarter/404-bank.md) — HackSmarter, Medium
- [Midgarden 2](WindowsAD/Midgraden2_HackSmarter/midgarden-2.md) — HackSmarter, Hard
- [NorthBridge](WindowsAD/NorthBridge_HackSmarter/northbridge.md) — HackSmarter, Hard
- Building Magic — HackSmarter, Easy _(coming soon)_

</details>

<details>
<summary><strong>Windows AD Ranges</strong></summary>

- [BitStream](WindowsAD_Ranges/BitStream_HackSmarter/bitstream.md) — HackSmarter, Easy
- [CTOS](WindowsAD_Ranges/CTOS_HackSmarter/ctos.md) — HackSmarter, Medium

</details>

---

## All Writeups

| Machine | Platform | OS | Difficulty | Key Themes | Highlight |
|---|---|---|---|---|---|
| [Orion](Linux/Orion_HTB/orion.md) | HTB | Linux | ![Easy](https://img.shields.io/badge/-Easy-brightgreen) | CMS RCE, telnet auth bypass | Chained a CVE'd telnet binary into a straight root shell. |
| [SysAdmins](Linux/SysAdmins_HackSmarter/sysadmins.md) | HackSmarter | Linux | ![Medium](https://img.shields.io/badge/-Medium-orange) | SNMP enum, sudo CVE | A years-old breached password still unlocked root. |
| [Walnut](Linux/Walnut_HackSmarter/walnut.md) | HackSmarter | Linux | ![Easy](https://img.shields.io/badge/-Easy-brightgreen) | LDAP creds, NFS misconfig | Rewrote `/etc/shadow` remotely via a permissive NFS export. |
| [Casino](Linux/Casino_HackSmarter/casino.md) | HackSmarter | Linux | ![Medium](https://img.shields.io/badge/-Medium-orange) | SSTI, credential chain | SSTI-based file read led straight to a private SSH key. |
| [ShadowGate 2](WindowsAD/ShadowGate2_HackSmarter/shadowgate-2.md) | HackSmarter | Windows AD | ![Medium](https://img.shields.io/badge/-Medium-orange) | SQLi, ACL abuse, ADCS ESC3 | Revived a deleted account and forged a certificate to take the domain. |
| [404 Bank](WindowsAD/404bank_HackSmarter/404-bank.md) | HackSmarter | Windows AD | ![Medium](https://img.shields.io/badge/-Medium-orange) | ACL chaining, ADCS ESC4 | Chained ACLs to re-enable a disabled account, then template-hijacked ADCS. |
| [Midgarden 2](WindowsAD/Midgraden2_HackSmarter/midgarden-2.md) | HackSmarter | Windows AD | ![Hard](https://img.shields.io/badge/-Hard-red) | BadSuccessor, DCSync | Used the newly-disclosed BadSuccessor dMSA attack to DCSync the domain. |
| [NorthBridge](WindowsAD/NorthBridge_HackSmarter/northbridge.md) | HackSmarter | Windows AD | ![Hard](https://img.shields.io/badge/-Hard-red) | RBCD, DPAPI extraction | Bypassed a hardened Machine Account Quota to pull off RBCD anyway. |
| Building Magic _(coming soon)_ | HackSmarter | Windows AD | ![Easy](https://img.shields.io/badge/-Easy-brightgreen) | _Pending publication_ | _Pending publication_ |
| [BitStream](WindowsAD_Ranges/BitStream_HackSmarter/bitstream.md) | HackSmarter | Windows AD | ![Easy](https://img.shields.io/badge/-Easy-brightgreen) | IDOR, DCSync | An inbox IDOR ultimately chained into a full DCSync. |
| [CTOS](WindowsAD_Ranges/CTOS_HackSmarter/ctos.md) | HackSmarter | Windows AD | ![Medium](https://img.shields.io/badge/-Medium-orange) | Deserialization RCE, GPO abuse | A cracked KeePass vault fed an ACL chain into a GPO-based domain takeover. |

---

## Repository Structure

```
├── Linux/                      # Standalone Linux machines
├── WindowsAD/                  # Single-host Windows AD machines
├── WindowsAD_Ranges/           # Multi-host Windows AD environments
│
└── <category>/<Machine>_<Platform>/
    ├── <machine>.md
    └── images/
```

Each machine folder is self-contained: one Markdown writeup and its supporting screenshots.