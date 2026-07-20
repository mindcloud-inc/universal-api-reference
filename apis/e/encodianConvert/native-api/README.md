# Encodian - Convert: Native API Reference

A consolidated summary of Encodian - Convert's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://support.encodian.com/hc/en-gb/articles/22002408782108-Encodian-Convert-Connector
- **OpenAPI specification:** https://api.apps-encodian.com/swagger/Conversion/swagger.json
- **API base URL:** `https://api.apps-encodian.com`

## Authentication

### API Key

Authenticate Encodian Flowr Convert requests with an API key in the X-ApiKey header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-ApiKey: <apiKey>
```

[Official authentication documentation](https://support.encodian.com/hc/en-gb/articles/360012267353-Create-an-Encodian-Connection-in-Power-Automate)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get an Operation Status](actions/conversion-get-operation-status.md) | `GET /api/v1/Conversion/GetOperationStatus` | [docs](https://api.apps-encodian.com/swagger/Conversion/swagger.json) |
| [Convert - CAD](actions/convert-cad.md) | `POST /api/v1/Conversion/ConvertCad` | [docs](https://support.encodian.com/hc/en-gb/articles/4542607350417) |
| [Convert - Email](actions/convert-email.md) | `POST /api/v1/Conversion/ConvertMailMessage` | [docs](https://support.encodian.com/hc/en-gb/articles/360011566298-Convert-Email) |
| [Convert - Excel](actions/convert-excel.md) | `POST /api/v1/Conversion/ConvertExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/360011804178) |
| [Convert - File to PDF](actions/convert-file-to-pdf.md) | `POST /api/v1/Conversion/BasicConversion` | [docs](https://support.encodian.com/hc/en-gb/articles/360011123574-Convert-File-to-PDF) |
| [Convert - HEIC to PDF](actions/convert-heic-to-pdf.md) | `POST /api/v1/Conversion/ConvertHeicToPdf` | [docs](https://support.encodian.com/hc/en-gb/articles/18068082274716-Convert-HEIC-to-PDF) |
| [Convert - HTML to Image](actions/convert-html-to-image.md) | `POST /api/v1/Conversion/HtmlToImage` | [docs](https://support.encodian.com/hc/en-gb/articles/13961998920732) |
| [Convert - HTML to PDF](actions/convert-html-to-pdf.md) | `POST /api/v1/Conversion/HtmlToPDF` | [docs](https://support.encodian.com/hc/en-gb/articles/360022205154-Convert-HTML-to-PDF) |
| [Convert - HTML to PDF (V2)](actions/convert-html-to-pdf-v2.md) | `POST /api/v1/Conversion/HtmlToPDFV2` | [docs](https://support.encodian.com/hc/en-gb/articles/16421778005020) |
| [Convert - HTML to Word](actions/convert-html-to-word.md) | `POST /api/v1/Conversion/HtmlToWord` | [docs](https://support.encodian.com/hc/en-gb/articles/360011823213) |
| [Convert - Image to PDF](actions/convert-image-to-pdf.md) | `POST /api/v1/Conversion/ConvertImageToPdf` | [docs](https://support.encodian.com/hc/en-gb/articles/23601928355228) |
| [Convert - JSON to Excel](actions/convert-json-to-excel.md) | `POST /api/v1/Conversion/ConvertJsonToExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/7690520790045) |
| [Convert - PDF to Excel](actions/convert-pdf-to-excel.md) | `POST /api/v1/Conversion/ConvertPdfToExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/17011591184284) |
| [Convert - PDF to Images](actions/convert-pdf-to-images.md) | `POST /api/v1/Conversion/ConvertPdfToImages` | [docs](https://support.encodian.com/hc/en-gb/articles/4418101623441) |
| [Convert - PDF to JPG](actions/convert-pdf-to-jpg.md) | `POST /api/v1/Conversion/ConvertPdfToJpg` | [docs](https://support.encodian.com/hc/en-gb/articles/11096881397277) |
| [Convert - PDF to PDFA](actions/convert-pdf-to-pdfa.md) | `POST /api/v1/Conversion/ConvertToPdfA` | [docs](https://support.encodian.com/hc/en-gb/articles/360010578413) |
| [Convert - PDF to PNG](actions/convert-pdf-to-png.md) | `POST /api/v1/Conversion/ConvertPdfToPng` | [docs](https://support.encodian.com/hc/en-gb/articles/10086003836701) |
| [Convert - PDF to TIFF](actions/convert-pdf-to-tiff.md) | `POST /api/v1/Conversion/ConvertPdfToTiff` | [docs](https://support.encodian.com/hc/en-gb/articles/4418024925457) |
| [Convert - PDF to Word](actions/convert-pdf-to-word.md) | `POST /api/v1/Conversion/ConvertPdfToWord` | [docs](https://support.encodian.com/hc/en-gb/articles/360027229294) |
| [Convert - PowerPoint](actions/convert-power-point.md) | `POST /api/v1/Conversion/ConvertPowerPoint` | [docs](https://support.encodian.com/hc/en-gb/articles/360015879777) |
| [Convert - Text to PDF](actions/convert-text-to-pdf.md) | `POST /api/v1/Conversion/TextToPDF` | [docs](https://support.encodian.com/hc/en-gb/articles/360011683054-Convert-Text-to-PDF) |
| [Convert - Visio](actions/convert-visio.md) | `POST /api/v1/Conversion/ConvertVisio` | [docs](https://support.encodian.com/hc/en-gb/articles/5306216347665) |
| [Convert - Word](actions/convert-word.md) | `POST /api/v1/Conversion/ConvertWord` | [docs](https://support.encodian.com/hc/en-gb/articles/360015616117-Convert-Word) |
| [Convert - Word to PDF Form](actions/convert-word-to-pdf-form.md) | `POST /api/v1/Conversion/WordToPdfForm` | [docs](https://support.encodian.com/hc/en-gb/articles/360012307133) |
