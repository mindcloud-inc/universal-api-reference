# Aquaforest PDF: Native API Reference

A consolidated summary of Aquaforest PDF's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/connectors/aquaforest/
- **OpenAPI specification:** https://raw.githubusercontent.com/microsoft/PowerPlatformConnectors/master/certified-connectors/Aquaforest%20PDF%20Connector/apiDefinition.swagger.json
- **API base URL:** `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`

## Authentication

### API Key

API key authentication for Aquaforest PDF API subscriptions.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Ocp-Apim-Subscription-Key: <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-us/connectors/aquaforest/#how-to-get-credentials)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Extract PDF pages by barcode](actions/extract-pdf-pages-by-barcode.md) | `POST /ExtractPageByBarcode` | [docs](https://learn.microsoft.com/en-us/connectors/aquaforest/#extract-pdf-pages-by-barcode) |
| [Extract PDF pages by text](actions/extract-pdf-pages-by-text.md) | `POST /ExtractPageByText` | [docs](https://learn.microsoft.com/en-us/connectors/aquaforest/#extract-pdf-pages-by-text) |
| [Get barcode value from PDF](actions/get-barcode-value-from-pdf.md) | `POST /GetBarcodeValue` | [docs](https://learn.microsoft.com/en-us/connectors/aquaforest/#get-barcode-value) |
| [Get data from PDF](actions/get-data-from-pdf.md) | `POST /GetPageData` | [docs](https://learn.microsoft.com/en-us/connectors/aquaforest/#get-data-from-pdf) |
| [Get PDF properties](actions/get-pdf-properties.md) | `POST /GetPDFInfo` | [docs](https://learn.microsoft.com/en-us/connectors/aquaforest/#get-pdf-properties) |
| [Get text from PDF](actions/get-text-from-pdf.md) | `POST /GetTextValue` | [docs](https://learn.microsoft.com/en-us/connectors/aquaforest/#get-text-from-pdf) |
| [OCR PDF or image to searchable PDF](actions/ocr-pdf-or-image-to-searchable-pdf.md) | `POST /OcrFile` | [docs](https://learn.microsoft.com/en-us/connectors/aquaforest/#ocr-pdf-or-images) |
| [Split PDF by barcode](actions/split-pdf-by-barcode.md) | `POST /SplitByBarcode` | [docs](https://learn.microsoft.com/en-us/connectors/aquaforest/#split-pdf-by-barcode) |
| [Split PDF by page](actions/split-pdf-by-page.md) | `POST /SplitPdfByPage` | [docs](https://learn.microsoft.com/en-us/connectors/aquaforest/#split-pdf-by-page) |
| [Split PDF by text match](actions/split-pdf-by-text-match.md) | `POST /SplitByText` | [docs](https://learn.microsoft.com/en-us/connectors/aquaforest/#split-pdf-by-text-match) |
