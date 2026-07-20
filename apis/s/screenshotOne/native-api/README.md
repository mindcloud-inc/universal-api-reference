# ScreenshotOne: Native API Reference

A consolidated summary of ScreenshotOne's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://screenshotone.com/docs/getting-started/
- **API base URL:** `https://api.screenshotone.com`

## Authentication

### API Key

Authenticate with a ScreenshotOne access key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://screenshotone.com/docs/getting-started/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Capture Selector Screenshot](actions/capture-selector-screenshot.md) | `GET /take` | [docs](https://screenshotone.com/docs/options/#selector) |
| [Extract Open Graph Metadata](actions/extract-open-graph-metadata.md) | `GET /take` | [docs](https://screenshotone.com/docs/options/#metadata_open_graph) |
| [Extract Page Content](actions/extract-page-content.md) | `GET /take` | [docs](https://screenshotone.com/docs/options/#metadata_content) |
| [Generate PDF](actions/generate-pdf.md) | `GET /take` | [docs](https://screenshotone.com/docs/options/#pdf-rendering) |
| [Get Usage](actions/get-usage.md) | `GET /usage` | [docs](https://screenshotone.com/docs/get-usage/) |
| [List Devices](actions/list-devices.md) | `GET /devices` | [docs](https://screenshotone.com/docs/viewport-devices/) |
| [Render HTML](actions/render-html.md) | `GET /take` | [docs](https://screenshotone.com/docs/options/#html) |
| [Render Markdown](actions/render-markdown.md) | `GET /take` | [docs](https://screenshotone.com/docs/options/#markdown) |
| [Store Rendered Asset](actions/store-rendered-asset.md) | `GET /take` | [docs](https://screenshotone.com/docs/options/#store) |
| [Take Full-Page Screenshot](actions/take-full-page-screenshot.md) | `GET /take` | [docs](https://screenshotone.com/docs/options/#full-page) |
| [Take Screenshot](actions/take-screenshot.md) | `GET /take` | [docs](https://screenshotone.com/docs/getting-started/) |
