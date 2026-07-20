# <img src="https://images.mindcloud.co/apps/icons/mendato_1774461620874.png" alt="Mendato logo" width="28" height="28"> Mendato: Universal API

Mendato is a field service and business operations platform for cleaning and facility-service teams, covering customers, employees, objects, orders, operations, tickets, estimates, invoices, and time records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mendato/latest
- **Category:** Support / Field Service
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mendato.com/
- **Vendor API docs:** https://developers.mendato.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company](actions/get-company.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [Get Operation](actions/get-operation.md) | GET |  |
| [List Operations](actions/list-operations.md) | GET |  |
| [List Unassigned Operations](actions/list-unassigned-operations.md) | GET |  |

### Attendance Records

| Action | Method | Description |
| --- | --- | --- |
| [List Time Records](actions/list-time-records.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Get Customer](actions/get-customer.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee](actions/get-employee.md) | GET |  |
| [Get Next Employee Personnel Number](actions/get-next-employee-personnel-number.md) | GET |  |
| [List Employees](actions/list-employees.md) | GET |  |

### Estimates

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST |  |
| [Get Estimate](actions/get-estimate.md) | GET |  |
| [List Estimates](actions/list-estimates.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Object](actions/get-object.md) | GET |  |
| [List Objects](actions/list-objects.md) | GET |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket](actions/get-ticket.md) | GET |  |
| [List Tickets](actions/list-tickets.md) | GET |  |

