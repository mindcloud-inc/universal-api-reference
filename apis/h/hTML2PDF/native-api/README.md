# HTML 2 PDF: Native API Reference

A consolidated summary of HTML 2 PDF's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://html2pdf.app/documentation/
- **API base URL:** `https://api.html2pdf.app/v1`

## Authentication

### API Key

Use your html2pdf.app API key to generate PDF documents.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://html2pdf.app/documentation/)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate PDF](actions/generate-pdf.md) | `POST /generate` | [docs](https://html2pdf.app/documentation/) |
