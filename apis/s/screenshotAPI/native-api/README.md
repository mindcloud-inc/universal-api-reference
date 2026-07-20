# ScreenshotAPI: Native API Reference

A consolidated summary of ScreenshotAPI's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://www.screenshotapi.net/docs/getStarted
- **API base URL:** `https://shot.screenshotapi.net/v3`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.screenshotapi.net/docs/getStarted)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Extract HTML](actions/extract-html.md) | `GET /screenshot` | [docs](https://www.screenshotapi.net/docs/renderScreenshot) |
| [Extract Text](actions/extract-text.md) | `GET /screenshot` | [docs](https://www.screenshotapi.net/docs/renderScreenshot) |
| [Generate PDF](actions/generate-pdf.md) | `GET /screenshot` | [docs](https://www.screenshotapi.net/docs/renderScreenshot) |
| [Record Multiple Scrolling Screenshots](actions/record-multiple-scrolling-screenshots.md) | `GET /screenshot` | [docs](https://www.screenshotapi.net/docs/scrollingScreenshot) |
| [Record Scrolling Screenshot](actions/record-scrolling-screenshot.md) | `GET /screenshot` | [docs](https://www.screenshotapi.net/docs/scrollingScreenshot) |
| [Render Custom HTML](actions/render-custom-html.md) | `GET /screenshot` | [docs](https://www.screenshotapi.net/docs/renderScreenshot) |
| [Render Screenshot](actions/render-screenshot.md) | `GET /screenshot` | [docs](https://www.screenshotapi.net/docs/renderScreenshot) |
| [Render Screenshot JSON](actions/render-screenshot-json.md) | `GET /screenshot` | [docs](https://www.screenshotapi.net/docs/renderScreenshot) |
