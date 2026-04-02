# Digital Forensics and eDiscovery — CA1

### Forensic Investigation of the Facebook Android App

\---

## Assignment Details

|Field|Details|
|-|-|
|**Module**|Digital Forensics and eDiscovery|
|**Assessment**|Continuous Assessment 1 (CA1) |
|**College**|National College of Ireland|
|**Programme**|Masters in Cybersecurity (PGDCYB\_SEP23)|
|**Semester**|Semester 1 — 2025/2026|
|||

\---

## Objective

This investigation focuses on the **Facebook Android app (v531.0.0.47.70)** to examine:

* Whether Facebook's **"unsend" feature** truly deletes message content
* What **forensic artifacts** remain after unsending messages
* The **database structure** of the Facebook app
* Sources of digital evidence available to forensic examiners

\---

## Key Findings

* The **"unsend" feature** deletes message content but leaves behind metadata — including sender identity, timestamp, and recipient info
* The **`prefs\_db` database** preserved complete account details (name, profile photo, user ID, device identifiers, and login timestamps) even after messages were unsent
* A separate **`crypto\_db` database** contains end-to-end encryption implementation with pre-keys, session states, and decrypt/encrypt journals
* The **contacts database** (`ssus.61582371911836.android\_facebook\_contacts\_db`) revealed information about friends in the test account

\---

## Tools \& Environment

|Tool|Purpose|
|-|-|
|**Memu Emulator v9.2.8.0**|Android test environment (Samsung Galaxy Note 10+, Android 9)|
|**Android Debug Bridge (ADB)**|Data acquisition from emulator|
|**DB Browser SQLite v3.13.1**|Primary database examination tool|
|**Autopsy v4.22.1**|File system analysis|
|**SHA-256 Hashing**|Chain of custody / evidence integrity|

\---

## Forensic Artifacts Found

|File|Description|Size|
|-|-|-|
|`msys\_database\_61582371911836`|Messages and threads database|6,709,248 bytes|
|`prefs\_db`|App configurations, user settings, login data|262,144 bytes|
|`time\_in\_app\_61582371911836.db`|Session times and activity durations|28,672 bytes|
|`crypto\_db\_61582371911836.db`|Encrypted message content database|249,856 bytes|
|`android\_facebook\_contacts\_db`|Friends/contacts of test account|90,112 bytes|

\---

## Investigation Framework

This investigation followed the **NIST Digital Forensics Framework**:

**Phase 1 — Collection**

* Set up test environment using Memu Emulator with root access
* Created test Facebook account (User ID: 61582371911836)
* Sent 26 messages over 3 days, then unsent 6 of them
* Used ADB to extract database files
* Calculated SHA-256 hashes for chain of custody

**Phase 2 — Examination**

* Examined SQLite databases using DB Browser SQLite
* Analysed file system using Autopsy

**Phase 3 — Analysis**

* Investigated message tables, encryption databases, and preference files
* Documented all findings with SQL queries and screenshots

**Phase 4 — Reporting**

* Compiled full findings in the report with appendix evidence

\---

## File in this folder

|File|Description|
|-|-|
|`CA1-Digital-Forensics-eDiscovery.docx`|Full investigation report with findings, methodology, screenshots and references|

\---

## References (Key Papers)

* Eriş \& Akbal (2021) — Facebook forensics on Android using Oxygen, Paraben \& Magnet Axiom
* Al Mutawa, Baggili \& Marrington (2012) — Facebook forensics across Android, iPhone \& BlackBerry
* Agrawal, Sharma \& Khatri (2021) — Facebook app analysis in virtual Android environment
* AlThebaity, Mishra \& Shukla (2020) — Forensic recovery of deleted Facebook data on Android
* Dusu \& Riadi (2021) — Mobile forensics of Facebook using NIST Framework

