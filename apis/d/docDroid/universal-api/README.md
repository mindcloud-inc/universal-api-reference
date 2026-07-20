# <img src="https://images.mindcloud.co/apps/icons/doc-droid_1774986889415.png" alt="DocDroid logo" width="28" height="28"> DocDroid: Universal API

Upload, share, manage, analyze, and subscribe to document webhooks in DocDroid.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docDroid/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.docdroid.com/
- **Vendor API docs:** https://www.docdroid.com/apidocs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List My Documents](actions/list-my-documents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docDroid/latest/actions/list-my-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from DocDroid. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from DocDroid by ID. |
| [List My Documents](actions/list-my-documents.md) | GET | Retrieves your uploaded documents from DocDroid. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in DocDroid. |
| [Upload Document](actions/upload-document.md) | POST | Uploads a new document to DocDroid. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in DocDroid. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from DocDroid. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from DocDroid by ID. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves your configured webhooks from DocDroid. |

