# <img src="https://images.mindcloud.co/apps/icons/id-xhd4uv-o-logos_1775073913364.jpeg" alt="DynamicPDF logo" width="28" height="28"> DynamicPDF: Universal API

Create, convert, and extract data from PDFs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dynamicPDFAPI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dpdf.io/
- **Vendor API docs:** https://dpdf.io/docs/usersguide/cloud-api/cloud-api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Convert PDF To Image](actions/convert-pdf-to-image.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/convert-pdf-to-image?connectionId=$CONNECTION_ID&pdf=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Convert Images To PDF](actions/convert-images-to-pdf.md) | POST | Converts images to a PDF in DynamicPDF API. |
| [Merge PDFs](actions/merge-pdfs.md) | POST | Merges PDFs in DynamicPDF API. |

### Image Information

| Action | Method | Description |
| --- | --- | --- |
| [Get Image Information](actions/get-image-information.md) | GET | Retrieves information about an image from DynamicPDF API. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create PDF Report From Template](actions/create-pdf-report-from-template.md) | POST | Creates a PDF report from a template in DynamicPDF API. |
| [Delete Pages From PDF](actions/delete-pages-from-pdf.md) | PUT | Deletes pages from a PDF in DynamicPDF API. |
| [Generate PDF From DLEX Layout](actions/generate-pdf-from-dlex-layout.md) | POST | Generates a PDF from a DLEX layout in DynamicPDF API. |
| [Generate PDF From DLEX Using PDF Endpoint](actions/generate-pdf-from-dlex-using-pdf-endpoint.md) | POST | Generates a PDF from DLEX using DynamicPDF API. |
| [Merge Mixed Resources Into PDF](actions/merge-mixed-resources-into-pdf.md) | POST | Merges mixed resources into a PDF in DynamicPDF API. |
| [Remove PDF Form Fields](actions/remove-pdf-form-fields.md) | PUT | Removes PDF form fields in DynamicPDF API. |
| [Retain Signature Fields During Processing](actions/retain-signature-fields-during-processing.md) | PUT | Retains signature fields while processing a PDF in DynamicPDF API. |
| [Split PDF Into Multiple PDFs](actions/split-pdf-into-multiple-pdfs.md) | GET | Splits a PDF into multiple PDFs in DynamicPDF API. |
| [Tag PDF For Accessibility](actions/tag-pdf-for-accessibility.md) | PUT | Tags a PDF for accessibility in DynamicPDF API. |

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Add Barcode To Existing PDF](actions/add-barcode-to-existing-pdf.md) | PUT | Adds a barcode to an existing PDF in DynamicPDF API. |
| [Add Barcode To New PDF](actions/add-barcode-to-new-pdf.md) | POST | Adds a barcode to a new PDF in DynamicPDF API. |
| [Add Cover Page To PDF](actions/add-cover-page-to-pdf.md) | PUT | Adds a cover page to a PDF in DynamicPDF API. |
| [Add Custom Fonts To PDF](actions/add-custom-fonts-to-pdf.md) | PUT | Adds custom fonts to a PDF in DynamicPDF API. |
| [Add Overlay Elements To PDF](actions/add-overlay-elements-to-pdf.md) | PUT | Adds overlay elements to a PDF in DynamicPDF API. |
| [Add Page Numbering To PDF](actions/add-page-numbering-to-pdf.md) | PUT | Adds page numbering to a PDF in DynamicPDF API. |
| [Add PDF Bookmarks](actions/add-pdf-bookmarks.md) | PUT | Adds bookmarks to a PDF in DynamicPDF API. |
| [Apply Template To PDF](actions/apply-template-to-pdf.md) | PUT | Applies a template to a PDF in DynamicPDF API. |
| [Convert Excel To PDF](actions/convert-excel-to-pdf.md) | POST | Converts an Excel file to a PDF in DynamicPDF API. |
| [Convert HTML To PDF](actions/convert-html-to-pdf.md) | POST | Converts HTML to a PDF in DynamicPDF API. |
| [Convert Word To PDF](actions/convert-word-to-pdf.md) | POST | Converts a Word document to a PDF in DynamicPDF API. |
| [Create Multi-Page PDF](actions/create-multi-page-pdf.md) | POST | Creates a multi-page PDF in DynamicPDF API. |
| [Create PDF From JSON](actions/create-pdf-from-json.md) | POST | Creates a PDF from JSON in DynamicPDF API. |
| [Encrypt PDF](actions/encrypt-pdf.md) | PUT | Encrypts a PDF in DynamicPDF API. |
| [Extract PDF Page Range](actions/extract-pdf-page-range.md) | GET | Extracts a page range from a PDF in DynamicPDF API. |
| [Fill PDF Form Fields](actions/fill-pdf-form-fields.md) | PUT | Fills PDF form fields in DynamicPDF API. |
| [Flatten PDF Form Fields](actions/flatten-pdf-form-fields.md) | PUT | Flattens PDF form fields in DynamicPDF API. |
| [Import PDF Bookmarks](actions/import-pdf-bookmarks.md) | PUT | Imports bookmarks into a PDF in DynamicPDF API. |
| [Set PDF Metadata](actions/set-pdf-metadata.md) | PUT | Sets PDF metadata in DynamicPDF API. |

### Pdf Image

| Action | Method | Description |
| --- | --- | --- |
| [Convert PDF To Image](actions/convert-pdf-to-image.md) | GET | Converts a PDF to images in DynamicPDF API. |

### Pdf Information

| Action | Method | Description |
| --- | --- | --- |
| [Get PDF Information](actions/get-pdf-information.md) | GET | Retrieves information about a PDF from DynamicPDF API. |

### Pdf Security Information

| Action | Method | Description |
| --- | --- | --- |
| [Get PDF Security Information](actions/get-pdf-security-information.md) | GET | Retrieves PDF security information from DynamicPDF API. |

### Pdf Xmp Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get PDF XMP Metadata](actions/get-pdf-xmp-metadata.md) | GET | Retrieves PDF XMP metadata from DynamicPDF API. |

