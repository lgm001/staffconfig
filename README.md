# ID4me Outlook Profile Generator

A secure internal-use tool to generate PowerShell scripts for Outlook profile setup using Autodiscover.


## Features

- Dropdown user selection from `users.json`
- Email and display name autofill
- Option to preserve existing Outlook profiles
- PowerShell script generation for registry-based profile creation
- Default profile name fallback to `_id4mecom` if one already exists
- Prompts Outlook for profile selection on launch

---

## Local Development

1. Clone the repository.
2. Add a `users.json` file to the root directory:

   ```json
   [
     { "name": "Alice Smith", "email": "alice@id4me.com" },
     { "name": "Bob Jones", "email": "bob@id4me.com" }
   ]
   ```

3. Open `index.html` in your browser.

---

## Azure Static Web Apps

This project is compatible with Azure Static Web Apps.  
Include the following `staticwebapp.config.json` in the root:

```json
{
  "navigationFallback": {
    "rewrite": "/index.html",
    "exclude": ["/images/*", "/css/*", "/js/*"]
  },
  "mimeTypes": {
    ".json": "application/json",
    ".ps1": "text/plain"
  }
}
```

---

## File Structure

```
├── index.html                  # Main interface
├── users.json                  # User definitions (not committed)
├── staticwebapp.config.json    # Azure Static Web App config
├── README.md
```
```

Let me know if you'd like it committed as a file or styled for internal doc systems too.
