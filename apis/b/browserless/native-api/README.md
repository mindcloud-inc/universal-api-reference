# Browserless: Native API Reference

A consolidated summary of Browserless's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://docs.browserless.io/rest-apis/intro
- **OpenAPI specification:** https://docs.browserless.io/redocusaurus/plugin-redoc-0.yaml
- **API base URL:** `https://production-sfo.browserless.io`

## Authentication

### API Token

Connect with your Browserless API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.browserless.io/overview/connection-urls)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Capture Screenshot](actions/capture-screenshot.md) | `POST /screenshot` | [docs](https://docs.browserless.io/rest-apis/screenshot-api) |
| [Download File](actions/download-file.md) | `POST /download` | [docs](https://docs.browserless.io/rest-apis/download) |
| [Export Url](actions/export-url.md) | `POST /export` | [docs](https://docs.browserless.io/rest-apis/export) |
| [Generate Pdf](actions/generate-pdf.md) | `POST /pdf` | [docs](https://docs.browserless.io/rest-apis/pdf-api) |
| [Get Page Content](actions/get-page-content.md) | `POST /content` | [docs](https://docs.browserless.io/rest-apis/content) |
| [Map Site Links](actions/map-site-links.md) | `POST /map` | [docs](https://docs.browserless.io/rest-apis/map) |
| [Run Browser Function](actions/run-browser-function.md) | `POST /function` | [docs](https://docs.browserless.io/rest-apis/function) |
| [Run Performance Audit](actions/run-performance-audit.md) | `POST /performance` | [docs](https://docs.browserless.io/rest-apis/performance) |
| [Scrape Page Data](actions/scrape-page-data.md) | `POST /scrape` | [docs](https://docs.browserless.io/rest-apis/scrape) |
| [Search Web](actions/search-web.md) | `POST /search` | [docs](https://docs.browserless.io/rest-apis/search) |
| [Smart Scrape Url](actions/smart-scrape-url.md) | `POST /smart-scrape` | [docs](https://docs.browserless.io/rest-apis/smart-scrape) |
| [Unblock Url](actions/unblock-url.md) | `POST /unblock` | [docs](https://docs.browserless.io/rest-apis/unblock) |
