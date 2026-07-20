# <img src="https://images.mindcloud.co/apps/icons/prodigi_1776713180663.png" alt="Prodigi logo" width="28" height="28"> Prodigi: Universal API

Prodigi is a print-on-demand fulfillment platform for creating orders, checking order status, quoting product and shipping costs, and looking up product details through the Prodigi Print API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/prodigi/latest
- **Category:** Commerce
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.prodigi.com/
- **Vendor API docs:** https://www.prodigi.com/print-api/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Orders](actions/list-orders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Actions](actions/get-order-actions.md) | GET | Retrieves available actions for a Prodigi order. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | PUT | Cancels a specific order in Prodigi. |
| [Create Order](actions/create-order.md) | POST | Creates and submits a new order in Prodigi. |
| [Get Order](actions/get-order.md) | GET | Retrieves details for a specific Prodigi order. |
| [List Orders](actions/list-orders.md) | GET | Retrieves a list of orders from Prodigi. |
| [Update Order Metadata](actions/update-order-metadata.md) | PUT | Updates metadata for a Prodigi order. |
| [Update Order Recipient](actions/update-order-recipient.md) | PUT | Updates recipient details for a Prodigi order. |
| [Update Order Shipping Method](actions/update-order-shipping-method.md) | PUT | Updates the shipping method for a Prodigi order. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Photobook Spine Details](actions/get-photobook-spine-details.md) | GET | Retrieves the required spine width for a Prodigi photobook. |
| [Get Product Details](actions/get-product-details.md) | GET | Retrieves details for a specific Prodigi product SKU. |

### Quotes

| Action | Method | Description |
| --- | --- | --- |
| [Create Quote](actions/create-quote.md) | GET | Retrieves Prodigi quotes for product and shipping costs. |

