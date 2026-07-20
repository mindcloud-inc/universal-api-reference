# <img src="https://images.mindcloud.co/apps/icons/pres-engage_1774977039431.png" alt="PresEngage logo" width="28" height="28"> PresEngage: Universal API

Manage PresEngage webhooks and test message integrations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/presEngage/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://presengage.com
- **Vendor API docs:** https://developer.presengage.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/presEngage/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves authenticated user details from PresEngage. |

### Webhook Message

| Action | Method | Description |
| --- | --- | --- |
| [List Sample Webhook Messages](actions/list-sample-webhook-messages.md) | GET | Retrieves sample webhook message data from PresEngage for setup. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a new webhook subscription in PresEngage. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes an existing webhook subscription from PresEngage. |

