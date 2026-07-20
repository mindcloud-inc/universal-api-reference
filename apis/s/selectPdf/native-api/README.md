# SelectPdf: Native API Reference

A consolidated summary of SelectPdf's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://selectpdf.com/html-to-pdf-api/
- **API base URL:** `https://selectpdf.com/api2`

## Authentication

### API Key

SelectPdf requires the tenant API key to be sent as the `key` request field in query strings or request bodies, not as an Authorization header.

### Credentials

- **API Key:** `apiKey` · required · Your SelectPdf API license key. The app injects it into the provider's required `key` request field.

[Official authentication documentation](https://selectpdf.com/html-to-pdf-api/)

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert HTML to PDF](actions/convert-html-to-pdf.md) | `POST /convert/` | [docs](https://selectpdf.com/html-to-pdf-api/) |
| [Convert URL to PDF](actions/convert-url-to-pdf.md) | `GET /convert/` | [docs](https://selectpdf.com/html-to-pdf-api/) |
| [Extract Text from PDF File](actions/extract-text-from-pdf-file.md) | `POST /pdftotext/` | [docs](https://selectpdf.com/pdf-to-text-api/) |
| [Extract Text from PDF URL](actions/extract-text-from-pdfurl.md) | `POST /pdftotext/` | [docs](https://selectpdf.com/pdf-to-text-api/) |
| [Get API Usage](actions/get-api-usage.md) | `GET /usage/` | [docs](https://selectpdf.com/html-to-pdf-api/) |
| [Merge PDFs from URLs](actions/merge-pd-fs-from-ur-ls.md) | `POST /pdfmerge/` | [docs](https://selectpdf.com/pdf-merge-api/) |
| [Merge PDF Files](actions/merge-pdf-files.md) | `POST /pdfmerge/` | [docs](https://selectpdf.com/pdf-merge-api/) |
| [Search PDF File](actions/search-pdf-file.md) | `POST /pdftotext/` | [docs](https://selectpdf.com/pdf-to-text-api/) |
| [Search PDF URL](actions/search-pdfurl.md) | `POST /pdftotext/` | [docs](https://selectpdf.com/pdf-to-text-api/) |
