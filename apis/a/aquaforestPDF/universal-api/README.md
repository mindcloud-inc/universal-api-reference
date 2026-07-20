# <img src="https://images.mindcloud.co/apps/icons/aquaforest-pdf-icon_1777649674756.png" alt="Aquaforest PDF logo" width="28" height="28"> Aquaforest PDF: Universal API

Aquaforest PDF automates PDF workflows for Office 365 and Power Automate, including text extraction, barcode extraction, PDF splitting, page extraction, OCR, searchable PDF generation, and PDF property inspection.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aquaforestPDF/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.aquaforest.com/en/aquaforest-connector.asp
- **Vendor API docs:** https://learn.microsoft.com/en-us/connectors/aquaforest/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get PDF properties](actions/get-pdf-properties.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aquaforestPDF/latest/actions/get-pdf-properties?connectionId=$CONNECTION_ID&fileContent=JVBERi0xLjQKMSAwIG9iago8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4KZW5kb2JqCjIgMCBvYmoKPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4KZW5kb2JqCjMgMCBvYmoKPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvTWVkaWFCb3ggWzAgMCA2MTIgNzkyXSAvUmVzb3VyY2VzIDw8IC9Gb250IDw8IC9GMSA0IDAgUiA%2BPiA%2BPiAvQ29udGVudHMgNSAwIFIgPj4KZW5kb2JqCjQgMCBvYmoKPDwgL1R5cGUgL0ZvbnQgL1N1YnR5cGUgL1R5cGUxIC9CYXNlRm9udCAvSGVsdmV0aWNhID4%2BCmVuZG9iago1IDAgb2JqCjw8IC9MZW5ndGggMTM0ID4%2BCnN0cmVhbQpCVAovRjEgMTggVGYKNzIgNzIwIFRkCihBcXVhZm9yZXN0IHJ1bnRpbWUgdmVyaWZpY2F0aW9uKSBUagowIC0yNCBUZAooSW52b2ljZSBOdW1iZXI6IElOVi0xMjM0NSkgVGoKMCAtMjQgVGQKKFRvdGFsOiA0Mi4wMCBVU0QpIFRqCkVUCmVuZHN0cmVhbQplbmRvYmoKeHJlZgowIDYKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAwMDA5IDAwMDAwIG4gCjAwMDAwMDAwNTggMDAwMDAgbiAKMDAwMDAwMDExNSAwMDAwMCBuIAowMDAwMDAwMjQxIDAwMDAwIG4gCjAwMDAwMDAzMTEgMDAwMDAgbiAKdHJhaWxlcgo8PCAvU2l6ZSA2IC9Sb290IDEgMCBSID4%2BCnN0YXJ0eHJlZgo0OTUKJSVFT0YK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Extracted Pdf Pages

| Action | Method | Description |
| --- | --- | --- |
| [Extract PDF pages by barcode](actions/extract-pdf-pages-by-barcode.md) | POST | Extracts PDF pages by barcode matches in Aquaforest PDF. |
| [Extract PDF pages by text](actions/extract-pdf-pages-by-text.md) | POST | Extracts PDF pages by text matches in Aquaforest PDF. |

### Pdf Barcode Result

| Action | Method | Description |
| --- | --- | --- |
| [Get barcode value from PDF](actions/get-barcode-value-from-pdf.md) | GET | Retrieves barcode values from PDFs in Aquaforest PDF. |

### Pdf Data

| Action | Method | Description |
| --- | --- | --- |
| [Get data from PDF](actions/get-data-from-pdf.md) | GET | Retrieves key-value data from PDFs in Aquaforest PDF. |

### Pdf Document

| Action | Method | Description |
| --- | --- | --- |
| [Get PDF properties](actions/get-pdf-properties.md) | GET | Retrieves PDF file properties from Aquaforest PDF. |

### Pdf Text Result

| Action | Method | Description |
| --- | --- | --- |
| [Get text from PDF](actions/get-text-from-pdf.md) | GET | Retrieves matched text from PDFs in Aquaforest PDF. |

### Searchable Pdf

| Action | Method | Description |
| --- | --- | --- |
| [OCR PDF or image to searchable PDF](actions/ocr-pdf-or-image-to-searchable-pdf.md) | POST | Creates a searchable PDF from a PDF or image in Aquaforest PDF. |

### Split Pdf Files

| Action | Method | Description |
| --- | --- | --- |
| [Split PDF by barcode](actions/split-pdf-by-barcode.md) | POST | Splits PDF files by barcode matches in Aquaforest PDF. |
| [Split PDF by page](actions/split-pdf-by-page.md) | POST | Splits PDF files by page range in Aquaforest PDF. |
| [Split PDF by text match](actions/split-pdf-by-text-match.md) | POST | Splits PDF files by text matches in Aquaforest PDF. |

