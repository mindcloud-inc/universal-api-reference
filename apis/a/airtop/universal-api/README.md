# <img src="https://images.mindcloud.co/apps/icons/airtop_1774292191378.png" alt="Airtop logo" width="28" height="28"> Airtop: Universal API

Automate browser sessions, web interactions, and AI extraction

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/airtop/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.airtop.ai
- **Vendor API docs:** https://docs.airtop.ai/api-reference/airtop-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sessions](actions/list-sessions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airtop/latest/actions/list-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Automation

| Action | Method | Description |
| --- | --- | --- |
| [Create Form Filler Automation](actions/create-form-filler-automation.md) | POST | Creates a form-filler automation synchronously in Airtop. |
| [Fill Form With Automation](actions/fill-form-with-automation.md) | PUT | Fills a form synchronously with an Airtop automation. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST | Creates a new file in Airtop. |
| [Push File To Session](actions/push-file-to-session.md) | PUT | Pushes a file to one or more Airtop sessions. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST | Creates a new session in Airtop. |
| [Get Session Info](actions/get-session-info.md) | GET | Retrieves session details from Airtop by ID. |
| [List Sessions](actions/list-sessions.md) | GET | Finds sessions in Airtop by ID or status. |
| [Save Profile On Termination](actions/save-profile-on-termination.md) | PUT | Saves a named profile when an Airtop session terminates. |
| [Terminate Session](actions/terminate-session.md) | DELETE | Terminates an existing session in Airtop. |

### Window

| Action | Method | Description |
| --- | --- | --- |
| [Click](actions/click.md) | PUT | Clicks an element in a specific Airtop window. |
| [Create Window](actions/create-window.md) | POST | Creates a new browser window in Airtop. |
| [File Input](actions/file-input.md) | PUT | Uploads a file in a specific Airtop window. |
| [Get Window Info](actions/get-window-info.md) | GET | Retrieves browser window details from Airtop. |
| [List Windows](actions/list-windows.md) | GET | Retrieves browser windows from an Airtop session. |
| [Load URL](actions/load-url.md) | PUT | Loads a specified URL in an Airtop window. |
| [Monitor For Condition](actions/monitor-for-condition.md) | GET | Monitors an Airtop window for a condition. |
| [Prompt Content](actions/prompt-content.md) | GET | Queries Airtop window content from a prompt. Deprecated; use Query a Page instead. |
| [Query a Page](actions/query-page.md) | GET | Queries Airtop window content with a prompt. |
| [Query a Page With Pagination](actions/query-page-with-pagination.md) | GET | Queries Airtop window content with pagination. |
| [Scrape Content](actions/scrape-content.md) | GET | Scrapes content from an Airtop window. |
| [Scroll](actions/scroll.md) | PUT | Scrolls within a specific Airtop window. |
| [Summarize Content](actions/summarize-content.md) | GET | Summarizes Airtop window content. Deprecated; use Query a Page instead. |
| [Take Screenshot](actions/take-screenshot.md) | GET | Takes a screenshot of an Airtop window. |
| [Type](actions/type.md) | PUT | Types text in a specific Airtop window. |

