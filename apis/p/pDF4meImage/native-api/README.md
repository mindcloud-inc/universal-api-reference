# PDF4me Image: Native API Reference

A consolidated summary of PDF4me Image's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.pdf4me.com/power-automate/getting-started/
- **API base URL:** `https://api.pdf4me.com/api/v2`

## Authentication

### API Key

Connect PDF4me Image with your PDF4me API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.pdf4me.com/power-automate/authorization/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Image Metadata](actions/get-image-metadata.md) | `POST /GetImageMetadata` | [docs](https://docs.pdf4me.com/url-api-tester/get-image-metadata/) |
| [Read Barcode from Image](actions/read-barcode-from-image.md) | `POST /ReadBarcodesfromImage` | [docs](https://docs.pdf4me.com/url-api-tester/read-barcode-from-image/) |
