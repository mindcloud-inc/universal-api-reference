# <img src="https://images.mindcloud.co/apps/icons/anchor_1774294980147.png" alt="Anchor logo" width="28" height="28"> Anchor: Universal API

Automate browsers, run web tasks, and manage sessions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/anchor/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://anchorbrowser.io
- **Vendor API docs:** https://docs.anchorbrowser.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Profiles](actions/list-profiles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anchor/latest/actions/list-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Browser Session

| Action | Method | Description |
| --- | --- | --- |
| [End Browser Session](actions/end-browser-session.md) | DELETE | Deletes a browser session from Anchor. |
| [Get Browser Session](actions/get-browser-session.md) | GET | Retrieves a browser session from Anchor. |
| [Keyboard Shortcut](actions/keyboard-shortcut.md) | PUT | Sends a keyboard shortcut in an Anchor session. |
| [List Browser Sessions](actions/list-browser-sessions.md) | GET | Retrieves browser sessions from Anchor. |
| [Mouse Click](actions/mouse-click.md) | PUT | Clicks the mouse in an Anchor session. |
| [Navigate to URL](actions/navigate-to-url.md) | PUT | Navigates an Anchor session to a URL. |
| [Start Browser Session](actions/start-browser-session.md) | POST | Creates a browser session in Anchor. |
| [Type Text](actions/type-text.md) | PUT | Types text in an Anchor session. |
| [Upload Files](actions/upload-files.md) | PUT | Uploads files to a browser session in Anchor. |

### Browser Session Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Browser Session Pages](actions/get-browser-session-pages.md) | GET | Retrieves browser session pages from Anchor. |

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Get Page PDF](actions/get-page-pdf.md) | GET | Retrieves a webpage PDF from Anchor. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create Profile](actions/create-profile.md) | POST | Creates a profile in Anchor. |
| [Delete Profile](actions/delete-profile.md) | DELETE | Deletes a profile from Anchor. |
| [Get Profile](actions/get-profile.md) | GET | Retrieves a profile from Anchor. |
| [List Profiles](actions/list-profiles.md) | GET | Retrieves profiles from Anchor. |

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Screenshot Webpage](actions/screenshot-webpage.md) | GET | Retrieves a webpage screenshot from Anchor. |
| [Take Session Screenshot](actions/take-session-screenshot.md) | GET | Retrieves a browser session screenshot from Anchor. |

### Session Download

| Action | Method | Description |
| --- | --- | --- |
| [List Session Downloads](actions/list-session-downloads.md) | GET | Retrieves session downloads from Anchor. |

### Task Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Run Status](actions/get-task-run-status.md) | GET | Retrieves task run status from Anchor. |
| [Run Task](actions/run-task.md) | POST | Creates a task run in Anchor. |

### Web Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Web Task Status](actions/get-web-task-status.md) | GET | Retrieves web task status from Anchor. |
| [Perform Web Task](actions/perform-web-task.md) | POST | Performs a web task in Anchor. |

### Webpage

| Action | Method | Description |
| --- | --- | --- |
| [Get Webpage Content](actions/get-webpage-content.md) | GET | Retrieves rendered webpage or PDF content from Anchor. |
| [Web Unlocker](actions/web-unlocker.md) | GET | Retrieves webpage content from bot-protected sites with Anchor Web Unlocker. |

