# <img src="https://images.mindcloud.co/apps/icons/favicon_1775481859052.png" alt="Realcrux logo" width="28" height="28"> Realcrux: Universal API

Realcrux is a Sendcrux-powered cold email outreach and deliverability platform for managing mailing lists, campaigns, and outreach workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/realcrux/latest
- **Category:** Communication / Email Communications
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.realcrux.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Mail Lists](actions/list-mail-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/list-mail-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get Mail List](actions/get-mail-list.md) | GET |  |
| [List Mail Lists](actions/list-mail-lists.md) | GET |  |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE |  |
| [Find Subscriber By Email](actions/find-subscriber-by-email.md) | GET |  |
| [Upsert Subscriber](actions/upsert-subscriber.md) | POST |  |

