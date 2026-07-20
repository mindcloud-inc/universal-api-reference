# <img src="https://images.mindcloud.co/apps/icons/favicon-9_1775148427280.png" alt="Sign Customiser logo" width="28" height="28"> Sign Customiser: Universal API

Design custom signs, sync orders, and manage integration webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/signCustomiser/latest
- **Category:** Commerce
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.signcustomiser.com/
- **Vendor API docs:** https://www.signcustomiser.com/help/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Webhooks](actions/list-webhooks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook subscription in Sign Customiser. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook subscription from Sign Customiser. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook subscription from Sign Customiser. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves all webhook subscriptions from Sign Customiser. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook subscription in Sign Customiser. |

