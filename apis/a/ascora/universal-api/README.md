# <img src="https://images.mindcloud.co/apps/icons/ascora_1774385046446.png" alt="Ascora logo" width="28" height="28"> Ascora: Universal API

Ascora: Manage leads, quotes, jobs, inventory, invoicing, and reporting

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ascora/latest
- **Category:** Support / Field Service
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ascora.com.au
- **Vendor API docs:** https://support.ascora.com.au/display/AS/API+Endpoints

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Labour Roles](actions/list-labour-roles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-labour-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Upsert Contact](actions/upsert-contact.md) | POST | Creates or updates a contact in Ascora. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Ascora. |

### Enquiry

| Action | Method | Description |
| --- | --- | --- |
| [Create Enquiry](actions/create-enquiry.md) | POST | Creates a new enquiry in Ascora. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoices To Send](actions/get-invoices-to-send.md) | GET | Retrieves customer invoices ready to send from Ascora. |
| [Mark Invoices Sent](actions/mark-invoices-sent.md) | PUT | Marks invoices as sent in Ascora. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST | Creates a new job in Ascora. |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from Ascora. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from Ascora. |

### Labour Role

| Action | Method | Description |
| --- | --- | --- |
| [List Labour Roles](actions/list-labour-roles.md) | GET | Retrieves available labour roles from Ascora. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Quote Sections](actions/add-quote-sections.md) | PUT | Adds sections to a quote in Ascora. |
| [Clear Quote Items](actions/clear-quote-items.md) | PUT | Clears items from a quote in Ascora. |
| [Delete Quote Or Section](actions/delete-quote-or-section.md) | DELETE | Deletes a quote or quote section from Ascora. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Ascora. |
| [Get Quote](actions/get-quote.md) | GET | Retrieves a quote from Ascora. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Ascora. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Ascora. |
| [List Contacts For Customer](actions/list-contacts-for-customer.md) | GET | Retrieves contacts for a customer from Ascora. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Ascora. |
| [List Kits](actions/list-kits.md) | GET | Retrieves kits from Ascora. |
| [List Quotes](actions/list-quotes.md) | GET | Retrieves quotes from Ascora. |
| [List Supplies](actions/list-supplies.md) | GET | Retrieves supplies from Ascora. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Ascora. |
| [Update Quote Status](actions/update-quote-status.md) | PUT | Updates the status of a quote in Ascora. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment](actions/create-payment.md) | POST | Creates a new payment in Ascora. |
| [Get Payments To Send](actions/get-payments-to-send.md) | GET | Retrieves payments ready to send from Ascora. |
| [Mark Payments Sent](actions/mark-payments-sent.md) | PUT | Marks payments as sent in Ascora. |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Add Kits To Quote](actions/add-kits-to-quote.md) | PUT | Adds kits to a quote in Ascora. |
| [Add Labour To Quote](actions/add-labour-to-quote.md) | PUT | Adds labour items to a quote in Ascora. |
| [Add Supplies To Quote](actions/add-supplies-to-quote.md) | PUT | Adds supplies to a quote in Ascora. |
| [Add Write-Ins To Quote](actions/add-write-ins-to-quote.md) | PUT | Adds write-ins to a quote in Ascora. |
| [Create Full Section-Based Quote](actions/create-full-section-based-quote.md) | POST | Creates a new section-based quote in Ascora. |
| [Create Quote](actions/create-quote.md) | POST | Creates a new quote in Ascora. |
| [Create Quote With Items](actions/create-quote-with-items.md) | POST | Creates a new quote with items in Ascora. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier](actions/create-supplier.md) | POST | Creates a new supplier in Ascora. |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from Ascora. |
| [Update Supplier](actions/update-supplier.md) | PUT | Updates an existing supplier in Ascora. |

### Supplier Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier Invoice](actions/create-supplier-invoice.md) | POST | Creates a new supplier invoice in Ascora. |
| [Get Supplier Invoice](actions/get-supplier-invoice.md) | GET | Retrieves a supplier invoice from Ascora. |
| [List Supplier Invoices](actions/list-supplier-invoices.md) | GET | Retrieves supplier invoices from Ascora. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a new webhook subscription in Ascora. |

