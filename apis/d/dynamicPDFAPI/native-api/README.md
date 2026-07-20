# DynamicPDF: Native API Reference

A consolidated summary of DynamicPDF's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://dpdf.io/docs/usersguide/cloud-api/cloud-api-overview
- **API base URL:** `https://api.dpdf.io`

## Authentication

### API Key

Use a DynamicPDF API key from Portal > API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dpdf.io/docs/usersguide/environment-manager/environment-manager-api-api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Barcode To Existing PDF](actions/add-barcode-to-existing-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/add-barcodes-to-pdf) |
| [Add Barcode To New PDF](actions/add-barcode-to-new-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/add-barcodes-to-pdf) |
| [Add Cover Page To PDF](actions/add-cover-page-to-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/visual-create-pdf-cover-page) |
| [Add Custom Fonts To PDF](actions/add-custom-fonts-to-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-pdf-instructions) |
| [Add Overlay Elements To PDF](actions/add-overlay-elements-to-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/add-content-to-existing-pdf) |
| [Add Page Numbering To PDF](actions/add-page-numbering-to-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-pdf-instructions) |
| [Add PDF Bookmarks](actions/add-pdf-bookmarks.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/add-bookmarks-to-pdf) |
| [Apply Template To PDF](actions/apply-template-to-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/tutorials/designer/creating-a-page-using-template) |
| [Convert Excel To PDF](actions/convert-excel-to-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/convert-excel-to-pdf) |
| [Convert HTML To PDF](actions/convert-html-to-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/convert-html-to-pdf) |
| [Convert Images To PDF](actions/convert-images-to-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/convert-images-to-pdf) |
| [Convert PDF To Image](actions/convert-pdf-to-image.md) | `POST /v1.0/pdf-image` | [docs](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-pdf-image) |
| [Convert Word To PDF](actions/convert-word-to-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/convert-word-to-pdf) |
| [Create Multi-Page PDF](actions/create-multi-page-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-pdf-instructions) |
| [Create PDF From JSON](actions/create-pdf-from-json.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-pdf-json) |
| [Create PDF Report From Template](actions/create-pdf-report-from-template.md) | `POST /v1.0/dlex-layout` | [docs](https://dpdf.io/docs/tutorials/designer/creating-a-report-using-template) |
| [Delete Pages From PDF](actions/delete-pages-from-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/delete-pages-from-pdf) |
| [Encrypt PDF](actions/encrypt-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/encrypt-pdfs) |
| [Extract PDF Page Range](actions/extract-pdf-page-range.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/split-pdf-into-multiple-files) |
| [Fill PDF Form Fields](actions/fill-pdf-form-fields.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/pdf-form-filling) |
| [Flatten PDF Form Fields](actions/flatten-pdf-form-fields.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/flatten-or-delete-pdf-form-fields) |
| [Generate PDF From DLEX Layout](actions/generate-pdf-from-dlex-layout.md) | `POST /v1.0/dlex-layout` | [docs](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-dlex-layout) |
| [Generate PDF From DLEX Using PDF Endpoint](actions/generate-pdf-from-dlex-using-pdf-endpoint.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/usersguide/cloud-api/client-libraries/pdf-endpoint/pdf-inputs) |
| [Get Image Information](actions/get-image-information.md) | `POST /v1.0/image-info` | [docs](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-image-info) |
| [Get PDF Information](actions/get-pdf-information.md) | `POST /v1.0/pdf-info` | [docs](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-pdf-info) |
| [Get PDF Security Information](actions/get-pdf-security-information.md) | `POST /v1.0/pdf-security-info` | [docs](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-pdf-security-info) |
| [Get PDF XMP Metadata](actions/get-pdf-xmp-metadata.md) | `POST /v1.0/pdf-xmp` | [docs](https://dpdf.io/docs/usersguide/cloud-api/cloud-api-pdf-xmp) |
| [Import PDF Bookmarks](actions/import-pdf-bookmarks.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/add-bookmarks-to-pdf) |
| [Merge Mixed Resources Into PDF](actions/merge-mixed-resources-into-pdf.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/tutorials/cloud-api/dlex-pdf-endpoint) |
| [Merge PDFs](actions/merge-pdfs.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/merge-pdfs) |
| [Remove PDF Form Fields](actions/remove-pdf-form-fields.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/flatten-or-delete-pdf-form-fields) |
| [Retain Signature Fields During Processing](actions/retain-signature-fields-during-processing.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/usersguide/cloud-api/schemas/cloud-api-schema-pdf) |
| [Set PDF Metadata](actions/set-pdf-metadata.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/usersguide/cloud-api/schemas/cloud-api-schema-pdf) |
| [Split PDF Into Multiple PDFs](actions/split-pdf-into-multiple-pdfs.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/split-pdf-into-multiple-files) |
| [Tag PDF For Accessibility](actions/tag-pdf-for-accessibility.md) | `POST /v1.0/pdf` | [docs](https://dpdf.io/docs/usersguide/cloud-api/schemas/cloud-api-schema-pdf) |
