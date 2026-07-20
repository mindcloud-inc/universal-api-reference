# <img src="https://images.mindcloud.co/apps/icons/parsio_1773857313532.png" alt="Parsio logo" width="28" height="28"> Parsio: Universal API

Parse emails, documents, and PDFs into structured data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/parsio/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.parsio.io
- **Vendor API docs:** https://help.parsio.io/public-api/parsio-public-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Mailboxes](actions/list-mailboxes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/list-mailboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Collected Email

| Action | Method | Description |
| --- | --- | --- |
| [List Collected Emails](actions/list-collected-emails.md) | GET |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create HTML or Text Document](actions/create-html-or-text-document.md) | POST |  |
| [Get Document](actions/get-document.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET |  |
| [Parse Document](actions/parse-document.md) | PUT |  |
| [Skip Documents](actions/skip-documents.md) | PUT |  |
| [Upload Document File](actions/upload-document-file.md) | POST |  |

### Mailbox

| Action | Method | Description |
| --- | --- | --- |
| [Create Mailbox](actions/create-mailbox.md) | POST |  |
| [Delete Mailbox](actions/delete-mailbox.md) | DELETE |  |
| [Get Mailbox](actions/get-mailbox.md) | GET |  |
| [List Mailboxes](actions/list-mailboxes.md) | GET |  |
| [Update Mailbox](actions/update-mailbox.md) | PUT |  |

### Parsed Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Parsed Data](actions/get-parsed-data.md) | GET |  |

### Table Field

| Action | Method | Description |
| --- | --- | --- |
| [List Table Fields](actions/list-table-fields.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Delete Templates](actions/delete-templates.md) | DELETE |  |
| [Disable Templates](actions/disable-templates.md) | PUT |  |
| [Enable Templates](actions/enable-templates.md) | PUT |  |
| [Get Template](actions/get-template.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhooks](actions/delete-webhooks.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

