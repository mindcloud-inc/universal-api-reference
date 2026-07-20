# <img src="https://images.mindcloud.co/apps/icons/order-out_1775167665606.png" alt="OrderOut logo" width="28" height="28"> OrderOut: Universal API

OrderOut: Manage restaurant accounts, menus, orders, and delivery operations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/orderOut/latest
- **Category:** Commerce
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://orderout.co
- **Vendor API docs:** https://developers.orderout.co/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Restaurants](actions/list-restaurants.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/list-restaurants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Restaurants](actions/list-restaurants.md) | GET | Lists restaurants in OrderOut. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates an account in OrderOut. |
| [Create Push Menu Webhook](actions/create-push-menu-webhook.md) | POST | Creates a push menu webhook in OrderOut. |
| [Create Push Order Webhook](actions/create-push-order-webhook.md) | POST | Creates a push order webhook in OrderOut. |
| [Delete Push Menu Webhook](actions/delete-push-menu-webhook.md) | DELETE | Deletes a push menu webhook from OrderOut. |
| [Delete Push Order Webhook](actions/delete-push-order-webhook.md) | DELETE | Deletes a push order webhook from OrderOut. |
| [Get Quotes](actions/get-quotes.md) | GET | Retrieves delivery quotes from OrderOut. |
| [List Accounts](actions/list-accounts.md) | GET | Lists accounts in OrderOut. |
| [Push Order](actions/push-order.md) | POST | Pushes an order from a channel to OrderOut. |
| [Update Integration Name](actions/update-integration-name.md) | PUT | Updates the integration name in OrderOut. |

