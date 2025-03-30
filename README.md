Perfect — here's a proper `README.md` for the Git repo backing the **ID4me Outlook Profile Generator**:

---

```markdown
# ID4me Outlook Profile Generator

A secure internal web tool for generating PowerShell scripts that preconfigure Outlook profiles for ID4me-managed users using Autodiscover.

---

## 🔍 Purpose

This tool simplifies the setup of Outlook profiles by allowing staff to generate a PowerShell script tailored to their user account. The script sets registry keys required for Outlook's Autodiscover to function correctly.

---

## 🧩 Features

- User selection from a dropdown list (`users.json`)
- Auto-filled email and display name
- Toggle to preserve existing Outlook profiles
- Registry-safe PowerShell generation
- Prompts Outlook to choose profile on next launch

---

## 🛠️ Local Development

1. Clone this repository.
2. Ensure a valid `users.json` is placed in the root directory. Example:
   ```json
   [
     { "name": "Alice Admin", "email": "alice@id4me.com" },
     { "name": "Bob Builder", "email": "bob@id4me.com" }
   ]
   ```
3. Open `index.html` in any browser.

---

## ⚠️ Important Notes

- **Do not deploy this publicly.** It is for internal administrative use only.
- The generated script writes to the current user’s registry under:
  - `HKCU:\Software\Microsoft\Office\16.0\Outlook`
- If a profile named `OutlookAutodiscover` already exists, the script appends `_id4mecom` to avoid overwriting.
- The checkbox **"Keep existing profiles"** is checked by default and should only be unchecked by advanced users.

---

## 📂 File Structure

```
├── index.html            # Main tool interface
├── users.json            # Source of user accounts
├── README.md             # You're here
```

---

## 🧯 Support & Maintenance

This tool is maintained by the internal IT automation team.  
For questions, contact: `support@id4me.com`.

---

## 🧾 License

This project is proprietary and not licensed for external distribution.
```

---

Want me to drop this directly into a `README.md` file for your repo?
