# Bitskout: Native API Reference

A consolidated summary of Bitskout's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/connectors/bitskout/
- **OpenAPI specification:** https://raw.githubusercontent.com/microsoft/PowerPlatformConnectors/dev/certified-connectors/bitskout/apiDefinition.swagger.json
- **API base URL:** `https://api.bitskout.com/v2`

## Authentication

### API Key

Use a Bitskout API token generated from Tokens and Passwords.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-us/connectors/bitskout/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Detect Document Type](actions/detect-document-type.md) | `POST /actions/doctype_:doctype` | [docs](https://learn.microsoft.com/en-us/connectors/bitskout/) |
| [Detect Response to Cold Email](actions/detect-response-to-cold-email.md) | `POST /actions/cold_response` | [docs](https://learn.microsoft.com/en-us/connectors/bitskout/) |
| [Extract Barcode from File](actions/extract-barcode-from-file.md) | `POST /actions/barcodes` | [docs](https://learn.microsoft.com/en-us/connectors/bitskout/) |
| [Extract Data from Bill of Lading](actions/extract-data-from-bill-of-lading.md) | `POST /actions/bill_of_lading` | [docs](https://learn.microsoft.com/en-us/connectors/bitskout/) |
| [Extract Data from Business Cards](actions/extract-data-from-business-cards.md) | `POST /actions/business_cards` | [docs](https://learn.microsoft.com/en-us/connectors/bitskout/) |
| [Extract Data from CV](actions/extract-data-from-cv.md) | `POST /actions/cv` | [docs](https://learn.microsoft.com/en-us/connectors/bitskout/) |
| [Extract Data from HARO Query](actions/extract-data-from-haro-query.md) | `POST /actions/haro` | [docs](https://learn.microsoft.com/en-us/connectors/bitskout/) |
| [Extract Data from Invoice](actions/extract-data-from-invoice.md) | `POST /actions/invoices` | [docs](https://learn.microsoft.com/en-us/connectors/bitskout/) |
| [Extract Data from Purchase Order](actions/extract-data-from-purchase-order.md) | `POST /actions/purchase_order` | [docs](https://learn.microsoft.com/en-us/connectors/bitskout/) |
| [Extract QR Code from Document](actions/extract-qr-code-from-document.md) | `POST /actions/qrcodes` | [docs](https://learn.microsoft.com/en-us/connectors/bitskout/) |
| [List Plugins](actions/list-plugins.md) | `GET /powerauto/plugins` | [docs](https://learn.microsoft.com/en-us/connectors/bitskout/) |
| [Run Plugin for File](actions/run-plugin-for-file.md) | `POST /powerauto/run_file` | [docs](https://learn.microsoft.com/en-us/connectors/bitskout/) |
| [Run Plugin for Text](actions/run-plugin-for-text.md) | `POST /powerauto/run_text` | [docs](https://learn.microsoft.com/en-us/connectors/bitskout/) |
