# OrderOut: Native API Reference

A consolidated summary of OrderOut's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://developers.orderout.co/reference
- **API base URL:** `https://api.orderout.co`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
api-key: <apiKey>
```

[Official authentication documentation](https://developers.orderout.co/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST /api/pos/account` | [docs](https://developers.orderout.co/reference/create-account) |
| [Create Push Menu Webhook](actions/create-push-menu-webhook.md) | `POST /api/webhooks/push_menu` | [docs](https://developers.orderout.co/reference/create-push_menu-webhook) |
| [Create Push Order Webhook](actions/create-push-order-webhook.md) | `POST /api/webhooks/push_order` | [docs](https://developers.orderout.co/reference/create-push_order-webhook) |
| [Delete Push Menu Webhook](actions/delete-push-menu-webhook.md) | `DELETE /api/webhooks/push_menu/:delivery_service_type` | [docs](https://developers.orderout.co/reference/delete-push_menu-webhook-1) |
| [Delete Push Order Webhook](actions/delete-push-order-webhook.md) | `DELETE /api/webhooks/push_order/:push_order_webhook_id` | [docs](https://developers.orderout.co/reference/delete-push_order-webhook-1) |
| [Get Quotes](actions/get-quotes.md) | `POST /v2/delivery/quotes` | [docs](https://developers.orderout.co/reference/delivery-get-quotes) |
| [List Accounts](actions/list-accounts.md) | `GET /api/pos/account/` | [docs](https://developers.orderout.co/reference/list-accounts) |
| [List Restaurants](actions/list-restaurants.md) | `GET /api/pos/restaurant/` | [docs](https://developers.orderout.co/reference/list-restaurants) |
| [Push Order](actions/push-order.md) | `POST /api/channel/order/push` | [docs](https://developers.orderout.co/reference/push-order-from-channel-to-orderout) |
| [Update Integration Name](actions/update-integration-name.md) | `POST /api/integrator/update_name` | [docs](https://developers.orderout.co/reference/update-integration-name) |
