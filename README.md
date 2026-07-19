# AryNotes

**Local, offline engagement notebook for authorized penetration testing workflows and general note-keeping.**

AryNotes is a lightweight, browser-based note-taking application designed to securely store findings, commands, and evidence during authorized security assessments. All data remains strictly on your device—no cloud, no servers, 100% offline.

---

## Quick Start

### Open AryNotes
Visit: **https://giriaryan694-a11y.github.io/AryNotes/**

No installation, no downloads required. Everything runs in your browser.

### Choose Your Mode
- **Freedom Mode** — Blank slate. Build your own folders for study, journaling, general use
- **Pentest Mode** — Pre-loaded with 8 standard engagement folders (Recon, Enumeration, Vulnerabilities, Exploitation, Post-Exploitation, Credentials, Evidence, Reporting)

### Create a Note
1. Select or create a folder from the sidebar
2. Click **＋ New** to start a fresh note
3. Enter a title and write your findings
4. Click **💾 Save** to persist to your browser

---

## Features at a Glance

✅ **Organized by Folders** — Categorize findings by engagement phase, client, or topic  
✅ **Full-Text Search** — Find notes instantly across all folders  
✅ **Markdown-Lite Rendering** — Write markdown, preview inline (images, bold, italic, code)  
✅ **Drag-and-Drop Images** — Drop screenshots directly; embedded as base64, no uploads  
✅ **Three Themes** — Dark, Light, Eye-saver (amber) for reduced eye strain  
✅ **Import/Export** — Full JSON backups for archival or transfer between devices  
✅ **100% Offline & Local** — Zero network calls, 100% private, browser storage only  

---

## Pentest Mode Folders

When you enable Pentest Mode, you get these 8 default folders:

| Folder | Purpose |
|--------|---------|
| **Reconnaissance** | Target identification, OSINT, passive gathering |
| **Enumeration** | Active scanning, service discovery, version detection |
| **Vulnerabilities** | CVEs found, misconfigurations, exploitable weaknesses |
| **Exploitation** | Successful attacks, proof of concept, shell access |
| **Post-Exploitation** | Lateral movement, privilege escalation, persistence |
| **Credentials** | Harvested usernames, passwords, API keys |
| **Evidence** | Screenshots, logs, artifacts for reporting |
| **Reporting** | Client summary, risk ratings, remediation steps |

---

## How to Use

### Write a Note
- **Title** — Required; used for search and identification
- **Tags** — Comma-separated keywords (e.g., `recon, smb, critical`)
- **Content** — Monospace textarea for commands, output, findings
- **Folder** — Assign to organize by engagement phase or topic

### Markdown-Lite Support
```
**bold text**  →  **bold**
*italic text*  →  *italic*
`code text`    →  code block
![alt](url)    →  inline image
```

### Drag & Drop Images
Simply drag an image file onto the note textarea. It's embedded as base64, stored locally—no external uploads.

### Search Notes
Type in the search box to filter by title, content, or tags. Search works within the selected folder or across all notes.

### Preview Mode
Toggle between **Write** (raw text) and **Preview** (rendered markdown + images) using the tabs above the textarea.

---

## Import & Export

### Export Your Workspace
Click **⇩ Export all** to download a complete JSON backup. Use this to:
- Archive engagement notes
- Transfer between machines or browsers
- Back up before clearing browser storage
- Share folder structure with colleagues

### Export a Single Note
Click **⬇ .txt** to download the current note as a text file with metadata (title, folder, tags, timestamp).

### Import Notes
Click **⇧ Import**, then select:
- **JSON files** — Full workspace backup (merges without overwriting)
- **TXT/MD files** — Each becomes a single note in your selected folder

---

## Themes

Toggle in the header (top right):

- **Dark** — Default; reduces eye strain in low-light
- **Light** — High contrast for daylight or accessibility
- **Eye-saver** — Warm amber background for extended use

Your theme preference is saved automatically.

---

## Keyboard Shortcuts & Quick Actions

