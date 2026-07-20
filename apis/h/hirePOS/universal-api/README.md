# <img src="https://images.mindcloud.co/apps/icons/hire-pos_1774459836857.png" alt="HirePOS logo" width="28" height="28"> HirePOS: Universal API

Manage hire rentals, bookings, invoices, and equipment availability

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hirePOS/latest
- **Category:** Commerce / ERP
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hirepos.com.au/
- **Vendor API docs:** https://docs.hirepos.com/en/categories/524033-hirepos-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Authenticate](actions/authenticate.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/authenticate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Availability Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Availability](actions/get-availability.md) | GET | Retrieves item availability from HirePOS for a date range. |

### Business

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | GET | Validates API credentials for a HirePOS account. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in HirePOS. |

### Dispatched Item

| Action | Method | Description |
| --- | --- | --- |
| [List Dispatched Today](actions/list-dispatched-today.md) | GET | Retrieves items dispatched today from HirePOS. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Delivery Pickup Status](actions/get-delivery-pickup-status.md) | GET | Retrieves delivery and pickup status for an invoice from HirePOS. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [List Items](actions/list-items.md) | GET | Finds items in HirePOS by item search fields. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in HirePOS. |

### Package

| Action | Method | Description |
| --- | --- | --- |
| [Get Package](actions/get-package.md) | GET | Finds a package in HirePOS by package code. |

### Returned Item

| Action | Method | Description |
| --- | --- | --- |
| [List Returned Today](actions/list-returned-today.md) | GET | Retrieves items returned today from HirePOS. |

### Sales Stock Level

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Stock Levels](actions/list-sales-stock-levels.md) | GET | Retrieves sales stock levels from HirePOS as a CSV feed. |

### Website Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Website Booking](actions/create-website-booking.md) | POST | Creates a new website booking in HirePOS. |
| [Get Website Booking](actions/get-website-booking.md) | GET | Retrieves a website booking from HirePOS by ID. |

### Website Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Last Website Order](actions/get-last-website-order.md) | GET | Retrieves a customer's last website order from HirePOS by email. |

