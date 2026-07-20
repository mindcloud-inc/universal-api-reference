# <img src="https://images.mindcloud.co/apps/icons/1653088104020_1770141968405.jpeg" alt="Extensiv Order Manager logo" width="28" height="28"> Extensiv Order Manager: Universal API

Extensiv Order Manager, formerly Skubana, manages ecommerce orders, shipments, inventory, listings, and fulfillment operations through the Order Manager API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/extensiv/latest
- **Category:** Commerce
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.extensiv.com/extensiv-order-manager
- **Vendor API docs:** https://documentation.skubana.com/pages/order-manager.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Orders](actions/list-orders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Product Listings](actions/list-product-listings.md) | GET | Retrieves product listings from Extensiv Order Manager. |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates orders in Extensiv Order Manager. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Extensiv Order Manager. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Extensiv Order Manager. |
| [Update Orders](actions/update-orders.md) | POST | Updates orders in Extensiv Order Manager. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Create External Shipment](actions/create-external-shipment.md) | POST | Creates an external shipment in Extensiv Order Manager. |
| [Create Standard Shipment](actions/create-standard-shipment.md) | POST | Creates a standard shipment in Extensiv Order Manager. |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves shipments from Extensiv Order Manager. |

