# PdfFiller: Native API Reference

A consolidated summary of PdfFiller's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://pdffiller.readme.io/docs/getting-started
- **API base URL:** `https://api.pdffiller.com`

## Authentication

### API Key

Connect with a PDFfiller bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pdffiller.readme.io/reference/post_v2-oauth-token)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Fillable Form](actions/create-fillable-form.md) | `POST /v2/fillable_forms` | [docs](https://pdffiller.readme.io/reference/post_v2-fillable-forms) |
| [Create Fillable Form From Completed Document](actions/create-fillable-form-from-completed-document.md) | `POST /v2/fillable_forms` | [docs](https://pdffiller.readme.io/reference/post_v2-fillable-forms) |
| [Create Fillable Form From Downloaded Document](actions/create-fillable-form-from-downloaded-document.md) | `POST /v2/fillable_forms` | [docs](https://pdffiller.readme.io/reference/post_v2-fillable-forms-) |
| [Create Signature Request](actions/create-signature-request.md) | `POST /v2/signature_requests` | [docs](https://pdffiller.readme.io/reference/post_v2-signature-requests) |
| [Create Signature Request From Completed Document](actions/create-signature-request-from-completed-document.md) | `POST /v2/signature_requests` | [docs](https://pdffiller.readme.io/reference/post_v2-signature-requests-) |
| [Create Template Constructor Link](actions/create-template-constructor-link.md) | `POST /v2/templates/:templateId/constructor` | [docs](https://pdffiller.readme.io/reference/post_v2-templates-template-id-constructor) |
| [Create Template From Upload](actions/create-template-from-upload.md) | `POST /v2/templates` | [docs](https://pdffiller.readme.io/reference/post_v2-templates) |
| [Create Template From Url](actions/create-template-from-url.md) | `POST /v2/templates` | [docs](https://pdffiller.readme.io/reference/post_v2-templates) |
| [Delete Fillable Form](actions/delete-fillable-form.md) | `DELETE /v2/fillable_forms/:linkToFillId` | [docs](https://pdffiller.readme.io/reference/delete_v2-fillable-forms-link-to-fill-id) |
| [Delete Filled Form](actions/delete-filled-form.md) | `DELETE /v2/fillable_forms/:linkToFillId/filled_forms/:filledFormId` | [docs](https://pdffiller.readme.io/reference/delete_v2-fillable-forms-link-to-fill-id-filled-forms-filled-form-id) |
| [Delete Template](actions/delete-template.md) | `DELETE /v2/templates/:templateId` | [docs](https://pdffiller.readme.io/reference/delete_v2-templates-template-id) |
| [Download All Filled Forms](actions/download-all-filled-forms.md) | `GET /v2/fillable_forms/:linkToFillId/download` | [docs](https://pdffiller.readme.io/reference/get_v2-fillable-forms-link-to-fill-id-download) |
| [Download Filled PDF Form](actions/download-filled-pdf-form.md) | `GET /v2/fillable_forms/:linkToFillId/filled_forms/:filledFormId/download` | [docs](https://pdffiller.readme.io/reference/get_v2-fillable-forms-link-to-fill-id-filled-forms-filled-form-id-download) |
| [Download Template](actions/download-template.md) | `GET /v2/templates/:templateId/download` | [docs](https://pdffiller.readme.io/reference/get_v2-templates-template-id-download) |
| [Download Template Original Document](actions/download-template-original-document.md) | `GET /v2/templates/:templateId/original_document` | [docs](https://pdffiller.readme.io/reference/get_v2-templates-template-id-original-document) |
| [Export Filled Form Data](actions/export-filled-form-data.md) | `GET /v2/fillable_forms/:linkToFillId/filled_forms/:filledFormId/export` | [docs](https://pdffiller.readme.io/reference/get_v2-fillable-forms-link-to-fill-id-filled-forms-filled-form-id-export) |
| [Fill Template](actions/fill-template.md) | `POST /v2/templates/:templateId` | [docs](https://pdffiller.readme.io/reference/post_v2-templates-template-id) |
| [Get Current User](actions/get-current-user.md) | `GET /v2/users/me` | [docs](https://pdffiller.readme.io/reference/get_v2-users-me) |
| [Get Fillable Form](actions/get-fillable-form.md) | `GET /v2/fillable_forms/:linkToFillId` | [docs](https://pdffiller.readme.io/reference/get_v2-fillable-forms-link-to-fill-id) |
| [Get Filled Form](actions/get-filled-form.md) | `GET /v2/fillable_forms/:linkToFillId/filled_forms/:filledFormId` | [docs](https://pdffiller.readme.io/reference/get_v2-fillable-forms-link-to-fill-id-filled-forms-filled-form-id) |
| [Get Template](actions/get-template.md) | `GET /v2/templates/:templateId` | [docs](https://pdffiller.readme.io/reference/get_v2-templates-template-id) |
| [List Fillable Forms](actions/list-fillable-forms.md) | `GET /v2/fillable_forms` | [docs](https://pdffiller.readme.io/reference/get_v2-fillable-forms) |
| [List Filled Forms](actions/list-filled-forms.md) | `GET /v2/fillable_forms/:linkToFillId/filled_forms` | [docs](https://pdffiller.readme.io/reference/get_v2-fillable-forms-link-to-fill-id-filled-forms) |
| [List Folders](actions/list-folders.md) | `GET /v2/folders` | [docs](https://pdffiller.readme.io/reference/get_v2-folders) |
| [List Template Child Documents](actions/list-template-child-documents.md) | `GET /v2/templates/:templateId/filled_documents` | [docs](https://pdffiller.readme.io/reference/get_v2-templates-template-id-filled-documents) |
| [List Template Fields](actions/list-template-fields.md) | `GET /v2/templates/:templateId/fields` | [docs](https://pdffiller.readme.io/reference/get_v2-templates-template-id-fields) |
| [List Template Previews](actions/list-template-previews.md) | `GET /v2/templates/:templateId/previews` | [docs](https://pdffiller.readme.io/reference/get_v2-templates-template-id-previews) |
| [List Templates](actions/list-templates.md) | `GET /v2/templates` | [docs](https://pdffiller.readme.io/reference/get_v2-templates) |
| [Update Fillable Form](actions/update-fillable-form.md) | `PUT /v2/fillable_forms/:linkToFillId` | [docs](https://pdffiller.readme.io/reference/put_v2-fillable-forms-link-to-fill-id) |
| [Update Template](actions/update-template.md) | `PUT /v2/templates/:templateId` | [docs](https://pdffiller.readme.io/reference/put_v2-templates-template-id) |
