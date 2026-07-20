# Nutrient Document Web Services: Native API Reference

A consolidated summary of Nutrient Document Web Services's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://www.nutrient.io/api/reference/public/
- **OpenAPI specification:** https://dashboard.nutrient.io/assets/specs/public@1.15.0-3df32e4a530b7714d7d35607cea57089.yml?vsn=d
- **API base URL:** `https://api.nutrient.io`

## Authentication

### API Key

Nutrient DWS bearer API key authentication

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.nutrient.io/guides/dws-processor/developer-guides/authentication/)

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Watermark](actions/add-watermark.md) | `POST /processor/watermark` | [docs](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/processor-watermark) |
| [AI Redact Sensitive Information](actions/ai-redact-sensitive-information.md) | `POST /ai/redact` | [docs](https://www.nutrient.io/api/reference/public/#tag/AI/operation/ai-redact) |
| [Analyze Build Request](actions/analyze-build-request.md) | `POST /analyze_build` | [docs](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/analyze_build) |
| [Build Document](actions/build-document.md) | `POST /build` | [docs](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/build-document) |
| [Convert HTML to PDF](actions/convert-html-to-pdf.md) | `POST /processor/generate_pdf` | [docs](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/processor-generate-pdf) |
| [Convert to PDF](actions/convert-to-pdf.md) | `POST /processor/convert_to_pdf` | [docs](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/processor-convert-to-pdf) |
| [Digitally Sign PDF](actions/digitally-sign-pdf.md) | `POST /sign` | [docs](https://www.nutrient.io/api/reference/public/#tag/Digital-Signatures/operation/sign-file) |
| [Generate API Token](actions/generate-api-token.md) | `POST /tokens` | [docs](https://www.nutrient.io/api/reference/public/#tag/JWT/operation/generate-token) |
| [Get Account Information](actions/get-account-information.md) | `GET /account/info` | [docs](https://www.nutrient.io/api/reference/public/#tag/Account/operation/get-account-info) |
| [PDF/UA Auto-Tagging](actions/pdf-ua-auto-tagging.md) | `POST /processor/pdfua` | [docs](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/processor-pdfua) |
| [Perform OCR](actions/perform-ocr.md) | `POST /processor/ocr` | [docs](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/processor-ocr) |
| [Redact Documents](actions/redact-documents.md) | `POST /processor/redact` | [docs](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/processor-redact-document) |
| [Revoke API Token](actions/revoke-api-token.md) | `DELETE /tokens` | [docs](https://www.nutrient.io/api/reference/public/#tag/JWT/operation/revoke-token) |
