# <img src="https://images.mindcloud.co/apps/icons/happy-sms-icon-square_1775574122521.png" alt="Happy SMS logo" width="28" height="28"> Happy SMS: Universal API

Happy SMS lets you send SMS messages, inspect delivery status, manage custom-data documents, and read account balances through the official Happy SMS REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/happySMS/latest
- **Category:** Communication / Team Messaging
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sms.happy.nc
- **Vendor API docs:** https://www.happy.nc/docs/sms.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST |  |
| [Create Documents Batch](actions/create-documents-batch.md) | POST |  |
| [Delete Document](actions/delete-document.md) | DELETE |  |
| [Delete Documents Batch](actions/delete-documents-batch.md) | DELETE |  |
| [Get Document](actions/get-document.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET |  |
| [Update Document](actions/update-document.md) | PUT |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST |  |
| [Create Messages Batch](actions/create-messages-batch.md) | POST |  |
| [Delete Message](actions/delete-message.md) | DELETE |  |
| [Delete Messages Batch](actions/delete-messages-batch.md) | DELETE |  |
| [Get Message](actions/get-message.md) | GET |  |
| [List Messages](actions/list-messages.md) | GET |  |
| [Pop Messages](actions/pop-messages.md) | GET |  |
| [Search Messages](actions/search-messages.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET |  |

