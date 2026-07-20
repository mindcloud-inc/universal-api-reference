# Shippify: Native API Reference

A consolidated summary of Shippify's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://docs.shippify.co/developers/en/shippify-api/first-steps
- **API base URL:** `https://api.shippify.co`

## Authentication

### Basic Auth

Use the APP ID and APP SECRET from Shippify company settings.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.shippify.co/developers/en/shippify-api/first-steps)

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Deliveries To Route](actions/add-deliveries-to-route.md) | `PATCH /v1/routes/add` |  |
| [Break Route](actions/break-route.md) | `PUT /v1/routes/destroy` |  |
| [Change Delivery Status](actions/change-delivery-status.md) | `PATCH /v1/deliveries/:id/status` |  |
| [Change Route Status](actions/change-route-status.md) | `PATCH /v1/routes/:id/status` |  |
| [Create Deliveries](actions/create-deliveries.md) | `POST /v1/deliveries` |  |
| [Create Route](actions/create-route.md) | `POST /v1/routes/create` |  |
| [Get Delivery Information](actions/get-delivery-information.md) | `GET /v1/deliveries/:id/complete` |  |
| [Get Delivery Quotes](actions/get-delivery-quotes.md) | `POST /v2/pricing/quotes/available` | [docs](https://docs.shippify.co/developers/en/shippify-api/deliveries/delivery-quotes) |
| [Get Route Information](actions/get-route-information.md) | `GET /v1/routes/:id` |  |
| [Get Tracking Link](actions/get-tracking-link.md) | `GET /v1/deliveries/token/:id` |  |
| [List Countries](actions/list-countries.md) | `GET /v1/country` | [docs](https://docs.shippify.co/developers/en/shippify-api/first-steps) |
| [Print Delivery Labels](actions/print-delivery-labels.md) | `POST /v2/integrations/deliveries/labels` |  |
| [Remove Deliveries From Route](actions/remove-deliveries-from-route.md) | `PATCH /v1/routes/remove` |  |
| [Update Delivery](actions/update-delivery.md) | `PATCH /v1/deliveries/dropoff` |  |
| [Update Pickup Point](actions/update-pickup-point.md) | `PATCH /v1/deliveries/pickup` |  |
