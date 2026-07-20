# Airtop: Native API Reference

A consolidated summary of Airtop's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.airtop.ai/api-reference/airtop-api
- **API base URL:** `https://api.airtop.ai/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.airtop.ai/guides/getting-started/quick-start)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Click](actions/click.md) | `POST /sessions/:sessionId/windows/:windowId/click` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/click) |
| [Create File](actions/create-file.md) | `POST /files` | [docs](https://docs.airtop.ai/api-reference/airtop-api/files/create) |
| [Create Form Filler Automation](actions/create-form-filler-automation.md) | `POST /sessions/:sessionId/windows/:windowId/create-form-filler` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/create-form-filler) |
| [Create Session](actions/create-session.md) | `POST /sessions` | [docs](https://docs.airtop.ai/api-reference/airtop-api/sessions/create) |
| [Create Window](actions/create-window.md) | `POST /sessions/:sessionId/windows` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/create) |
| [File Input](actions/file-input.md) | `POST /sessions/:sessionId/windows/:windowId/file-input` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/file-input) |
| [Fill Form With Automation](actions/fill-form-with-automation.md) | `POST /sessions/:sessionId/windows/:windowId/fill-form` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/fill-form) |
| [Get Session Info](actions/get-session-info.md) | `GET /sessions/:sessionId` | [docs](https://docs.airtop.ai/api-reference/airtop-api/sessions/get-info) |
| [Get Window Info](actions/get-window-info.md) | `GET /sessions/:sessionId/windows/:windowId` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/get-window-info) |
| [List Sessions](actions/list-sessions.md) | `GET /sessions` | [docs](https://docs.airtop.ai/api-reference/airtop-api/sessions/list) |
| [List Windows](actions/list-windows.md) | `GET /sessions/:sessionId/windows` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/list) |
| [Load URL](actions/load-url.md) | `POST /sessions/:sessionId/windows/:windowId` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/load-url) |
| [Monitor For Condition](actions/monitor-for-condition.md) | `POST /sessions/:sessionId/windows/:windowId/monitor` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/monitor) |
| [Prompt Content](actions/prompt-content.md) | `POST /sessions/:sessionId/windows/:windowId/prompt-content` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/prompt-content) |
| [Push File To Session](actions/push-file-to-session.md) | `POST /files/:fileId/push` | [docs](https://docs.airtop.ai/api-reference/airtop-api/files/push) |
| [Query a Page](actions/query-page.md) | `POST /sessions/:sessionId/windows/:windowId/page-query` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/page-query) |
| [Query a Page With Pagination](actions/query-page-with-pagination.md) | `POST /sessions/:sessionId/windows/:windowId/paginated-extraction` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/paginated-extraction) |
| [Save Profile On Termination](actions/save-profile-on-termination.md) | `PUT /sessions/:sessionId/save-profile-on-termination/:profileName` | [docs](https://docs.airtop.ai/api-reference/airtop-api/sessions/save-profile-on-termination) |
| [Scrape Content](actions/scrape-content.md) | `POST /sessions/:sessionId/windows/:windowId/scrape-content` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/scrape-content) |
| [Scroll](actions/scroll.md) | `POST /sessions/:sessionId/windows/:windowId/scroll` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/scroll) |
| [Summarize Content](actions/summarize-content.md) | `POST /sessions/:sessionId/windows/:windowId/summarize-content` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/summarize-content) |
| [Take Screenshot](actions/take-screenshot.md) | `POST /sessions/:sessionId/windows/:windowId/screenshot` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/screenshot) |
| [Terminate Session](actions/terminate-session.md) | `DELETE /sessions/:sessionId` | [docs](https://docs.airtop.ai/api-reference/airtop-api/sessions/terminate) |
| [Type](actions/type.md) | `POST /sessions/:sessionId/windows/:windowId/type` | [docs](https://docs.airtop.ai/api-reference/airtop-api/windows/type) |
