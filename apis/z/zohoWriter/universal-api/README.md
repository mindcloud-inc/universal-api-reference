# <img src="https://images.mindcloud.co/apps/icons/zoho-writer-logo_1775233594834.png" alt="Zoho Writer logo" width="28" height="28"> Zoho Writer: Universal API

Create, merge, combine, sign, and manage Writer documents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoWriter/latest
- **Category:** Content & Files / Storage
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/writer/
- **Vendor API docs:** https://www.zoho.com/writer/help/api/v1/getting-started.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Documents](actions/list-documents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Copy Document](actions/copy-document.md) | POST | Creates a copy of a document in Zoho Writer. |
| [Create/Upload Documents](actions/create-upload-documents.md) | POST | Creates or uploads a document in Zoho Writer. |
| [Delete Document Permanently](actions/delete-document-permanently.md) | DELETE | Deletes a document permanently from Zoho Writer. |
| [Download Document](actions/download-document.md) | GET | Downloads a document from Zoho Writer. |
| [Get All Fields](actions/get-all-fields.md) | GET | Retrieves all fields from a Zoho Writer document. |
| [Get Document Details](actions/get-document-details.md) | GET | Retrieves document details from Zoho Writer. |
| [Get Document Metrics](actions/get-document-metrics.md) | GET | Retrieves document metrics from Zoho Writer. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Zoho Writer. |
| [Rename Document](actions/rename-document.md) | PUT | Renames a document in Zoho Writer. |
| [Restore Document](actions/restore-document.md) | PUT | Restores a document in Zoho Writer. |
| [Trash Document](actions/trash-document.md) | DELETE | Moves a document to trash in Zoho Writer. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Combine And Deliver Via Webhook](actions/combine-and-deliver-via-webhook.md) | POST | Combines documents and delivers them via webhook in Zoho Writer. |
| [Combine And Store](actions/combine-and-store.md) | POST | Combines documents and stores them in Zoho Writer. |
| [Enable Or Disable Track Changes](actions/enable-or-disable-track-changes.md) | PUT | Enables or disables track changes in Zoho Writer. |
| [Lock Or Unlock Document](actions/lock-or-unlock-document.md) | PUT | Locks or unlocks a document in Zoho Writer. |
| [Merge And Email](actions/merge-and-email.md) | POST | Merges a document and emails it in Zoho Writer. |
| [Merge and Store V2](actions/merge-and-store-v2.md) | POST | Merges a document and stores it in Zoho Writer. |
| [Merge Document](actions/merge-document.md) | POST | Merges a document in Zoho Writer. |
| [Publish Document](actions/publish-document.md) | PUT | Publishes a document in Zoho Writer. |
| [Search Documents](actions/search-documents.md) | GET | Finds documents in Zoho Writer. |
| [Unpublish Document](actions/unpublish-document.md) | PUT | Unpublishes a document in Zoho Writer. |
| [Update Document Description](actions/update-document-description.md) | PUT | Updates a document description in Zoho Writer. |

### Fillable Template

| Action | Method | Description |
| --- | --- | --- |
| [List Fillable Templates](actions/list-fillable-templates.md) | GET | Retrieves fillable templates from Zoho Writer. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from Zoho Writer. |

### Merge Template

| Action | Method | Description |
| --- | --- | --- |
| [List Merge Templates](actions/list-merge-templates.md) | GET | Retrieves merge templates from Zoho Writer. |

### Sign Template

| Action | Method | Description |
| --- | --- | --- |
| [List Sign Templates](actions/list-sign-templates.md) | GET | Retrieves sign templates from Zoho Writer. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a template in Zoho Writer. |
| [Get Template Details](actions/get-template-details.md) | GET | Retrieves template details from Zoho Writer. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Zoho Writer. |

