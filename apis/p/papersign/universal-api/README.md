# <img src="https://images.mindcloud.co/apps/icons/papersign_1774455599114.png" alt="Papersign logo" width="28" height="28"> Papersign: Universal API

Send, sign, and manage documents with Papersign

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/papersign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://papersign.com/
- **Vendor API docs:** https://paperform.readme.io/reference/getting-started-1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Papersign Spaces](actions/list-papersign-spaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/papersign/latest/actions/list-papersign-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Papersign Document

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Papersign Document](actions/cancel-papersign-document.md) | PUT |  |
| [Copy Papersign Document](actions/copy-papersign-document.md) | POST |  |
| [Get Papersign Document](actions/get-papersign-document.md) | GET |  |
| [List Papersign Documents](actions/list-papersign-documents.md) | GET |  |
| [Move Papersign Document](actions/move-papersign-document.md) | PUT |  |
| [Send Papersign Document](actions/send-papersign-document.md) | PUT |  |

### Papersign Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Papersign Folder](actions/create-papersign-folder.md) | POST |  |
| [List Papersign Folders](actions/list-papersign-folders.md) | GET |  |

### Papersign Folder Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Papersign Folder Webhook](actions/create-papersign-folder-webhook.md) | POST |  |
| [Delete Papersign Folder Webhook](actions/delete-papersign-folder-webhook.md) | DELETE |  |
| [List Papersign Folder Webhooks](actions/list-papersign-folder-webhooks.md) | GET |  |
| [Update Papersign Folder Webhook](actions/update-papersign-folder-webhook.md) | PUT |  |

### Papersign Space

| Action | Method | Description |
| --- | --- | --- |
| [List Papersign Spaces](actions/list-papersign-spaces.md) | GET |  |

