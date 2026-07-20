# <img src="https://images.mindcloud.co/apps/icons/flexport-icon_1776719782973.png" alt="Flexport logo" width="28" height="28"> Flexport: Universal API

Flexport is a logistics platform for managing shipments, bookings, purchase orders, products, invoices, documents, customs data, and network resources through Flexport's public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/flexport/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.flexport.com
- **Vendor API docs:** https://apidocs.flexport.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Shipments](actions/list-shipments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexport/latest/actions/list-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from your Flexport account. |
| [Retrieve Booking](actions/retrieve-booking.md) | GET | Retrieves a booking from your Flexport account. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Flexport. |
| [List Products](actions/list-products.md) | GET | Retrieves products for a client from Flexport. |
| [Retrieve Product](actions/retrieve-product.md) | GET | Retrieves a product from your Flexport account. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Flexport. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [List Containers](actions/list-containers.md) | GET | Retrieves containers from your Flexport account. |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves shipments from your Flexport account. |
| [Retrieve Container](actions/retrieve-container.md) | GET | Retrieves a container from your Flexport account. |
| [Retrieve Shipment](actions/retrieve-shipment.md) | GET | Retrieves a shipment from your Flexport account. |
| [Update Shipment](actions/update-shipment.md) | PUT | Updates an existing shipment in Flexport. |

