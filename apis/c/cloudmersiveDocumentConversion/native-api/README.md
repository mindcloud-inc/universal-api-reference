# Cloudmersive Document Conversion: Native API Reference

A consolidated summary of Cloudmersive Document Conversion's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.cloudmersive.com/docs/convert.asp
- **OpenAPI specification:** https://api.cloudmersive.com/convert/docs/v1/swagger
- **API base URL:** `https://api.cloudmersive.com`

## Authentication

### API Key

Cloudmersive API key authentication using the Apikey request header.

### Credentials

- **Cloudmersive API Key:** `apiKey` · required

Send these headers with each API request:

```http
Apikey: <apiKey>
```

[Official authentication documentation](https://api.cloudmersive.com/docs/convert.asp)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert CSV to XLSX](actions/convert-csv-to-xlsx.md) | `POST /convert/csv/to/xlsx` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert Document to JPG Array](actions/convert-document-to-jpg-array.md) | `POST /convert/autodetect/to/jpg` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert Document to PDF](actions/convert-document-to-pdf.md) | `POST /convert/autodetect/to/pdf` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert Document to PNG Array](actions/convert-document-to-png-array.md) | `POST /convert/autodetect/to/png` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert Document to Text](actions/convert-document-to-text.md) | `POST /convert/autodetect/to/txt` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert Word DOCX to HTML](actions/convert-docx-to-html.md) | `POST /convert/docx/to/html` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert Word DOCX to PDF](actions/convert-docx-to-pdf.md) | `POST /convert/docx/to/pdf` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert Word DOCX to Text](actions/convert-docx-to-text.md) | `POST /convert/docx/to/txt` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert Email EML to PDF](actions/convert-eml-to-pdf.md) | `POST /convert/eml/to/pdf` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert File to Thumbnail](actions/convert-file-to-thumbnail.md) | `POST /convert/autodetect/to/thumbnail` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert HTML File to PDF](actions/convert-html-file-to-pdf.md) | `POST /convert/html/to/pdf` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert HTML String to PDF](actions/convert-html-string-to-pdf.md) | `POST /convert/web/html/to/pdf` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert Image Format](actions/convert-image-format.md) | `POST /convert/image/{format1}/to/{format2}` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert ODT to DOCX](actions/convert-odt-to-docx.md) | `POST /convert/odt/to/docx` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert PDF to Word DOCX](actions/convert-pdf-to-docx.md) | `POST /convert/pdf/to/docx` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert PDF to PNG Array](actions/convert-pdf-to-png-array.md) | `POST /convert/pdf/to/png` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert PDF to Text](actions/convert-pdf-to-text.md) | `POST /convert/pdf/to/txt` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert PowerPoint PPTX to PDF](actions/convert-pptx-to-pdf.md) | `POST /convert/pptx/to/pdf` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert PowerPoint PPTX to Text](actions/convert-pptx-to-text.md) | `POST /convert/pptx/to/txt` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert URL to PDF](actions/convert-url-to-pdf.md) | `POST /convert/web/url/to/pdf` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert Excel XLSX to CSV](actions/convert-xlsx-to-csv.md) | `POST /convert/xlsx/to/csv` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert Excel XLSX to HTML](actions/convert-xlsx-to-html.md) | `POST /convert/xlsx/to/html` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Convert Excel XLSX to PDF](actions/convert-xlsx-to-pdf.md) | `POST /convert/xlsx/to/pdf` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
| [Get Document Type Information](actions/get-document-type-information.md) | `POST /convert/autodetect/get-info` | [docs](https://api.cloudmersive.com/docs/convert.asp) |
