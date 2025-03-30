
PowerShell Script Output
========================

The generated `.ps1` script performs the following:

- Creates or modifies the registry key:
  HKCU:\Software\Microsoft\Office\16.0\Outlook\AutoDiscover  
  to enable `ZeroConfigExchange`.

- Creates a new Outlook profile:
  HKCU:\Software\Microsoft\Office\16.0\Outlook\Profiles\<ProfileName>

- Sets the new profile as default by updating:
  - DefaultProfile  
  - DefaultProfileName

- Enables `PromptForProfile` so Outlook will prompt the user to choose a profile at launch.

Profile Naming Logic
--------------------

- If a profile named `OutlookAutodiscover` does **not** already exist, it is used.
- If it **does exist**, the fallback name will be:  
  `OutlookAutodiscover_id4mecom`

MIME Type Handling
------------------

To ensure the `.ps1` file is served as plaintext and not executed or blocked by the browser, this line is set in `staticwebapp.config.json`:

  ".ps1": "text/plain"

Important
---------

Running the script modifies the registry under the current user hive (HKCU).  
It does **not** delete or remove existing profiles unless that behavior is explicitly added.
