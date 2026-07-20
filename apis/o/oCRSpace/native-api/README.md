# OCRSpace: Native API Reference

A consolidated summary of OCRSpace's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://ocr.space/ocrapi
- **API base URL:** `https://api.ocr.space`

## Authentication

### API Key

Connect with your OCRSpace API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://ocr.space/ocrapi)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Searchable PDF From Base64](actions/create-searchable-pdf-from-base64.md) | `POST /parse/image` | [docs](https://ocr.space/ocrapi) |
| [Create Searchable PDF From File](actions/create-searchable-pdf-from-file.md) | `POST /parse/image` | [docs](https://ocr.space/ocrapi) |
| [Create Searchable PDF From URL](actions/create-searchable-pdf-from-url.md) | `POST /parse/image` | [docs](https://ocr.space/ocrapi) |
| [Detect Language From URL](actions/detect-language-from-url.md) | `POST /parse/image` | [docs](https://ocr.space/blog/ocr-api-language-autodetect/) |
| [Extract Tables From Base64](actions/extract-tables-from-base64.md) | `POST /parse/image` | [docs](https://ocr.space/receiptscanning) |
| [Extract Tables From File](actions/extract-tables-from-file.md) | `POST /parse/image` | [docs](https://ocr.space/receiptscanning) |
| [Extract Tables From URL](actions/extract-tables-from-url.md) | `POST /parse/image` | [docs](https://ocr.space/receiptscanning) |
| [Parse Base64 Document](actions/parse-base64-document.md) | `POST /parse/image` | [docs](https://ocr.space/ocrapi) |
| [Parse Base64 With Overlay](actions/parse-base64-with-overlay.md) | `POST /parse/image` | [docs](https://ocr.space/ocrapi) |
| [Parse Image URL](actions/parse-image-url.md) | `GET /parse/imageurl` | [docs](https://ocr.space/ocrapi) |
| [Parse Image URL With Overlay](actions/parse-image-url-with-overlay.md) | `GET /parse/imageurl` | [docs](https://ocr.space/ocrapi) |
| [Parse URL Securely](actions/parse-url-securely.md) | `POST /parse/image` | [docs](https://ocr.space/ocrapi) |
| [Recognize Layout From Base64](actions/recognize-layout-from-base64.md) | `POST /parse/image` | [docs](https://ocr.space/ocrapi) |
| [Recognize Layout From File](actions/recognize-layout-from-file.md) | `POST /parse/image` | [docs](https://ocr.space/tablerecognition) |
| [Recognize Layout From URL](actions/recognize-layout-from-url.md) | `POST /parse/image` | [docs](https://ocr.space/ocrapi) |
| [Upload File For OCR](actions/upload-file-for-ocr.md) | `POST /parse/image` | [docs](https://ocr.space/ocrapi) |
| [Upload File With Overlay](actions/upload-file-with-overlay.md) | `POST /parse/image` | [docs](https://ocr.space/ocrapi) |
