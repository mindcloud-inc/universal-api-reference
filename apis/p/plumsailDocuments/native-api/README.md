# Plumsail Documents: Native API Reference

A consolidated summary of Plumsail Documents's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)
- **OpenAPI specification:** https://us-api.plumsail.com/swagger/documents-v2/swagger.json
- **API base URL:** `https://us-api.plumsail.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://plumsail.com/docs/documents/v1.x/user-guide/api-keys.html)

## API conventions

Request bodies use multipart form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

Responses from this API use JSON.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Watermark to PDF](actions/add-watermark-to-pdf.md) | `POST /api/v2/watermark/pdf-to-pdf` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Watermark) |
| [Compress PDF Document](actions/compress-pdf-document.md) | `POST /api/v2/pdf/compress` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Pdf) |
| [Convert Any to PDF](actions/convert-any-to-pdf.md) | `POST /api/v2/convert/any-to-pdf` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert) |
| [Convert CSV to XLSX](actions/convert-csv-to-xlsx.md) | `POST /api/v2/convert/csv-to-xlsx` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert) |
| [Convert DOC to DOCX](actions/convert-doc-to-docx.md) | `POST /api/v2/convert/doc-to-docx` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert) |
| [Convert DOCX to PDF](actions/convert-docx-to-pdf.md) | `POST /api/v2/convert/docx-to-pdf` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert) |
| [Convert HTML to PDF](actions/convert-html-to-pdf.md) | `POST /api/v2/convert/html-to-pdf` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert) |
| [Convert PPT to PPTX](actions/convert-ppt-to-pptx.md) | `POST /api/v2/convert/ppt-to-pptx` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert) |
| [Convert PPTX to PDF](actions/convert-pptx-to-pdf.md) | `POST /api/v2/convert/pptx-to-pdf` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert) |
| [Convert XLS to XLSX](actions/convert-xls-to-xlsx.md) | `POST /api/v2/convert/xls-to-xlsx` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert) |
| [Convert XLSX to PDF](actions/convert-xlsx-to-pdf.md) | `POST /api/v2/convert/xlsx-to-pdf` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert) |
| [Create DOCX Document](actions/create-docx-document.md) | `POST /api/v2/generate/from-docx` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Generate) |
| [Create HTML Document](actions/create-html-document.md) | `POST /api/v2/generate/from-html` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Generate) |
| [Create PPTX Document](actions/create-pptx-document.md) | `POST /api/v2/generate/from-pptx` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Generate) |
| [Create XLSX Document](actions/create-xlsx-document.md) | `POST /api/v2/generate/from-xlsx` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Generate) |
| [Extract Text from PDF](actions/extract-text-from-pdf.md) | `POST /api/v2/convert/pdf-to-text` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert) |
| [Fill DOCX Merge Fields](actions/fill-docx-merge-fields.md) | `POST /api/v2/generate/from-fillable-docx` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Generate) |
| [Fill PDF Form](actions/fill-pdf-form.md) | `POST /api/v2/pdf/fill-form` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Pdf) |
| [Get PDF Form](actions/get-pdf-form.md) | `GET /api/v2/pdf/get-form` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Pdf) |
| [Get Profile Info](actions/get-profile-info.md) | `GET /api/v2/user/Profiles/me` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/UserAPI) |
| [Protect PDF Document](actions/protect-pdf-document.md) | `POST /api/v2/pdf/protect` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Pdf) |
| [Split PDF](actions/split-pdf.md) | `POST /api/v2/pdf/split` | [docs](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Pdf) |
