# <img src="https://images.mindcloud.co/apps/icons/xps-ship-icon_1776714454329.png" alt="XPS Ship logo" width="28" height="28"> XPS Ship: Universal API

XPS Ship is an eCommerce shipping API for retrieving services and quotes, managing eCommerce orders, retrieving shipment and label data, searching shipments, and managing order tags.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/xPSShip/latest
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://xpsship.com
- **Vendor API docs:** https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/overview/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Services](actions/list-services.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Integrated Quoting Option

| Action | Method | Description |
| --- | --- | --- |
| [List Integrated Quoting Options](actions/list-integrated-quoting-options.md) | GET | Retrieves integrated quoting options from XPS Ship. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Delete Order](actions/delete-order.md) | DELETE | Deletes an existing order from XPS Ship. |
| [Put Order](actions/put-order.md) | PUT | Creates or updates an order in XPS Ship. |

### Order Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Order Tags](actions/list-order-tags.md) | GET | Retrieves order tags from XPS Ship. |

### Order Tag Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Assign Tags to Order](actions/assign-tags-to-order.md) | PUT | Assigns tags to an order in XPS Ship. |
| [Unassign Tags from Order](actions/unassign-tags-from-order.md) | PUT | Unassigns tags from an order in XPS Ship. |

### Request For Quote

| Action | Method | Description |
| --- | --- | --- |
| [Create Quote](actions/create-quote.md) | POST | Creates a shipping quote in XPS Ship. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [List Services](actions/list-services.md) | GET | Retrieves shipping services from XPS Ship. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Shipment](actions/retrieve-shipment.md) | GET | Retrieves a shipment from XPS Ship. |
| [Retrieve Shipments](actions/retrieve-shipments.md) | GET | Retrieves shipments from XPS Ship. |
| [Search Shipments](actions/search-shipments.md) | GET | Finds booked shipments in XPS Ship by keyword. |

### Shipping Label

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Shipping Label](actions/retrieve-shipping-label.md) | GET | Retrieves a shipping label from XPS Ship. |

