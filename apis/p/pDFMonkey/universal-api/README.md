# <img src="https://images.mindcloud.co/apps/icons/p-dfmonkey_1772836080659.png" alt="PDFMonkey logo" width="28" height="28"> PDFMonkey: Universal API

Generate PDFs, manage templates, preview documents, and automate delivery.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pDFMonkey/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pdfmonkey.io
- **Vendor API docs:** https://pdfmonkey.io/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a document asynchronously in PDFMonkey. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from PDFMonkey. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from PDFMonkey. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in PDFMonkey. |

### Document Card

| Action | Method | Description |
| --- | --- | --- |
| [Generate Document Synchronously](actions/generate-document-synchronously.md) | POST | Generates a document synchronously in PDFMonkey. |
| [Get Document Card](actions/get-document-card.md) | GET | Retrieves a document card from PDFMonkey. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from PDFMonkey. |

### Document Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a template in PDFMonkey. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from PDFMonkey. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from PDFMonkey. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in PDFMonkey. |

### Document Template Card

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from PDFMonkey. |

### Pdf Engine

| Action | Method | Description |
| --- | --- | --- |
| [List PDF Engines](actions/list-pdf-engines.md) | GET | Retrieves PDF engines from PDFMonkey. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from PDFMonkey. |

