# <img src="https://images.mindcloud.co/apps/icons/clever-elements_1775239441212.png" alt="Clever Elements logo" width="28" height="28"> Clever Elements: Universal API

SOAP API wrapper for Clever Elements mailing lists, subscribers, newsletters, and custom subscriber fields.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cleverElements/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cleverelements.com/
- **Vendor API docs:** https://docs.cleverelements.com/kb/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber Field](actions/add-subscriber-field.md) | POST |  |
| [Delete Subscriber Field](actions/delete-subscriber-field.md) | DELETE |  |
| [List Subscriber Fields](actions/list-subscriber-fields.md) | GET |  |

### Email Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscriber History](actions/get-subscriber-history.md) | GET |  |
| [List Sent Newsletters](actions/list-sent-newsletters.md) | GET |  |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Add List](actions/add-list.md) | POST |  |
| [Delete List](actions/delete-list.md) | DELETE |  |
| [Get List Details](actions/get-list-details.md) | GET |  |
| [List Lists](actions/list-lists.md) | GET |  |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber](actions/add-subscriber.md) | POST |  |
| [Add Subscriber DOI](actions/add-subscriber-doi.md) | POST |  |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE |  |
| [Get Subscriber By Email](actions/get-subscriber-by-email.md) | GET |  |
| [List Newsletter Receivers](actions/list-newsletter-receivers.md) | GET |  |
| [List Subscriber Details](actions/list-subscriber-details.md) | GET |  |
| [List Subscribers](actions/list-subscribers.md) | GET |  |
| [List Unsubscribed Subscribers](actions/list-unsubscribed-subscribers.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriber Subscriptions](actions/list-subscriber-subscriptions.md) | GET |  |
| [Unsubscribe Subscriber From All Lists](actions/unsubscribe-subscriber-from-all-lists.md) | DELETE |  |
| [Unsubscribe Subscriber From List](actions/unsubscribe-subscriber-from-list.md) | DELETE |  |

