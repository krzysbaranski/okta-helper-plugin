# okta-helper-plugin

A Chrome extension that speeds up the Okta login flow by:

- **Pre-filling** your username / email on the sign-in page.
- **Checking the "Remember Me" checkbox** automatically.
- **Clicking "Next"** to advance to the password step (optional).

---

## Installation (Developer / Unpacked)

1. Clone or download this repository.
2. Open **Chrome** and navigate to `chrome://extensions`.
3. Enable **Developer mode** (toggle in the top-right corner).
4. Click **Load unpacked** and select the repository folder.
5. The *Okta Login Helper* icon will appear in the Chrome toolbar.

---

## Usage

1. Click the extension icon to open the settings popup.
2. Enter your **default username** (email address).
3. Toggle **Check "Remember Me"** on if you want the checkbox ticked automatically.
4. Toggle **Auto-click Next** on if you want the form submitted automatically after the username is filled.
5. Click **Save Settings**.

The next time you visit an Okta sign-in page the extension will apply your settings automatically.

---

## Supported Okta Environments

The extension activates on the following Okta domains:

| Domain pattern      | Example                   |
|---------------------|---------------------------|
| `*.okta.com`        | `yourorg.okta.com`        |
| `*.okta-emea.com`   | `yourorg.okta-emea.com`   |
| `*.oktapreview.com` | `yourorg.oktapreview.com` |
| `*.login.samba.tv`  | `yourorg.login.samba.tv`  |

Both **Classic Engine** and **Okta Identity Engine (OIE)** page layouts are supported.

---

## Files

| File | Purpose |
|---|---|
| `manifest.json` | Chrome extension manifest (v3) |
| `popup.html` | Settings UI shown when the toolbar icon is clicked |
| `popup.js` | Loads and saves settings via `chrome.storage.sync` |
| `content.js` | Runs on Okta pages; fills username, checks Remember Me, clicks Next |
| `icons/` | Extension icons (16 × 16, 48 × 48, 128 × 128 px) |

---

## Privacy

All settings are stored locally in Chrome's synced storage (`chrome.storage.sync`).  
No data is sent to any external server.
