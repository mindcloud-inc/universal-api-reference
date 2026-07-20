# CustomJS: Native API Reference

A consolidated summary of CustomJS's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://www.customjs.space/integration/native-api/documentation/
- **REST API base URL:** `https://e.customjs.io`
- **REST API base URL:** `https://api.app.customjs.io`

## Authentication

### API Key

Authenticate with your CustomJS API key from the dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://www.customjs.space/integration/native-api/api-key/)

## API conventions

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Capture Screenshot](actions/capture-screenshot.md) | `POST https://e.customjs.io/screenshot` | [docs](https://www.customjs.space/integration/native-api/documentation/) |
| [Compress PDF](actions/compress-pdf.md) | `POST https://e.customjs.io/__js1-` | [docs](https://www.customjs.space/integration/pdf-api/compress-pdf/) |
| [Convert HTML to PDF](actions/convert-html-to-pdf.md) | `POST https://e.customjs.io/html2pdf` | [docs](https://www.customjs.space/integration/pdf-api/html-to-pdf/) |
| [Convert HTML to PNG](actions/convert-html-to-png.md) | `POST https://e.customjs.io/__js1-` | [docs](https://www.customjs.space/api/docs/) |
| [Convert Markdown to PDF](actions/convert-markdown-to-pdf.md) | `POST https://e.customjs.io/markdown2pdf` | [docs](https://www.customjs.space/integration/native-api/documentation/) |
| [Convert PDF to PNG](actions/convert-pdf-to-png.md) | `POST https://e.customjs.io/__js1-` | [docs](https://www.customjs.space/integration/pdf-api/pdf-to-png/) |
| [Convert PDF to Text](actions/convert-pdf-to-text.md) | `POST https://e.customjs.io/__js1-` | [docs](https://www.customjs.space/integration/pdf-api/pdf-to-text/) |
| [Execute Custom JavaScript](actions/execute-custom-java-script.md) | `POST https://e.customjs.io/__js1-` | [docs](https://www.customjs.space/integration/native-api/documentation/) |
| [Extract Pages from PDF](actions/extract-pages-from-pdf.md) | `POST https://e.customjs.io/__js1-` | [docs](https://www.customjs.space/integration/pdf-api/extract-pages-from-pdf/) |
| [List HTML Pages](actions/list-html-pages.md) | `GET https://api.app.customjs.io/pages/api/page` | [docs](https://www.customjs.space/integration/native-api/documentation/) |
| [Merge PDFs](actions/merge-pdfs.md) | `POST https://e.customjs.io/__js1-` | [docs](https://www.customjs.space/integration/pdf-api/merge-pdfs/) |
| [Scrape HTML](actions/scrape-html.md) | `POST https://e.customjs.io/scraper` | [docs](https://www.customjs.space/integration/native-api/html-scraper/) |
