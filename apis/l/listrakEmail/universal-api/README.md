# <img src="https://images.mindcloud.co/apps/icons/favicon-www-listrak-com-64x64_1782479376848.png" alt="Listrak Email logo" width="28" height="28"> Listrak Email: Universal API

Manage contacts, campaigns, and email analytics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/listrakEmail/latest
- **Category:** Marketing
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.listrak.com
- **Vendor API docs:** https://api.listrak.com/email

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get List](actions/get-list.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listrakEmail/latest/actions/get-list?connectionId=$CONNECTION_ID&listID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get List](actions/get-list.md) | GET |  |
| [List Lists](actions/list-lists.md) | GET |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Message](actions/get-message.md) | GET |  |
| [Get Transactional Message](actions/get-transactional-message.md) | GET |  |
| [List Messages](actions/list-messages.md) | GET |  |
| [List Transactional Messages](actions/list-transactional-messages.md) | GET |  |

### Transactional Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Transactional Email](actions/send-transactional-email.md) | POST |  |

