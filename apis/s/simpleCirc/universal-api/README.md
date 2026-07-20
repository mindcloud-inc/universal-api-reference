# <img src="https://images.mindcloud.co/apps/icons/simple-circ_1776371462234.png" alt="SimpleCirc logo" width="28" height="28"> SimpleCirc: Universal API

SimpleCirc helps magazine publishers manage subscribers, subscriptions, and mailing addresses.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/simpleCirc/latest
- **Category:** Support / Customer Success
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://simplecirc.com
- **Vendor API docs:** https://simplecirc.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Subscribers](actions/list-subscribers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleCirc/latest/actions/list-subscribers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Address](actions/create-or-update-address.md) | POST | Creates or updates a subscriber address in SimpleCirc. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in SimpleCirc. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves a list of subscribers from SimpleCirc. |
| [Retrieve Subscriber](actions/retrieve-subscriber.md) | GET | Retrieves details for a subscriber from SimpleCirc. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in SimpleCirc. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a subscription in SimpleCirc, or renews an existing one. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in SimpleCirc. |

