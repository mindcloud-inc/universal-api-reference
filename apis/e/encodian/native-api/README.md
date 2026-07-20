# Encodian: Native API Reference

A consolidated summary of Encodian's API configuration and 43 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/connectors/encodianpdf/
- **API base URL:** `https://api.apps-encodian.com`

## Authentication

### API Key

Use an Encodian Flowr API key to authenticate requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-ApiKey: <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-us/connectors/encodianpdf/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (43 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Excel](actions/convert-excel.md) | `POST /api/v1/Conversion/ConvertExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/360011804178) |
| [Convert File To PDF](actions/convert-file-to-pdf.md) | `POST /api/v1/Conversion/BasicConversion` | [docs](https://support.encodian.com/hc/en-gb/articles/360011123574) |
| [Convert HTML To PDF V2](actions/convert-html-to-pdf-v2.md) | `POST /api/v1/Conversion/HtmlToPDFV2` | [docs](https://support.encodian.com/hc/en-gb/articles/16421778005020) |
| [Convert Image To PDF](actions/convert-image-to-pdf.md) | `POST /api/v1/Conversion/ConvertImageToPdf` | [docs](https://support.encodian.com/hc/en-gb/articles/23601928355228) |
| [Convert JSON To Excel](actions/convert-json-to-excel.md) | `POST /api/v1/Conversion/ConvertJsonToExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/7690520790045) |
| [Convert PDF To Excel](actions/convert-pdf-to-excel.md) | `POST /api/v1/Conversion/ConvertPdfToExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/17011591184284) |
| [Convert PDF To Images](actions/convert-pdf-to-images.md) | `POST /api/v1/Conversion/ConvertPdfToImages` | [docs](https://support.encodian.com/hc/en-gb/articles/4418101623441) |
| [Convert PDF To Word](actions/convert-pdf-to-word.md) | `POST /api/v1/Conversion/ConvertPdfToWord` | [docs](https://support.encodian.com/hc/en-gb/articles/360027229294) |
| [Convert Word](actions/convert-word.md) | `POST /api/v1/Conversion/ConvertWord` | [docs](https://support.encodian.com/hc/en-gb/articles/360015616117) |
| [Convert Word To PDF Form](actions/convert-word-to-pdf-form.md) | `POST /api/v1/Conversion/WordToPdfForm` | [docs](https://support.encodian.com/hc/en-gb/articles/360012307133) |
| [Email Extract Attachments](actions/email-extract-attachments.md) | `POST /api/v1/General/GetEmailAttachments` | [docs](https://support.encodian.com/hc/en-gb/articles/10531671561629) |
| [Email Extract Metadata](actions/email-extract-metadata.md) | `POST /api/v1/General/GetEmailInfo` | [docs](https://support.encodian.com/hc/en-gb/articles/12237799140252) |
| [Excel Extract Rows](actions/excel-extract-rows.md) | `POST /api/v1/Excel/GetRowsFromExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/9390845334172) |
| [Excel Populate](actions/excel-populate.md) | `POST /api/v1/Excel/PopulateExcel` | [docs](https://support.encodian.com/hc/en-gb/articles/12736409527324) |
| [Get Subscription Status](actions/get-subscription-status.md) | `GET /api/v1/General/GetSubscriptionStatus` | [docs](https://support.encodian.com/hc/en-gb/articles/360010176717-Get-Subscription-Status) |
| [PDF Extract Form Data](actions/p-df-extract-form-data.md) | `POST /api/v1/PDF/GetPdfFormData` | [docs](https://support.encodian.com/hc/en-gb/articles/360035107433) |
| [PDF Extract Table Data](actions/p-df-extract-table-data.md) | `POST /api/v1/PDF/PdfExtractTableData` | [docs](https://support.encodian.com/hc/en-gb/articles/15064945594268) |
| [PDF Extract Text](actions/p-df-extract-text.md) | `POST /api/v1/PDF/GetPdfTextLayer` | [docs](https://support.encodian.com/hc/en-gb/articles/360015539373) |
| [PDF Extract Text By Page](actions/p-df-extract-text-by-page.md) | `POST /api/v1/PDF/PdfExtractTextByPage` | [docs](https://support.encodian.com/hc/en-gb/articles/20683984513180) |
| [PDF Add Page Numbers](actions/pdf-add-page-numbers.md) | `POST /api/v1/PDF/AddPageNumbers` | [docs](https://support.encodian.com/hc/en-gb/articles/360014464534) |
| [PDF Apply OCR AI](actions/pdf-apply-ocr-ai.md) | `POST /api/v1/PDF/AIOcrPdfDocument` | [docs](https://support.encodian.com/hc/en-gb/articles/14286080106908) |
| [PDF Compress](actions/pdf-compress.md) | `POST /api/v1/PDF/CompressPdf` | [docs](https://support.encodian.com/hc/en-gb/articles/360019994857-Compress-PDF) |
| [PDF Delete Pages](actions/pdf-delete-pages.md) | `POST /api/v1/PDF/DeletePdfPages` | [docs](https://support.encodian.com/hc/en-gb/articles/13690317983132/) |
| [PDF Extract Pages](actions/pdf-extract-pages.md) | `POST /api/v1/PDF/ExtractPdfPages` | [docs](https://support.encodian.com/hc/en-gb/articles/13958097048732) |
| [PDF Fill Form](actions/pdf-fill-form.md) | `POST /api/v1/PDF/FillPdfForm` | [docs](https://support.encodian.com/hc/en-gb/articles/360008556077) |
| [PDF Flatten](actions/pdf-flatten.md) | `POST /api/v1/PDF/FlattenPdf` | [docs](https://support.encodian.com/hc/en-gb/articles/4416473033105) |
| [PDF Merge Files](actions/pdf-merge-files.md) | `POST /api/v1/PDF/MergeArrayOfDocumentsToPdf` | [docs](https://support.encodian.com/hc/en-gb/articles/360014632213) |
| [PDF Redact](actions/pdf-redact.md) | `POST /api/v1/PDF/RedactPdf` | [docs](https://support.encodian.com/hc/en-gb/articles/360018607954) |
| [PDF Replace Text](actions/pdf-replace-text.md) | `POST /api/v1/PDF/PdfSearchAndReplaceText` | [docs](https://support.encodian.com/hc/en-gb/articles/15962260285980) |
| [PDF Split](actions/pdf-split.md) | `POST /api/v1/PDF/SplitDocument` | [docs](https://support.encodian.com/hc/en-gb/articles/360002953277) |
| [PDF Split By Barcode](actions/pdf-split-by-barcode.md) | `POST /api/v1/PDF/SplitPdfByBarcode` | [docs](https://support.encodian.com/hc/en-gb/articles/360013629457) |
| [PDF Split By Text](actions/pdf-split-by-text.md) | `POST /api/v1/PDF/SplitPdfByText` | [docs](https://support.encodian.com/hc/en-gb/articles/360012726397) |
| [PDF Unlock](actions/pdf-unlock.md) | `POST /api/v1/PDF/UnlockPdfDocument` | [docs](https://support.encodian.com/hc/en-gb/articles/360003714237) |
| [PowerPoint Compress](actions/power-point-compress.md) | `POST /api/v1/PowerPoint/CompressPowerPoint` | [docs](https://support.encodian.com/hc/en-gb/articles/7621965500189) |
| [PowerPoint Delete Slides](actions/power-point-delete-slides.md) | `POST /api/v1/PowerPoint/PowerPointDeleteSlides` | [docs](https://support.encodian.com/hc/en-gb/articles/16535770370844) |
| [PowerPoint Merge Files](actions/power-point-merge-files.md) | `POST /api/v1/PowerPoint/MergePresentations` | [docs](https://support.encodian.com/hc/en-gb/articles/4425652063761) |
| [PowerPoint Populate](actions/power-point-populate.md) | `POST /api/v1/PowerPoint/PopulatePowerPoint` | [docs](https://support.encodian.com/hc/en-gb/articles/9715390966300) |
| [PowerPoint Replace Text](actions/power-point-replace-text.md) | `POST /api/v1/PowerPoint/PowerPointSearchAndReplaceText` | [docs](https://support.encodian.com/hc/en-gb/articles/19804599079836) |
| [PowerPoint Split](actions/power-point-split.md) | `POST /api/v1/PowerPoint/PowerPointSplit` | [docs](https://support.encodian.com/hc/en-gb/articles/16517600430620) |
| [Word Compare](actions/word-compare.md) | `POST /api/v1/Word/CompareWordDocuments` | [docs](https://support.encodian.com/hc/en-gb/articles/360018576278-Compare-Word-Documents) |
| [Word Extract Text](actions/word-extract-text.md) | `POST /api/v1/Word/GetTextFromWord` | [docs](https://support.encodian.com/hc/en-gb/articles/10583756977180) |
| [Word Populate](actions/word-populate.md) | `POST /api/v1/Word/PopulateWordDocument` | [docs](https://support.encodian.com/hc/en-gb/articles/360019620578-Populate-Word-Document) |
| [Word Replace Text](actions/word-replace-text.md) | `POST /api/v1/Word/WordSearchAndReplaceText` | [docs](https://support.encodian.com/hc/en-gb/articles/15949925002268) |
