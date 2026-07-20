# <img src="https://images.mindcloud.co/apps/icons/laposta_1774888684329.png" alt="Laposta logo" width="28" height="28"> Laposta: Universal API

Manage subscribers, lists, campaigns, and newsletter data in Laposta

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/laposta/latest
- **Category:** Communication / Email Communications
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.laposta.org
- **Vendor API docs:** https://api.laposta.nl/doc/index.en.php

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a custom field in Laposta. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes an existing custom field from Laposta. |
| [Get Field](actions/get-field.md) | GET | Retrieves a custom field from Laposta. |
| [List Fields](actions/list-fields.md) | GET | Retrieves custom fields from Laposta. |
| [Update Field](actions/update-field.md) | PUT | Updates an existing custom field in Laposta. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in Laposta. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes an existing list from Laposta. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from Laposta. |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from Laposta. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in Laposta. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from Laposta. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in Laposta. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes an existing subscriber from Laposta. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber from Laposta. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from Laposta. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in Laposta. |

