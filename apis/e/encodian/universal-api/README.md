# <img src="https://images.mindcloud.co/apps/icons/id0b9yl6g-k-1776279150251_1776279245552.jpeg" alt="Encodian logo" width="28" height="28"> Encodian: Universal API

Create, convert, secure, split, merge, and extract data from PDF and Office documents with Encodian Flowr document automation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/encodian/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 43
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.encodian.com/
- **Vendor API docs:** https://learn.microsoft.com/en-us/connectors/encodianpdf/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Subscription Status](actions/get-subscription-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/get-subscription-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (43)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Email Extract Attachments](actions/email-extract-attachments.md) | GET | Retrieves email attachments from Encodian. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Convert PDF To Excel](actions/convert-pdf-to-excel.md) | POST | Converts a PDF document to Excel in Encodian. |
| [Convert PDF To Images](actions/convert-pdf-to-images.md) | POST | Converts a PDF document to images in Encodian. |
| [Convert PDF To Word](actions/convert-pdf-to-word.md) | POST | Converts a PDF document to Word in Encodian. |
| [PDF Add Page Numbers](actions/pdf-add-page-numbers.md) | PUT | Adds page numbers to a PDF in Encodian. |
| [PDF Apply OCR AI](actions/pdf-apply-ocr-ai.md) | PUT | Applies OCR to a PDF in Encodian. |
| [PDF Compress](actions/pdf-compress.md) | PUT | Compresses a PDF document in Encodian. |
| [PDF Delete Pages](actions/pdf-delete-pages.md) | DELETE | Deletes PDF pages in Encodian. |
| [PDF Extract Pages](actions/pdf-extract-pages.md) | GET | Extracts PDF pages in Encodian. |
| [PDF Fill Form](actions/pdf-fill-form.md) | POST | Populates a PDF form in Encodian. |
| [PDF Flatten](actions/pdf-flatten.md) | PUT | Flattens a PDF document in Encodian. |
| [PDF Redact](actions/pdf-redact.md) | PUT | Redacts text in a PDF with Encodian. |
| [PDF Replace Text](actions/pdf-replace-text.md) | PUT | Replaces text in a PDF with Encodian. |
| [PDF Split](actions/pdf-split.md) | DELETE | Splits a PDF document in Encodian. |
| [PDF Split By Barcode](actions/pdf-split-by-barcode.md) | DELETE | Splits a PDF by barcode in Encodian. |
| [PDF Split By Text](actions/pdf-split-by-text.md) | DELETE | Splits a PDF by text in Encodian. |
| [PDF Unlock](actions/pdf-unlock.md) | PUT | Unlocks a PDF document in Encodian. |
| [Word Compare](actions/word-compare.md) | GET | Compares Word or PDF documents in Encodian. |
| [Word Replace Text](actions/word-replace-text.md) | PUT | Replaces text in a Word document with Encodian. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Convert Excel](actions/convert-excel.md) | POST | Converts an Excel file in Encodian. |
| [Convert File To PDF](actions/convert-file-to-pdf.md) | POST | Converts a file to PDF in Encodian. |
| [Convert HTML To PDF V2](actions/convert-html-to-pdf-v2.md) | POST | Converts HTML to PDF in Encodian. |
| [Convert Image To PDF](actions/convert-image-to-pdf.md) | POST | Converts an image to PDF in Encodian. |
| [Convert JSON To Excel](actions/convert-json-to-excel.md) | POST | Converts JSON data to Excel in Encodian. |
| [Convert Word](actions/convert-word.md) | POST | Converts a Word document in Encodian. |
| [Convert Word To PDF Form](actions/convert-word-to-pdf-form.md) | POST | Converts Word to a PDF form in Encodian. |
| [Excel Extract Rows](actions/excel-extract-rows.md) | GET | Extracts Excel rows in Encodian. |
| [Excel Populate](actions/excel-populate.md) | POST | Populates an Excel workbook in Encodian. |
| [PDF Extract Form Data](actions/p-df-extract-form-data.md) | GET | Extracts PDF form data in Encodian. |
| [PDF Extract Table Data](actions/p-df-extract-table-data.md) | GET | Extracts PDF table data in Encodian. |
| [PDF Extract Text](actions/p-df-extract-text.md) | GET | Extracts text from a PDF in Encodian. |
| [PDF Extract Text By Page](actions/p-df-extract-text-by-page.md) | GET | Extracts PDF text by page in Encodian. |
| [PDF Merge Files](actions/pdf-merge-files.md) | POST | Merges PDF files in Encodian. |
| [PowerPoint Compress](actions/power-point-compress.md) | PUT | Compresses a PowerPoint file in Encodian. |
| [PowerPoint Delete Slides](actions/power-point-delete-slides.md) | DELETE | Deletes PowerPoint slides in Encodian. |
| [PowerPoint Merge Files](actions/power-point-merge-files.md) | POST | Merges PowerPoint files in Encodian. |
| [PowerPoint Populate](actions/power-point-populate.md) | POST | Populates a PowerPoint file in Encodian. |
| [PowerPoint Replace Text](actions/power-point-replace-text.md) | PUT | Replaces text in PowerPoint files with Encodian. |
| [PowerPoint Split](actions/power-point-split.md) | POST | Splits a PowerPoint file in Encodian. |
| [Word Extract Text](actions/word-extract-text.md) | GET | Extracts text from a Word document in Encodian. |
| [Word Populate](actions/word-populate.md) | POST | Populates a Word document in Encodian. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Email Extract Metadata](actions/email-extract-metadata.md) | GET | Retrieves email metadata from Encodian. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Status](actions/get-subscription-status.md) | GET | Retrieves subscription status from Encodian. |

