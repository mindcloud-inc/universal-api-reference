# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-21-as-13_1776790398752.png" alt="Cloudflare Browser Run logo" width="28" height="28"> Cloudflare Browser Run: Universal API

Cloudflare Browser Run, formerly Browser Rendering, runs headless Chrome on Cloudflare's global network for Quick Actions, browser sessions, screenshots, PDFs, markdown extraction, crawling, and DevTools automation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudflareBrowserRun/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cloudflare.com/
- **Vendor API docs:** https://developers.cloudflare.com/browser-rendering/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify API Token](actions/verify-api-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/verify-api-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Verify API Token](actions/verify-api-token.md) | GET | Verifies whether a Cloudflare API token works. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get HTML Content](actions/get-html-content.md) | GET | Retrieves rendered HTML from Cloudflare Browser Run. |
| [Get JSON](actions/get-json.md) | GET | Retrieves structured JSON from Cloudflare Browser Run. |
| [Get Links](actions/get-links.md) | GET | Retrieves webpage links from Cloudflare Browser Run. |
| [Get Markdown](actions/get-markdown.md) | GET | Retrieves webpage Markdown from Cloudflare Browser Run. |
| [Get Snapshot](actions/get-snapshot.md) | GET | Retrieves a DOM snapshot from Cloudflare Browser Run. |
| [Scrape Elements](actions/scrape-elements.md) | GET | Extracts page elements from Cloudflare Browser Run. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get PDF](actions/get-pdf.md) | GET | Generates a webpage PDF in Cloudflare Browser Run. |
| [Get Screenshot](actions/get-screenshot.md) | GET | Captures a webpage screenshot in Cloudflare Browser Run. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Crawl Job](actions/cancel-crawl-job.md) | DELETE | Cancels a crawl job in Cloudflare Browser Run. |
| [Create Crawl Job](actions/create-crawl-job.md) | POST | Creates a crawl job in Cloudflare Browser Run. |
| [Get Crawl Result](actions/get-crawl-result.md) | GET | Retrieves crawl job results from Cloudflare Browser Run. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Activate Browser Target](actions/activate-browser-target.md) | PUT | Activates a browser target in Cloudflare Browser Run. |
| [Connect DevTools Page](actions/connect-devtools-page.md) | GET | Retrieves DevTools page connection details from Cloudflare Browser Run. |
| [Get Browser Target](actions/get-browser-target.md) | GET | Retrieves browser target details from Cloudflare Browser Run. |
| [List Browser Targets](actions/list-browser-targets.md) | GET | Lists browser targets in Cloudflare Browser Run. |
| [Open Browser Tab](actions/open-browser-tab.md) | POST | Opens a new browser tab in Cloudflare Browser Run. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Acquire Browser Session](actions/acquire-browser-session.md) | GET | Retrieves an available browser session from Cloudflare Browser Run. |
| [Close Browser Session](actions/close-browser-session.md) | DELETE | Closes a browser session in Cloudflare Browser Run. |
| [Connect Browser Session](actions/connect-browser-session.md) | GET | Retrieves browser session connection details from Cloudflare Browser Run. |
| [Create Browser Session](actions/create-browser-session.md) | POST | Creates a browser session in Cloudflare Browser Run. |
| [Get Browser Session Details](actions/get-browser-session-details.md) | GET | Retrieves browser session details from Cloudflare Browser Run. |
| [Get Browser Version](actions/get-browser-version.md) | GET | Retrieves browser version details from Cloudflare Browser Run. |
| [List Browser Sessions](actions/list-browser-sessions.md) | GET | Lists browser sessions in Cloudflare Browser Run. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get DevTools Protocol Schema](actions/get-devtools-protocol-schema.md) | GET | Retrieves the DevTools protocol schema from Cloudflare Browser Run. |

