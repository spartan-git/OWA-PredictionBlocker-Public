# Outlook OWA Text Prediction Blocker

A lightweight Chrome Web Extension that improves your writing focus by hiding automated inline text predictions and suggestions while you type in Outlook on the web.

### Privacy Policy Below ###

## Features
* **Zero Distractions:** Disables the grey ghost-text inline predictions in the compose windows.
* **100% Private:** Operates entirely locally. No tracking, no analytical scripts, and no external servers.
* **Ultra-Lightweight:** Only triggers on target Outlook mail paths to maximize system performance.

---

## Installation

### For Users (Manual Installation)
1. Download or clone this repository to your local machine.
2. Open Google Chrome and navigate to `chrome://extensions/`.
3. Enable **Developer mode** using the toggle switch in the top-right corner.
4. Click **Load unpacked** in the top-left corner.
5. Select the root folder containing the extension files (including the `manifest.json`).

---

## Technical Details

### Permissions & Architecture
This extension requests access strictly to target Outlook mail portals via isolated content scripts:
* **No `activeTab` or management permissions:** Maximizes user security by requesting minimal API access.
* **Optimized Match Patterns:** Uses highly scoped URLs to prevent unnecessary background processes on other websites.

### `manifest.json` Structure
```json
{
  "manifest_version": 3,
  "name": "Outlook OWA Text Prediction Blocker",
  "version": "1.0",
  "description": "Hides automated text prediction inline suggestions in Outlook on the web.",
  "content_scripts": [
    {
      "matches": [
        "https://cloud.microsoft*"
      ],
      "css": ["content.css"],
      "js": ["content.js"],
      "run_at": "document_idle"
    }
  ]
}
```

---

# Privacy Policy

**Effective Date:** July 7, 2026

## 1. Overview

Outlook OWA Text Prediction Blocker is a browser extension designed to hide Outlook Web App text prediction and suggestion interfaces while composing email.

The extension operates entirely within the user's browser and does not collect, store, or transmit user data.

## 2. Data Collection

Outlook OWA Text Prediction Blocker does not collect, store, transmit, share, sell, or otherwise process personal information.

The extension does not collect:

- Personal information
- Email content
- Email addresses
- Recipient information
- Authentication credentials
- Browsing history
- Location information
- Analytics data
- User activity data

## 3. How the Extension Works

The extension runs only on Outlook Web App pages matching:

`https://outlook.cloud.microsoft/mail/*`

To perform its functionality, the extension injects local CSS and JavaScript files into supported Outlook Web App pages.

These files identify, hide, or remove Outlook text prediction and suggestion interface elements. All processing occurs locally within the browser and is performed solely to prevent predictive text suggestions from being displayed.

The extension does not:

- Read email content
- Analyze typed text
- Record keystrokes
- Store communications
- Monitor browsing activity
- Transmit information to external services

## 4. Data Storage and Transmission

All processing occurs locally within the user's browser.

The extension:

- Does not use remote servers
- Does not use cloud services
- Does not use analytics platforms
- Does not use advertising networks
- Does not transmit user data

No user data leaves the user's device.

## 5. Third-Party Sharing

Because the extension does not collect or store user data, no user information is shared, sold, transferred, or disclosed to third parties.

## 6. Changes to This Privacy Policy

This Privacy Policy may be updated to reflect future changes to the extension or browser platform requirements. Any updates will be published with the extension listing or privacy policy page.

## 7. Contact

For questions regarding this Privacy Policy or the extension, please contact:

**Spartan Capital Group**  
**IT@spartancapitalgroup.com**
---

## License
Copyright (c) 2026 Spartan Capital Group, LLC. All rights reserved.

This software and associated documentation files are the intellectual property 
of Spartan Capital Group, LLC. 

Strictly for internal use only. Unauthorized copying, distribution, modification, 
or transmission of this file, via any medium, is strictly prohibited.
