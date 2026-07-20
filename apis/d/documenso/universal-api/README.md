# <img src="https://images.mindcloud.co/apps/icons/output-onlinepngtools_1775071732184.png" alt="Documenso logo" width="28" height="28"> Documenso: Universal API

Sign everywhere with Documenso to build document workflows, create templates, and integrate secure e-signature processes into the tools you already use.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/documenso/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://documenso.com/
- **Vendor API docs:** https://docs.documenso.com/docs/developers/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Documents](actions/list-documents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documenso/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Documenso. |
| [Create Document From Template](actions/create-document-from-template.md) | POST | Creates a document from a template in Documenso. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from Documenso. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Documenso. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Documenso. |
| [Send Document](actions/send-document.md) | PUT | Sends an existing document in Documenso. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in Documenso. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Fields](actions/create-fields.md) | POST | Creates fields in Documenso. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes an existing field from Documenso. |
| [Get Field](actions/get-field.md) | GET | Retrieves a field from Documenso. |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipients](actions/create-recipients.md) | POST | Creates recipients in Documenso. |
| [Delete Recipient](actions/delete-recipient.md) | DELETE | Deletes an existing recipient from Documenso. |
| [Get Recipient](actions/get-recipient.md) | GET | Retrieves a recipient from Documenso. |
| [Update Recipients](actions/update-recipients.md) | PUT | Updates existing recipients in Documenso. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Documenso. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from Documenso. |
| [Duplicate Template](actions/duplicate-template.md) | POST | Creates a duplicate template in Documenso. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Documenso. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Documenso. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Documenso. |

