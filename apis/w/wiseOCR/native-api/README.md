# WiseOCR: Native API Reference

A consolidated summary of WiseOCR's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://developers.wiseocr.com
- **API base URL:** `https://api.wiseocr.com/v1`

## Authentication

### API Key

Connect with your WiseOCR API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.wiseocr.com/basics)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Extract Receipt Data From File](actions/extract-receipt-data-from-file.md) | `POST /file` | [docs](https://developers.wiseocr.com/file-data-extraction) |
| [Extract Receipt Data From Text](actions/extract-receipt-data-from-text.md) | `POST /text` | [docs](https://developers.wiseocr.com/text-data-extraction) |
| [Extract Receipt Data From URL](actions/extract-receipt-data-from-url.md) | `POST /url` | [docs](https://developers.wiseocr.com/url-data-extraction) |
