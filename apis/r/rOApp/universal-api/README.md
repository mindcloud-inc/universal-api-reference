# <img src="https://images.mindcloud.co/apps/icons/r-oapp_1774360648272.png" alt="RO App logo" width="28" height="28"> RO App: Universal API

RO App is a field-service and operations platform for managing contacts, bookings, estimates, orders, invoices, employees, and company data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rOApp/latest
- **Category:** Commerce
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://web.roapp.io
- **Vendor API docs:** https://roapp.readme.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company](actions/get-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST |  |
| [Get Booking](actions/get-booking.md) | GET |  |
| [List Bookings](actions/list-bookings.md) | GET |  |
| [Update Booking](actions/update-booking.md) | PUT |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [List Employees](actions/list-employees.md) | GET |  |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST |  |
| [Get Estimate](actions/get-estimate.md) | GET |  |
| [List Estimates](actions/list-estimates.md) | GET |  |
| [Update Estimate](actions/update-estimate.md) | PUT |  |

### Estimate Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate Item](actions/create-estimate-item.md) | POST |  |
| [List Estimate Items](actions/list-estimate-items.md) | GET |  |
| [Update Estimate Item](actions/update-estimate-item.md) | PUT |  |

### Estimate Status

| Action | Method | Description |
| --- | --- | --- |
| [List Estimate Statuses](actions/list-estimate-statuses.md) | GET |  |
| [Update Estimate Status](actions/update-estimate-status.md) | PUT |  |

### Estimate Type

| Action | Method | Description |
| --- | --- | --- |
| [List Estimate Types](actions/list-estimate-types.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoice Items](actions/list-invoice-items.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Invoice Status

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Statuses](actions/list-invoice-statuses.md) | GET |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST |  |
| [Get Order](actions/get-order.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |
| [Update Order](actions/update-order.md) | PUT |  |

### Order Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Order Item](actions/create-order-item.md) | POST |  |
| [List Order Items](actions/list-order-items.md) | GET |  |
| [Update Order Item](actions/update-order-item.md) | PUT |  |

### Order Status

| Action | Method | Description |
| --- | --- | --- |
| [List Order Statuses](actions/list-order-statuses.md) | GET |  |
| [Update Order Status](actions/update-order-status.md) | PUT |  |

### Order Type

| Action | Method | Description |
| --- | --- | --- |
| [List Order Types](actions/list-order-types.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST |  |
| [Get Organization](actions/get-organization.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET |  |
| [Update Organization](actions/update-organization.md) | PUT |  |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST |  |
| [Get Person](actions/get-person.md) | GET |  |
| [List People](actions/list-people.md) | GET |  |
| [Update Person](actions/update-person.md) | PUT |  |

### Tax

| Action | Method | Description |
| --- | --- | --- |
| [List Taxes](actions/list-taxes.md) | GET |  |

