# AryNotes

**Local, offline engagement notebook for authorized penetration testing workflows and general note-keeping.**

AryNotes is a lightweight, browser-based note-taking application for securely logging findings, commands, and evidence during authorized security assessments — or just for study notes and journaling. All data stays on your device by default. No cloud, no accounts, no tracking.

---

## Quick Start

Visit: **https://giriaryan694-a11y.github.io/AryNotes/**

No installation. Everything runs in your browser.

1. Pick a **Mode** (top right) — this sets up your folder structure
2. Click a folder, then **＋ New** to start a note
3. Write, then **💾 Save**

---

## Modes

Modes give you a ready-made folder structure for the kind of work you're doing. Switch anytime from the **Mode ▾** menu in the header, which splits into two sections:

**Default modes**
| Mode | Folders |
|---|---|
| **Freedom Mode** | Blank — build your own, for study/journaling/general notes |
| **Pentest Mode** | Reconnaissance, Enumeration, Vulnerabilities, Exploitation, Post-Exploitation, Credentials, Evidence, Reporting |
| **Bug Bounty Mode** | Scope & Program Rules, Recon, Asset & Subdomain Enum, Vulnerabilities, Proof of Concept, Reports Submitted, Triage & Payouts |
| **OSINT Mode** | Target Profile, Social Media, Public Records, Infrastructure & DNS, Leaks & Breach Data, Documentation |
| **OffSec Plan Mode** | RoE, CONOPS, Mission Plan, Communication Plan, Operation Plan, Resources Plan, Reporting Plan, Intelligence Collection Plan, Risk Assessment, Kill Chain / Attack Path, Rollback / Recovery Plan |

OffSec Plan Mode also drops a pinned **"ℹ️ About"** note into every folder explaining what that planning document is, why it matters, and what to put in it — real engagement-planning reference material, not just empty folders. Don't need them? Toggle **👁 Hide starter notes** in the sidebar to tuck them away without deleting them.

**Installed / created modes**
- **＋ Create custom mode** — name it, optionally list starter folders
- **⇧ Import mode** — load a `.json` template or a `.zip` (full folders + notes + attachments) someone shares with you
- **⇩ Export mode template (.json)** — share just your folder structure
- **⇩ Export mode + notes (.zip)** — share the real folders, notes as `.md` files, and attachments, all zipped

---

## Writing Notes

- **Title, tags, folder** — required basics; tags are comma-separated
- **Line numbers** — a code-editor-style gutter tracks lines as you type, in both Write and Preview
- **Write / Preview tabs** — Preview renders full markdown: headers, bold/italic, `code`, fenced ```code blocks```, bullet & numbered lists, tables, blockquotes, horizontal rules, and links. Your Write/Preview choice sticks as you switch between notes — it won't reset to Write every time you open something.

### Attachments (drag & drop into the note)
Drop a file straight into the editor and it embeds inline — no separate upload step:

| File type | What happens |
|---|---|
| Image (png/jpg/gif/webp) | Embedded inline, shows in Preview |
| Video (mp4/webm/mov) | Embedded as a playable video in Preview (4MB cap) |
| PDF | Embedded as an in-line viewer with a Download link (4MB cap) |
| CSV | Parsed and inserted as a real markdown table (up to 50 rows shown) |
| XLSX | First sheet parsed and inserted as a markdown table |
| Anything else | Added as a downloadable attachment link (4MB cap) |

The size caps exist because everything is stored as base64 in browser storage — see [Storage](#storage) below for a way around that.

---

## Organizing: Pinning & Reordering

- **📌 Pin** — every folder and note has a pin toggle. Pinned items get their own section at the top, above the rest
- **⇅ Reorder** — click the ⇅ button above the folder list or note list to enter edit mode, then drag items by the ⋮⋮ handle to rearrange them. Click again ("✓ Done") to lock it in
- Pinning and manual order are independent — pin something to keep it visible, reorder to control the sequence within pinned or unpinned groups

---

## Search

Type in the search box to filter by title, content, or tags — scoped to the current folder or across **≡ All Notes**.

---

## Import & Export

**Notes / full workspace**
- **⇩ Export all** — full JSON backup (folders, notes, custom modes)
- **⇧ Import notes** — merge a `.json` backup, or drop in individual `.txt`/`.md` files as new notes

**Per-note**
- **⬇ .txt** — download the open note with a metadata header

**Modes** (see the Modes section above for the `.json` vs `.zip` options)

---

## Themes

**Dark** (default) · **Light** · **Eye-saver** (warm amber) — toggle in the header, saved automatically.

---

## Storage

By default, AryNotes saves to your browser's local storage (device + browser-specific, nothing leaves your machine).

Click **⚙** in the header for storage options:
- **📁 Save notes to a folder on this device** — uses the File System Access API to write `arynotes-data.json` into a real folder you pick, with an automatic browser-storage backup kept alongside it. Useful for larger attachments, syncing via your own cloud drive folder, or just keeping notes as a plain file you control. Chromium browsers only (Chrome/Edge/Brave) — Firefox/Safari stay on browser storage
- **🌐 Switch back to browser storage** — reverts without touching your folder file
- If your browser closes and reopens with permission already granted, it reconnects silently; otherwise a **🔓 Reconnect folder** bar appears at the top

---

## Mobile

On phones, the layout switches to a bottom tab bar: **📁 Folders → 📝 Notes → ✎ Editor**. Tapping a folder jumps to its notes; tapping a note or **New** jumps to the editor. All other actions (mode picker, settings, themes, import/export) collapse into a **☰** menu.

---

## Local Storage Limits

Most browsers cap local storage around 5–10MB per site:
- 100–500 text-only notes ≈ 1–5MB ✅
- 20–50 notes with a few small attachments ≈ 3–10MB ✅
- Regularly attaching video/PDFs → use **⚙ Local Folder storage** instead

Export backups (**⇩ Export all**) periodically regardless of which storage mode you use.

---

## Privacy & Security Notes

- No network calls for your notes — everything stays local unless you export/share a file yourself
- Notes are stored in plaintext (no built-in encryption) — use your OS's disk encryption (BitLocker/FileVault) for extra protection
- No password lock — anyone with access to your browser profile or connected folder can read your notes
- Sanitize exported backups before sharing (remove real credentials/client names if needed)

---

## FAQ

**Team collaboration?** Not built-in — export a mode `.zip` or workspace `.json` and share manually.

**Sync across devices?** Not automatic. Export from one, import on the other — or use Local Folder storage pointed at a synced cloud folder.

**Password protection?** Not built-in. Rely on device-level encryption, or keep exported files on an encrypted drive.

**Why no cloud sync?** Sensitive engagement notes shouldn't leave your machine by default. Local-first is intentional.

---

## Browser Compatibility

Chrome, Edge, Brave, Firefox, Safari (modern versions). Local Folder storage specifically needs a Chromium browser.

---

## Disclaimer

Use AryNotes only for authorized penetration testing, bug bounty programs you're enrolled in, personal study, or note-taking on your own systems. The creator assumes no liability for misuse or data loss — keep backups.

---

**AryNotes** — Made by **Aryan Giri**.
Visit: https://giriaryan694-a11y.github.io/AryNotes/
