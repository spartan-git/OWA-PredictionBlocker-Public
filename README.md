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

## Privacy Policy

**Effective Date:** July 7, 2026

### 1. Overview
The **Outlook OWA Text Prediction Blocker** extension values and respects user privacy. This Privacy Policy outlines how our software interacts with data while you utilize the tool.

### 2. Data Collection and Transmission
* **Zero Data Collection:** We do not collect, store, track, transmit, or monetize any personal information, browsing history, or user communications.
* **Local Processing:** All code executes strictly and locally within your client browser instance. 
* **No Remote Telemetry:** The extension does not configure or maintain external server infrastructures, tracking pixels, or third-party analytical frameworks.

### 3. Functional Data Use
The extension injects a CSS stylesheet and a localized JavaScript payload exclusively into authorized `https://cloud.microsoft*` domains. It scans elements inside your active viewport for the sole purpose of hiding automated predictive elements inside text input fields. 

### 4. Third-Party Sharing
Because no user metrics, behavioral profiles, or data packets are harvested or cached, no information is ever shared with or sold to third-party entities.

### 5. Policy Updates
We reserve the right to modify this policy to align with future web standard revisions or browser manifest alterations. Updated policies will be documented transparently directly within this file.

### 6. Contact Support
For code inquiries, open repository issues, or questions regarding this statement, please reach out via GitHub Issues or contact the developer directly at: **IT@spartancapitalgroup.com**

---

## License
Copyright (c) 2026 Spartan Capital Group, LLC. All rights reserved.

This software and associated documentation files are the intellectual property 
of Spartan Capital Group, LLC. 

Strictly for internal use only. Unauthorized copying, distribution, modification, 
or transmission of this file, via any medium, is strictly prohibited.
