# PDF Tools by Tachytelic: Native API Reference

A consolidated summary of PDF Tools by Tachytelic's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/
- **API base URL:** `https://pdf.tachytelic.net/api`

## Authentication

### No authentication

Tachytelic's public PDF Tools API does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Extract PDF Pages](actions/extract-pdf-pages.md) | `POST /extractpages` | [docs](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#extract-specific-pages) |
| [Extract Text from PDF](actions/extract-text-from-pdf.md) | `POST /extracttext` | [docs](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#extract-text) |
| [Get PDF Info](actions/get-pdf-info.md) | `POST /getinfo` | [docs](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#extract-info) |
| [Merge PDFs](actions/merge-pdfs.md) | `POST /merge` | [docs](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#merge-pdfs) |
| [Optimize PDF](actions/optimize-pdf.md) | `POST /optimize` | [docs](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#optimize-pdf) |
| [Set PDF Metadata](actions/set-pdf-metadata.md) | `POST /setmetadata` | [docs](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#set-metadata) |
| [Split PDF](actions/split-pdf.md) | `POST /split` | [docs](https://learn.microsoft.com/en-us/connectors/pdftoolsbytachytelic/#split-pdf) |
