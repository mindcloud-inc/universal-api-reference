# Invoice.xhub: Native API Reference

A consolidated summary of Invoice.xhub's API configuration and 84 documented operations, with links to official documentation.

- **Official docs:** https://invoice-api.xhub.io/en/docs/api
- **OpenAPI specification:** https://service.invoice-api.xhub.io/openapi.json
- **API base URL:** `https://service.invoice-api.xhub.io`

## Authentication

### API Key

Use an Invoice.xhub API key with the provider's bearer Authorization header contract.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://invoice-api.xhub.io/en/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (84 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Auto-Detect and Parse Invoice](actions/auto-detect-and-parse-invoice.md) | `POST /api/v1/invoice/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Generate Austria ebInterface Invoice](actions/generate-austria-eb-interface-invoice.md) | `POST /api/v1/invoice/AT/EBINTERFACE/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Austria PDF Invoice](actions/generate-austria-pdf-invoice.md) | `POST /api/v1/invoice/AT/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Belgium PDF Invoice](actions/generate-belgium-pdf-invoice.md) | `POST /api/v1/invoice/BE/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Belgium UBL Invoice](actions/generate-belgium-ubl-invoice.md) | `POST /api/v1/invoice/BE/UBL/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Bulgaria PDF Invoice](actions/generate-bulgaria-pdf-invoice.md) | `POST /api/v1/invoice/BG/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Bulgaria UBL Invoice](actions/generate-bulgaria-ubl-invoice.md) | `POST /api/v1/invoice/BG/UBL/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Czech Republic ISDOC Invoice](actions/generate-czech-republic-isdoc-invoice.md) | `POST /api/v1/invoice/CZ/ISDOC/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Czech Republic PDF Invoice](actions/generate-czech-republic-pdf-invoice.md) | `POST /api/v1/invoice/CZ/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate France Factur-X Invoice](actions/generate-france-factur-x-invoice.md) | `POST /api/v1/invoice/FR/FACTURX/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate France PDF Invoice](actions/generate-france-pdf-invoice.md) | `POST /api/v1/invoice/FR/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Germany PDF Invoice](actions/generate-germany-pdf-invoice.md) | `POST /api/v1/invoice/DE/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Germany XRechnung Invoice](actions/generate-germany-x-rechnung-invoice.md) | `POST /api/v1/invoice/DE/XRECHNUNG/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Germany ZUGFeRD Invoice](actions/generate-germany-zug-fe-rd-invoice.md) | `POST /api/v1/invoice/DE/ZUGFERD/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Hungary NAV Invoice](actions/generate-hungary-nav-invoice.md) | `POST /api/v1/invoice/HU/NAV/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Hungary PDF Invoice](actions/generate-hungary-pdf-invoice.md) | `POST /api/v1/invoice/HU/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Italy FatturaPA Invoice](actions/generate-italy-fattura-pa-invoice.md) | `POST /api/v1/invoice/IT/FATTURAPA/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Italy PDF Invoice](actions/generate-italy-pdf-invoice.md) | `POST /api/v1/invoice/IT/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Netherlands PDF Invoice](actions/generate-netherlands-pdf-invoice.md) | `POST /api/v1/invoice/NL/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Netherlands UBL Invoice](actions/generate-netherlands-ubl-invoice.md) | `POST /api/v1/invoice/NL/UBL/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Poland PDF Invoice](actions/generate-poland-pdf-invoice.md) | `POST /api/v1/invoice/PL/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Portugal PDF Invoice](actions/generate-portugal-pdf-invoice.md) | `POST /api/v1/invoice/PT/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Romania PDF Invoice](actions/generate-romania-pdf-invoice.md) | `POST /api/v1/invoice/RO/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Romania UBL Invoice](actions/generate-romania-ubl-invoice.md) | `POST /api/v1/invoice/RO/UBL/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Spain Facturae Invoice](actions/generate-spain-facturae-invoice.md) | `POST /api/v1/invoice/ES/FACTURAE/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Spain PDF Invoice](actions/generate-spain-pdf-invoice.md) | `POST /api/v1/invoice/ES/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Switzerland PDF Invoice](actions/generate-switzerland-pdf-invoice.md) | `POST /api/v1/invoice/CH/pdf/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Generate Switzerland QR-Bill Invoice](actions/generate-switzerland-qr-bill-invoice.md) | `POST /api/v1/invoice/CH/QR-BILL/generate` | [docs](https://invoice-api.xhub.io/en/docs/api/creator) |
| [Get All Supported Formats](actions/get-all-supported-formats.md) | `GET /api/v1/invoice/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get Austria Formats](actions/get-austria-formats.md) | `GET /api/v1/invoice/AT/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get Belgium Formats](actions/get-belgium-formats.md) | `GET /api/v1/invoice/BE/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get Bulgaria Formats](actions/get-bulgaria-formats.md) | `GET /api/v1/invoice/BG/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get Czech Republic Formats](actions/get-czech-republic-formats.md) | `GET /api/v1/invoice/CZ/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get France Formats](actions/get-france-formats.md) | `GET /api/v1/invoice/FR/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get Germany Formats](actions/get-germany-formats.md) | `GET /api/v1/invoice/DE/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get Hungary Formats](actions/get-hungary-formats.md) | `GET /api/v1/invoice/HU/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get Italy Formats](actions/get-italy-formats.md) | `GET /api/v1/invoice/IT/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get Netherlands Formats](actions/get-netherlands-formats.md) | `GET /api/v1/invoice/NL/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get Poland Formats](actions/get-poland-formats.md) | `GET /api/v1/invoice/PL/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get Portugal Formats](actions/get-portugal-formats.md) | `GET /api/v1/invoice/PT/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get Romania Formats](actions/get-romania-formats.md) | `GET /api/v1/invoice/RO/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get Spain Formats](actions/get-spain-formats.md) | `GET /api/v1/invoice/ES/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Get Switzerland Formats](actions/get-switzerland-formats.md) | `GET /api/v1/invoice/CH/formats` | [docs](https://invoice-api.xhub.io/en/docs/api/formats) |
| [Parse Austria ebInterface Invoice](actions/parse-austria-eb-interface-invoice.md) | `POST /api/v1/invoice/AT/EBINTERFACE/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Austria PDF Invoice](actions/parse-austria-pdf-invoice.md) | `POST /api/v1/invoice/AT/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Belgium PDF Invoice](actions/parse-belgium-pdf-invoice.md) | `POST /api/v1/invoice/BE/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Belgium UBL Invoice](actions/parse-belgium-ubl-invoice.md) | `POST /api/v1/invoice/BE/UBL/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Bulgaria PDF Invoice](actions/parse-bulgaria-pdf-invoice.md) | `POST /api/v1/invoice/BG/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Bulgaria UBL Invoice](actions/parse-bulgaria-ubl-invoice.md) | `POST /api/v1/invoice/BG/UBL/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Czech Republic ISDOC Invoice](actions/parse-czech-republic-isdoc-invoice.md) | `POST /api/v1/invoice/CZ/ISDOC/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Czech Republic PDF Invoice](actions/parse-czech-republic-pdf-invoice.md) | `POST /api/v1/invoice/CZ/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse France Factur-X Invoice](actions/parse-france-factur-x-invoice.md) | `POST /api/v1/invoice/FR/FACTURX/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse France PDF Invoice](actions/parse-france-pdf-invoice.md) | `POST /api/v1/invoice/FR/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Germany PDF Invoice](actions/parse-germany-pdf-invoice.md) | `POST /api/v1/invoice/DE/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Germany XRechnung Invoice](actions/parse-germany-x-rechnung-invoice.md) | `POST /api/v1/invoice/DE/XRECHNUNG/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Germany ZUGFeRD Invoice](actions/parse-germany-zug-fe-rd-invoice.md) | `POST /api/v1/invoice/DE/ZUGFERD/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Hungary NAV Invoice](actions/parse-hungary-nav-invoice.md) | `POST /api/v1/invoice/HU/NAV/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Hungary PDF Invoice](actions/parse-hungary-pdf-invoice.md) | `POST /api/v1/invoice/HU/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Italy FatturaPA Invoice](actions/parse-italy-fattura-pa-invoice.md) | `POST /api/v1/invoice/IT/FATTURAPA/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Italy PDF Invoice](actions/parse-italy-pdf-invoice.md) | `POST /api/v1/invoice/IT/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Netherlands PDF Invoice](actions/parse-netherlands-pdf-invoice.md) | `POST /api/v1/invoice/NL/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Netherlands UBL Invoice](actions/parse-netherlands-ubl-invoice.md) | `POST /api/v1/invoice/NL/UBL/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Poland PDF Invoice](actions/parse-poland-pdf-invoice.md) | `POST /api/v1/invoice/PL/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Portugal PDF Invoice](actions/parse-portugal-pdf-invoice.md) | `POST /api/v1/invoice/PT/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Romania PDF Invoice](actions/parse-romania-pdf-invoice.md) | `POST /api/v1/invoice/RO/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Romania UBL Invoice](actions/parse-romania-ubl-invoice.md) | `POST /api/v1/invoice/RO/UBL/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Spain Facturae Invoice](actions/parse-spain-facturae-invoice.md) | `POST /api/v1/invoice/ES/FACTURAE/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Spain PDF Invoice](actions/parse-spain-pdf-invoice.md) | `POST /api/v1/invoice/ES/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Switzerland PDF Invoice](actions/parse-switzerland-pdf-invoice.md) | `POST /api/v1/invoice/CH/pdf/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Parse Switzerland QR-Bill Invoice](actions/parse-switzerland-qr-bill-invoice.md) | `POST /api/v1/invoice/CH/QR-BILL/parse` | [docs](https://invoice-api.xhub.io/en/docs/api/parser) |
| [Validate Austria Invoice](actions/validate-austria-invoice.md) | `POST /api/v1/invoice/AT/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
| [Validate Belgium Invoice](actions/validate-belgium-invoice.md) | `POST /api/v1/invoice/BE/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
| [Validate Bulgaria Invoice](actions/validate-bulgaria-invoice.md) | `POST /api/v1/invoice/BG/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
| [Validate Czech Republic Invoice](actions/validate-czech-republic-invoice.md) | `POST /api/v1/invoice/CZ/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
| [Validate France Invoice](actions/validate-france-invoice.md) | `POST /api/v1/invoice/FR/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
| [Validate Germany Invoice](actions/validate-germany-invoice.md) | `POST /api/v1/invoice/DE/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
| [Validate Hungary Invoice](actions/validate-hungary-invoice.md) | `POST /api/v1/invoice/HU/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
| [Validate Italy Invoice](actions/validate-italy-invoice.md) | `POST /api/v1/invoice/IT/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
| [Validate Netherlands Invoice](actions/validate-netherlands-invoice.md) | `POST /api/v1/invoice/NL/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
| [Validate Poland Invoice](actions/validate-poland-invoice.md) | `POST /api/v1/invoice/PL/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
| [Validate Portugal Invoice](actions/validate-portugal-invoice.md) | `POST /api/v1/invoice/PT/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
| [Validate Romania Invoice](actions/validate-romania-invoice.md) | `POST /api/v1/invoice/RO/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
| [Validate Spain Invoice](actions/validate-spain-invoice.md) | `POST /api/v1/invoice/ES/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
| [Validate Switzerland Invoice](actions/validate-switzerland-invoice.md) | `POST /api/v1/invoice/CH/validate` | [docs](https://invoice-api.xhub.io/en/docs/api/validator) |
