# Diffchecker: Native API Reference

A consolidated summary of Diffchecker's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://www.diffchecker.com/docs/getting-started/
- **OpenAPI specification:** https://www.diffchecker.com/openapi.yaml
- **API base URL:** `https://api.diffchecker.com/public`

## Authentication

### API Key

Use your Diffchecker paid-plan API key. Diffchecker expects it in the X-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://www.diffchecker.com/docs/getting-started/)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compare Documents (HTML JSON, Character, Data URLs)](actions/compare-documents-html-json-character-data-urls.md) | `POST /pdf` | [docs](https://www.diffchecker.com/docs/document/) |
| [Compare Documents (HTML JSON, Character, Uploads)](actions/compare-documents-html-json-character-uploads.md) | `POST /pdf` | [docs](https://www.diffchecker.com/docs/document/) |
| [Compare Documents (HTML JSON, Data URLs)](actions/compare-documents-html-json-data-urls.md) | `POST /pdf` | [docs](https://www.diffchecker.com/docs/document/) |
| [Compare Documents (HTML JSON, Default Word, Data URLs)](actions/compare-documents-html-json-default-word-data-urls.md) | `POST /pdf` | [docs](https://www.diffchecker.com/docs/document/) |
| [Compare Documents (HTML JSON, Default Word, Uploads)](actions/compare-documents-html-json-default-word-uploads.md) | `POST /pdf` | [docs](https://www.diffchecker.com/docs/document/) |
| [Compare Documents (HTML JSON, Uploads)](actions/compare-documents-html-json-uploads.md) | `POST /pdf` | [docs](https://www.diffchecker.com/docs/document/) |
| [Compare Documents (JSON, Character, Data URLs)](actions/compare-documents-json-character-data-urls.md) | `POST /pdf` | [docs](https://www.diffchecker.com/docs/document/) |
| [Compare Documents (JSON, Character, Uploads)](actions/compare-documents-json-character-uploads.md) | `POST /pdf` | [docs](https://www.diffchecker.com/docs/document/) |
| [Compare Documents (JSON, Data URLs)](actions/compare-documents-json-data-urls.md) | `POST /pdf` | [docs](https://www.diffchecker.com/docs/document/) |
| [Compare Documents (JSON, Default Word, Data URLs)](actions/compare-documents-json-default-word-data-urls.md) | `POST /pdf` | [docs](https://www.diffchecker.com/docs/document/) |
| [Compare Documents (JSON, Default Word, Uploads)](actions/compare-documents-json-default-word-uploads.md) | `POST /pdf` | [docs](https://www.diffchecker.com/docs/document/) |
| [Compare Documents (JSON, Uploads)](actions/compare-documents-json-uploads.md) | `POST /pdf` | [docs](https://www.diffchecker.com/docs/document/) |
| [Compare Excel Spreadsheets (Formulas, Data URLs)](actions/compare-excel-spreadsheets-formulas-data-urls.md) | `POST /excel` | [docs](https://www.diffchecker.com/docs/excel/) |
| [Compare Excel Spreadsheets (Formulas, Normalized, Data URLs)](actions/compare-excel-spreadsheets-formulas-normalized-data-urls.md) | `POST /excel` | [docs](https://www.diffchecker.com/docs/excel/) |
| [Compare Excel Spreadsheets (Formulas, Normalized, Uploads)](actions/compare-excel-spreadsheets-formulas-normalized-uploads.md) | `POST /excel` | [docs](https://www.diffchecker.com/docs/excel/) |
| [Compare Excel Spreadsheets (Formulas, Uploads)](actions/compare-excel-spreadsheets-formulas-uploads.md) | `POST /excel` | [docs](https://www.diffchecker.com/docs/excel/) |
| [Compare Excel Spreadsheets (Standard, Data URLs)](actions/compare-excel-spreadsheets-standard-data-urls.md) | `POST /excel` | [docs](https://www.diffchecker.com/docs/excel/) |
| [Compare Excel Spreadsheets (Standard, Hide Unchanged, Data URLs)](actions/compare-excel-spreadsheets-standard-hide-unchanged-data-urls.md) | `POST /excel` | [docs](https://www.diffchecker.com/docs/excel/) |
| [Compare Excel Spreadsheets (Standard, Normalized, Data URLs)](actions/compare-excel-spreadsheets-standard-normalized-data-urls.md) | `POST /excel` | [docs](https://www.diffchecker.com/docs/excel/) |
| [Compare Excel Spreadsheets (Standard, Normalized, Uploads)](actions/compare-excel-spreadsheets-standard-normalized-uploads.md) | `POST /excel` | [docs](https://www.diffchecker.com/docs/excel/) |
| [Compare Excel Spreadsheets (Standard, Uploads)](actions/compare-excel-spreadsheets-standard-uploads.md) | `POST /excel` | [docs](https://www.diffchecker.com/docs/excel/) |
| [Compare Images (JSON, Data URLs)](actions/compare-images-json-data-urls.md) | `POST /image` | [docs](https://www.diffchecker.com/docs/image/) |
| [Compare Images (JSON, Uploads)](actions/compare-images-json-uploads.md) | `POST /image` | [docs](https://www.diffchecker.com/docs/image/) |
| [Compare Text (HTML JSON)](actions/compare-text-html-json.md) | `POST /text` | [docs](https://www.diffchecker.com/docs/text/) |
| [Compare Text (HTML JSON, Character)](actions/compare-text-html-json-character.md) | `POST /text` | [docs](https://www.diffchecker.com/docs/text/) |
| [Compare Text (HTML JSON, Default Word)](actions/compare-text-html-json-default-word.md) | `POST /text` | [docs](https://www.diffchecker.com/docs/text/) |
| [Compare Text (JSON)](actions/compare-text-json.md) | `POST /text` | [docs](https://www.diffchecker.com/docs/text/) |
| [Compare Text (JSON, Character)](actions/compare-text-json-character.md) | `POST /text` | [docs](https://www.diffchecker.com/docs/text/) |
| [Compare Text (JSON, Default Word)](actions/compare-text-json-default-word.md) | `POST /text` | [docs](https://www.diffchecker.com/docs/text/) |
| [Test Authentication](actions/test-authentication.md) | `GET /auth-test` | [docs](https://www.diffchecker.com/docs/getting-started/) |
