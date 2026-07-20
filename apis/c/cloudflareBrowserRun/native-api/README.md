# Cloudflare Browser Run: Native API Reference

A consolidated summary of Cloudflare Browser Run's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://developers.cloudflare.com/browser-rendering/
- **API base URL:** `https://api.cloudflare.com/client/v4`

## Authentication

### API Token

Use a Cloudflare API token. Browser Run REST calls send the token as Authorization: Bearer <API_TOKEN>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.cloudflare.com/fundamentals/api/get-started/create-token/)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Cloudflare account ID. Browser Run REST endpoints are account-scoped. |

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Acquire Browser Session](actions/acquire-browser-session.md) | `GET /accounts/:accountId/browser-rendering/devtools/browser` | [docs](https://developers.cloudflare.com/api/resources/browser_rendering/) |
| [Activate Browser Target](actions/activate-browser-target.md) | `GET /accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/activate/:targetId` | [docs](https://developers.cloudflare.com/api/resources/browser_rendering/) |
| [Cancel Crawl Job](actions/cancel-crawl-job.md) | `DELETE /accounts/:accountId/browser-rendering/crawl/:jobId` | [docs](https://developers.cloudflare.com/browser-rendering/rest-api/crawl-endpoint/) |
| [Close Browser Session](actions/close-browser-session.md) | `DELETE /accounts/:accountId/browser-rendering/devtools/browser/:sessionId` | [docs](https://developers.cloudflare.com/api/resources/browser_rendering/) |
| [Connect Browser Session](actions/connect-browser-session.md) | `GET /accounts/:accountId/browser-rendering/devtools/browser/:sessionId` | [docs](https://developers.cloudflare.com/api/resources/browser_rendering/) |
| [Connect DevTools Page](actions/connect-devtools-page.md) | `GET /accounts/:accountId/browser-rendering/devtools/browser/:sessionId/page/:targetId` | [docs](https://developers.cloudflare.com/api/resources/browser_rendering/) |
| [Create Browser Session](actions/create-browser-session.md) | `POST /accounts/:accountId/browser-rendering/devtools/browser` | [docs](https://developers.cloudflare.com/api/resources/browser_rendering/) |
| [Create Crawl Job](actions/create-crawl-job.md) | `POST /accounts/:accountId/browser-rendering/crawl` | [docs](https://developers.cloudflare.com/browser-rendering/rest-api/crawl-endpoint/) |
| [Get Browser Session Details](actions/get-browser-session-details.md) | `GET /accounts/:accountId/browser-rendering/devtools/session/:sessionId` | [docs](https://developers.cloudflare.com/api/resources/browser_rendering/) |
| [Get Browser Target](actions/get-browser-target.md) | `GET /accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/list/:targetId` | [docs](https://developers.cloudflare.com/api/resources/browser_rendering/) |
| [Get Browser Version](actions/get-browser-version.md) | `GET /accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/version` | [docs](https://developers.cloudflare.com/api/resources/browser_rendering/) |
| [Get Crawl Result](actions/get-crawl-result.md) | `GET /accounts/:accountId/browser-rendering/crawl/:jobId` | [docs](https://developers.cloudflare.com/browser-rendering/rest-api/crawl-endpoint/) |
| [Get DevTools Protocol Schema](actions/get-devtools-protocol-schema.md) | `GET /accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/protocol` | [docs](https://developers.cloudflare.com/api/resources/browser_rendering/) |
| [Get HTML Content](actions/get-html-content.md) | `POST /accounts/:accountId/browser-rendering/content` | [docs](https://developers.cloudflare.com/browser-rendering/rest-api/content-endpoint/) |
| [Get JSON](actions/get-json.md) | `POST /accounts/:accountId/browser-rendering/json` | [docs](https://developers.cloudflare.com/browser-rendering/rest-api/json-endpoint/) |
| [Get Links](actions/get-links.md) | `POST /accounts/:accountId/browser-rendering/links` | [docs](https://developers.cloudflare.com/browser-rendering/rest-api/links-endpoint/) |
| [Get Markdown](actions/get-markdown.md) | `POST /accounts/:accountId/browser-rendering/markdown` | [docs](https://developers.cloudflare.com/browser-rendering/rest-api/markdown-endpoint/) |
| [Get PDF](actions/get-pdf.md) | `POST /accounts/:accountId/browser-rendering/pdf` | [docs](https://developers.cloudflare.com/browser-rendering/rest-api/pdf-endpoint/) |
| [Get Screenshot](actions/get-screenshot.md) | `POST /accounts/:accountId/browser-rendering/screenshot` | [docs](https://developers.cloudflare.com/browser-rendering/rest-api/screenshot-endpoint/) |
| [Get Snapshot](actions/get-snapshot.md) | `POST /accounts/:accountId/browser-rendering/snapshot` | [docs](https://developers.cloudflare.com/browser-rendering/rest-api/snapshot-endpoint/) |
| [List Browser Sessions](actions/list-browser-sessions.md) | `GET /accounts/:accountId/browser-rendering/devtools/session` | [docs](https://developers.cloudflare.com/api/resources/browser_rendering/) |
| [List Browser Targets](actions/list-browser-targets.md) | `GET /accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/list` | [docs](https://developers.cloudflare.com/api/resources/browser_rendering/) |
| [Open Browser Tab](actions/open-browser-tab.md) | `PUT /accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/new` | [docs](https://developers.cloudflare.com/api/resources/browser_rendering/) |
| [Scrape Elements](actions/scrape-elements.md) | `POST /accounts/:accountId/browser-rendering/scrape` | [docs](https://developers.cloudflare.com/browser-rendering/rest-api/scrape-endpoint/) |
| [Verify API Token](actions/verify-api-token.md) | `GET /accounts/:accountId/tokens/verify` | [docs](https://developers.cloudflare.com/api/resources/accounts/subresources/tokens/methods/verify/) |
