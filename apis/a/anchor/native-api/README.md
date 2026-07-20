# Anchor: Native API Reference

A consolidated summary of Anchor's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.anchorbrowser.io
- **OpenAPI specification:** https://docs.anchorbrowser.io/openapi.yaml
- **API base URL:** `https://api.anchorbrowser.io`

## Authentication

### API Key

Connect with an Anchor Browser API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
anchor-api-key: <apiKey>
```

[Official authentication documentation](https://docs.anchorbrowser.io/quickstart/use-via-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Profile](actions/create-profile.md) | `POST /v1/profiles` | [docs](https://docs.anchorbrowser.io/api-reference/profiles/create-profile) |
| [Delete Profile](actions/delete-profile.md) | `DELETE /v1/profiles/:name` | [docs](https://docs.anchorbrowser.io/api-reference/profiles/delete-profile) |
| [End Browser Session](actions/end-browser-session.md) | `DELETE /v1/sessions/:sessionId` | [docs](https://docs.anchorbrowser.io/api-reference/browser-sessions/end-browser-session) |
| [Get Browser Session](actions/get-browser-session.md) | `GET /v1/sessions/:sessionId` | [docs](https://docs.anchorbrowser.io/api-reference/browser-sessions/get-browser-session) |
| [Get Browser Session Pages](actions/get-browser-session-pages.md) | `GET /v1/sessions/:sessionId/pages` | [docs](https://docs.anchorbrowser.io/api-reference/browser-sessions/get-browser-session-pages) |
| [Get Page PDF](actions/get-page-pdf.md) | `POST /v1/tools/page-pdf` | [docs](https://docs.anchorbrowser.io/api-reference/tools/get-page-pdf) |
| [Get Profile](actions/get-profile.md) | `GET /v1/profiles/:name` | [docs](https://docs.anchorbrowser.io/api-reference/profiles/get-profile) |
| [Get Task Run Status](actions/get-task-run-status.md) | `GET /v2/tasks/runs/:runId/status` | [docs](https://docs.anchorbrowser.io/api-reference/tasks/get-task-run-status) |
| [Get Web Task Status](actions/get-web-task-status.md) | `GET /v1/tools/perform-web-task/:workflowId/status` | [docs](https://docs.anchorbrowser.io/api-reference/ai-tools/get-perform-web-task-status) |
| [Get Webpage Content](actions/get-webpage-content.md) | `POST /v1/tools/fetch-webpage` | [docs](https://docs.anchorbrowser.io/api-reference/tools/get-webpage-content) |
| [Keyboard Shortcut](actions/keyboard-shortcut.md) | `POST /v1/sessions/:sessionId/keyboard/shortcut` | [docs](https://docs.anchorbrowser.io/api-reference/os-level-control/keyboard-shortcut) |
| [List Browser Sessions](actions/list-browser-sessions.md) | `GET /v1/sessions` | [docs](https://docs.anchorbrowser.io/api-reference/browser-sessions/list-sessions-history-page) |
| [List Profiles](actions/list-profiles.md) | `GET /v1/profiles` | [docs](https://docs.anchorbrowser.io/api-reference/profiles/list-profiles) |
| [List Session Downloads](actions/list-session-downloads.md) | `GET /v1/sessions/:sessionId/downloads` | [docs](https://docs.anchorbrowser.io/api-reference/browser-sessions/list-session-downloads) |
| [Mouse Click](actions/mouse-click.md) | `POST /v1/sessions/:sessionId/mouse/click` | [docs](https://docs.anchorbrowser.io/api-reference/os-level-control/mouse-click) |
| [Navigate to URL](actions/navigate-to-url.md) | `POST /v1/sessions/:sessionId/goto` | [docs](https://docs.anchorbrowser.io/api-reference/os-level-control/navigate-to-url) |
| [Perform Web Task](actions/perform-web-task.md) | `POST /v1/tools/perform-web-task` | [docs](https://docs.anchorbrowser.io/api-reference/ai-tools/perform-web-task) |
| [Run Task](actions/run-task.md) | `POST /v2/tasks/:taskId/run` | [docs](https://docs.anchorbrowser.io/api-reference/tasks/run-a-task) |
| [Screenshot Webpage](actions/screenshot-webpage.md) | `POST /v1/tools/screenshot` | [docs](https://docs.anchorbrowser.io/api-reference/tools/screenshot-webpage) |
| [Start Browser Session](actions/start-browser-session.md) | `POST /v1/sessions` | [docs](https://docs.anchorbrowser.io/api-reference/browser-sessions/start-browser-session) |
| [Take Session Screenshot](actions/take-session-screenshot.md) | `GET /v1/sessions/:sessionId/screenshot` | [docs](https://docs.anchorbrowser.io/api-reference/os-level-control/take-screenshot) |
| [Type Text](actions/type-text.md) | `POST /v1/sessions/:sessionId/keyboard/type` | [docs](https://docs.anchorbrowser.io/api-reference/os-level-control/type-text) |
| [Upload Files](actions/upload-files.md) | `POST /v1/sessions/:sessionId/uploads` | [docs](https://docs.anchorbrowser.io/api-reference/browser-sessions/upload-files) |
| [Web Unlocker](actions/web-unlocker.md) | `POST /v1/tools/fetch/webpage` | [docs](https://docs.anchorbrowser.io/api-reference/tools/web-unlocker) |
