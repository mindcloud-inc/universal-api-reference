# <img src="https://images.mindcloud.co/apps/icons/syncro_1773686860220.png" alt="Syncro logo" width="28" height="28"> Syncro: Universal API

Manage tickets, customers, contacts, invoices, and payments in Syncro

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/syncro/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://syncromsp.com/
- **Vendor API docs:** https://api-docs.syncromsp.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contact](actions/get-contact.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [List Assets](actions/list-assets.md) | GET | Retrieves a list of assets from Syncro. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Add Ticket Comment](actions/add-ticket-comment.md) | POST | Adds a comment to a ticket in Syncro. |
| [List Ticket Comments](actions/list-ticket-comments.md) | GET | Retrieves comments for a ticket from Syncro. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Syncro. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Syncro by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from Syncro. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Syncro. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from Syncro. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Syncro. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Syncro by ID. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Syncro. |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST | Creates a new estimate in Syncro. |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves a list of estimates from Syncro. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Convert Estimate To Invoice](actions/convert-estimate-to-invoice.md) | POST | Creates an invoice from an estimate in Syncro. |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Syncro. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Syncro by ID or number. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves a list of invoices from Syncro. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Syncro. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Add Ticket Line Item](actions/add-ticket-line-item.md) | POST | Creates a ticket line item in Syncro. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET | Retrieves a list of payments from Syncro. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in Syncro. |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket from Syncro by ID. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves a list of tickets from Syncro. |
| [Update Ticket](actions/update-ticket.md) | PUT | Updates an existing ticket in Syncro. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket Timer](actions/create-ticket-timer.md) | POST | Creates a ticket timer entry in Syncro. |