| Action | How |
|--------|-----|
| Save note | Click **💾 Save** or `Ctrl+S` (browser) |
| New note | Click **＋ New** |
| Delete note | Click **🗑 Delete** (appears after opening a note) |
| Download as .txt | Click **⬇ .txt** |
| Toggle Preview | Click **Preview** tab |
| Search | Type in search box (real-time filtering) |
| Switch folder | Click folder in sidebar |
| View all notes | Click **≡ All Notes** |

---

## Local Storage & Data Safety

### What Happens to Your Notes
- Stored in your browser's `localStorage` (no network, no cloud)
- Persists across browser sessions and restarts
- Cleared only if you explicitly clear browser cache/data

### Storage Limits
Most browsers allow ~5–10 MB per domain. Practical guidelines:
- 100–500 text-only notes = 1–5 MB ✅
- 20–50 notes with screenshots = 3–10 MB ✅
- Dozens of high-res images = may hit limit ⚠️

**Pro Tip:** Export backups regularly. If you hit limits, export as JSON, clear storage, and re-import.

### Security Notes
- ⚠️ Notes are stored in plaintext (no encryption at rest)
- ⚠️ No password protection built-in
- ✅ No cloud sync = no data leaves your device
- ✅ Use device encryption (BitLocker, FileVault, LUKS) for extra safety

---

## Workflow Example: Authorized Pentest

1. **Start:** Open AryNotes, switch to **Pentest Mode**
2. **Recon:** Log passive findings in **Reconnaissance** folder
3. **Scan:** Log active scans in **Enumeration** folder
4. **Issues:** Document CVEs and weaknesses in **Vulnerabilities**
5. **Attack:** Log successful exploits in **Exploitation**
6. **Escalate:** Record lateral movement in **Post-Exploitation**
7. **Harvest:** Store access creds in **Credentials** folder
8. **Collect:** Save screenshots & logs in **Evidence** folder
9. **Report:** Summarize findings in **Reporting** folder
10. **Backup:** Click **⇩ Export all** before final report delivery

---

## FAQ

**Q: Can I use AryNotes for team collaboration?**  
A: Not directly. It's single-user, offline-first. For teams, export JSON and merge manually.

**Q: Can I sync across my laptop and phone?**  
A: Not automatically. Export from one device, transfer the JSON file, import on the other.

**Q: Is there a mobile app?**  
A: No, but AryNotes is responsive. Open the web version in a mobile browser.

**Q: Can I password-protect my notes?**  
A: Not built-in. Use OS-level encryption on your device, or store exported backups on an encrypted USB.

**Q: What if I accidentally delete a note?**  
A: Deletions are permanent. Always keep regular backups by exporting JSON.

**Q: Why no cloud sync?**  
A: Cloud introduces privacy risks for sensitive engagement notes. Staying local and offline is intentional.

**Q: Can I use this for client reporting?**  
A: Yes. Export individual notes as `.txt` files or copy/paste findings into your report template.

---

## Browser Compatibility

AryNotes works on all modern browsers:
- Chrome/Chromium (v90+)
- Firefox (v88+)
- Safari (v14+)
- Edge (v90+)

Requires `localStorage` support (enabled by default on all modern browsers).

---

## Best Practices

1. **Export Regularly** — Don't rely solely on browser storage
2. **Sanitize Before Sharing** — Remove credentials or customer names from exported backups
3. **Use Encrypted Storage** — Keep exported JSON files on an encrypted drive
4. **Separate Profiles** — Use different browser profiles for different clients (if needed)
5. **Clear Selectively** — Clear only cookies, not all browser data (preserves notes)
6. **Avoid Public WiFi** — Don't open sensitive notes on untrusted networks

---

## Privacy & Disclaimer

**Use AryNotes only for:**
- ✅ Authorized penetration testing engagements
- ✅ Personal study and learning
- ✅ Secure note-taking on your own systems

**Do not use for:**
- ❌ Unauthorized access to systems
- ❌ Illegal or unethical activities

The creator assumes no liability for misuse or data loss. Always maintain encrypted backups of critical notes and follow responsible disclosure practices.

---

**AryNotes** — Keep your findings safe, local, and organized.  
Made by **Aryan Giri** for the security research community.  
Visit: https://giriaryan694-a11y.github.io/AryNotes/
