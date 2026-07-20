# <img src="https://images.mindcloud.co/apps/icons/pdf-filler_1773855861893.png" alt="PdfFiller logo" width="28" height="28"> PdfFiller: Universal API

Manage PDF templates, fill requests, signatures, and document workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pdfFiller/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pdffiller.com
- **Vendor API docs:** https://pdffiller.readme.io/docs/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from PdfFiller. |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Delete Filled Form](actions/delete-filled-form.md) | DELETE | Deletes an existing filled form from PdfFiller. |
| [Download Filled PDF Form](actions/download-filled-pdf-form.md) | GET | Downloads a filled PDF form from PdfFiller. |
| [Export Filled Form Data](actions/export-filled-form-data.md) | GET | Retrieves exported data for a filled form in PdfFiller. |
| [Get Filled Form](actions/get-filled-form.md) | GET | Retrieves a filled form from PdfFiller. |
| [List Filled Forms](actions/list-filled-forms.md) | GET | Retrieves filled forms from a PdfFiller fill request. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Fillable Form](actions/create-fillable-form.md) | POST | Creates a fillable form in PdfFiller. |
| [Create Fillable Form From Completed Document](actions/create-fillable-form-from-completed-document.md) | POST | Creates a fillable form in PdfFiller from a completed document. |
| [Create Fillable Form From Downloaded Document](actions/create-fillable-form-from-downloaded-document.md) | POST | Creates a fillable form in PdfFiller from a downloaded document. |
| [Delete Fillable Form](actions/delete-fillable-form.md) | DELETE | Deletes an existing fillable form from PdfFiller. |
| [Download All Filled Forms](actions/download-all-filled-forms.md) | GET | Downloads all filled forms from a PdfFiller fill request. |
| [Get Fillable Form](actions/get-fillable-form.md) | GET | Retrieves a fillable form from PdfFiller. |
| [List Fillable Forms](actions/list-fillable-forms.md) | GET | Retrieves fillable forms from PdfFiller. |
| [Update Fillable Form](actions/update-fillable-form.md) | PUT | Updates an existing fillable form in PdfFiller. |

### Signature Requests

| Action | Method | Description |
| --- | --- | --- |
| [Create Signature Request](actions/create-signature-request.md) | POST | Creates a signature request in PdfFiller. |
| [Create Signature Request From Completed Document](actions/create-signature-request-from-completed-document.md) | POST | Creates a signature request in PdfFiller from a completed document. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Template Constructor Link](actions/create-template-constructor-link.md) | POST | Creates a constructor link for a PdfFiller template. |
| [Create Template From Upload](actions/create-template-from-upload.md) | POST | Creates a template in PdfFiller from an uploaded file. |
| [Create Template From Url](actions/create-template-from-url.md) | POST | Creates a template in PdfFiller from a file URL. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from PdfFiller. |
| [Download Template](actions/download-template.md) | GET | Downloads a template from PdfFiller. |
| [Download Template Original Document](actions/download-template-original-document.md) | GET | Downloads the original document for a PdfFiller template. |
| [Fill Template](actions/fill-template.md) | POST | Creates a filled document from a PdfFiller template. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from PdfFiller. |
| [List Template Child Documents](actions/list-template-child-documents.md) | GET | Retrieves filled documents for a PdfFiller template. |
| [List Template Fields](actions/list-template-fields.md) | GET | Retrieves fields for a PdfFiller template. |
| [List Template Previews](actions/list-template-previews.md) | GET | Retrieves previews for a PdfFiller template. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from PdfFiller. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in PdfFiller. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from PdfFiller. |

