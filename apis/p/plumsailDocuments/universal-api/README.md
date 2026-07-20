# <img src="https://images.mindcloud.co/apps/icons/plumsail-documents_1773833482190.png" alt="Plumsail Documents logo" width="28" height="28"> Plumsail Documents: Universal API

Generate, convert, and protect documents and PDFs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/plumsailDocuments/latest
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://plumsail.com/documents/
- **Vendor API docs:** https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile Info](actions/get-profile-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/get-profile-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Add Watermark to PDF](actions/add-watermark-to-pdf.md) | POST | Adds a watermark to a PDF in Plumsail Documents. |
| [Compress PDF Document](actions/compress-pdf-document.md) | POST | Compresses a PDF document in Plumsail Documents. |
| [Convert Any to PDF](actions/convert-any-to-pdf.md) | POST | Converts a document to PDF in Plumsail Documents. |
| [Convert CSV to XLSX](actions/convert-csv-to-xlsx.md) | POST | Converts CSV to XLSX in Plumsail Documents. |
| [Convert DOC to DOCX](actions/convert-doc-to-docx.md) | POST | Converts DOC to DOCX in Plumsail Documents. |
| [Convert DOCX to PDF](actions/convert-docx-to-pdf.md) | POST | Converts DOCX to PDF in Plumsail Documents. |
| [Convert HTML to PDF](actions/convert-html-to-pdf.md) | POST | Converts HTML to PDF in Plumsail Documents. |
| [Convert PPT to PPTX](actions/convert-ppt-to-pptx.md) | POST | Converts PPT to PPTX in Plumsail Documents. |
| [Convert PPTX to PDF](actions/convert-pptx-to-pdf.md) | POST | Converts PPTX to PDF in Plumsail Documents. |
| [Convert XLS to XLSX](actions/convert-xls-to-xlsx.md) | POST | Converts XLS to XLSX in Plumsail Documents. |
| [Convert XLSX to PDF](actions/convert-xlsx-to-pdf.md) | POST | Converts XLSX to PDF in Plumsail Documents. |
| [Create DOCX Document](actions/create-docx-document.md) | POST | Creates a DOCX document in Plumsail Documents. |
| [Create HTML Document](actions/create-html-document.md) | POST | Creates an HTML document in Plumsail Documents. |
| [Create PPTX Document](actions/create-pptx-document.md) | POST | Creates a PPTX document in Plumsail Documents. |
| [Create XLSX Document](actions/create-xlsx-document.md) | POST | Creates an XLSX document in Plumsail Documents. |
| [Extract Text from PDF](actions/extract-text-from-pdf.md) | POST | Extracts text from a PDF in Plumsail Documents. |
| [Fill DOCX Merge Fields](actions/fill-docx-merge-fields.md) | POST | Fills merge fields in a DOCX document in Plumsail Documents. |
| [Fill PDF Form](actions/fill-pdf-form.md) | POST | Fills a PDF form in Plumsail Documents. |
| [Get PDF Form](actions/get-pdf-form.md) | GET | Retrieves form fields from a PDF in Plumsail Documents. |
| [Protect PDF Document](actions/protect-pdf-document.md) | POST | Protects a PDF document in Plumsail Documents. |
| [Split PDF](actions/split-pdf.md) | POST | Splits a PDF in Plumsail Documents. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile Info](actions/get-profile-info.md) | GET | Retrieves profile information from Plumsail Documents. |

