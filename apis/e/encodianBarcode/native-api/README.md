# Encodian - Barcode: Native API Reference

A consolidated summary of Encodian - Barcode's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://api.apps-encodian.com/swagger/Barcode/swagger.json
- **OpenAPI specification:** https://api.apps-encodian.com/swagger/Barcode/swagger.json
- **API base URL:** `https://api.apps-encodian.com`

## Authentication

### API Key

Authenticate requests to Encodian Flowr Barcode with the X-ApiKey header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-ApiKey: <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-us/connectors/encodianbarcode/#creating-a-connection)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Barcode - Create](actions/barcode-create.md) | `POST /api/v1/Barcodes/CreateBarcode` | [docs](https://support.encodian.com/hc/en-gb/articles/360006165457-Create-Barcode) |
| [Barcode - Read Document Status](actions/barcode-read-document-status.md) | `GET /api/v1/Barcodes/GetOperationStatusReadBarcodeFromDocument` | [docs](https://api.apps-encodian.com/swagger/Barcode/swagger.json) |
| [Barcode - Read from Document](actions/barcode-read-from-document.md) | `POST /api/v1/Barcodes/ReadBarcodeFromDocument` | [docs](https://support.encodian.com/hc/en-gb/articles/360006170938-Read-Barcode-Document) |
| [Barcode - Read from Image](actions/barcode-read-from-image.md) | `POST /api/v1/Barcodes/ReadBarcodeFromImage` | [docs](https://support.encodian.com/hc/en-gb/articles/360006170918-Read-Barcode-Image) |
| [QR Code - Create](actions/qr-code-create.md) | `POST /api/v1/Barcodes/CreateQrCode` | [docs](https://support.encodian.com/hc/en-gb/articles/360005178237-Create-QR-Code) |
| [QR Code - Read Document Status](actions/qr-code-read-document-status.md) | `GET /api/v1/Barcodes/GetOperationStatusReadQrCodeFromDocument` | [docs](https://api.apps-encodian.com/swagger/Barcode/swagger.json) |
| [QR Code - Read from Document](actions/qr-code-read-from-document.md) | `POST /api/v1/Barcodes/ReadQrCodeFromDocument` | [docs](https://support.encodian.com/hc/en-gb/articles/360006165437-Read-QR-Code-Document) |
| [QR Code - Read from Image](actions/qr-code-read-from-image.md) | `POST /api/v1/Barcodes/ReadQrCodeFromImage` | [docs](https://support.encodian.com/hc/en-gb/articles/360006170898-Read-QR-Code-Image) |
| [Swiss QR Code - Create](actions/swiss-qr-code-create.md) | `POST /api/v1/Barcodes/CreateSwissQrCode` | [docs](https://support.encodian.com/hc/en-gb/articles/22209145105052) |
| [Swiss QR Code - Read from Document](actions/swiss-qr-code-read-from-document.md) | `POST /api/v1/Barcodes/ReadSwissQrCodesFromDocument` | [docs](https://support.encodian.com/hc/en-gb/articles/23404516960668) |
| [Swiss QR Code - Read from Image](actions/swiss-qr-code-read-from-image.md) | `POST /api/v1/Barcodes/ReadSwissQrCodeFromImage` | [docs](https://support.encodian.com/hc/en-gb/articles/22624743460892) |
