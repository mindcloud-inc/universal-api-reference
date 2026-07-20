# <img src="https://images.mindcloud.co/apps/icons/download_1776711033851.png" alt="InflatableOffice logo" width="28" height="28"> InflatableOffice: Universal API

Manage rentals, customers, leads, workers, and payments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/inflatableOffice/latest
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://inflatableoffice.com
- **Vendor API docs:** https://rental.software/support/knowledge-base/articles/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from InflatableOffice. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories By Location](actions/list-categories-by-location.md) | GET | Retrieves categories for a location from InflatableOffice. |
| [List Categories By WordPress Sync](actions/list-categories-by-word-press-sync.md) | GET | Retrieves categories for a WordPress sync from InflatableOffice. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from InflatableOffice. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in InflatableOffice. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from InflatableOffice. |
| [List Detailed Customers](actions/list-detailed-customers.md) | GET | Retrieves customers with detailed fields from InflatableOffice. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in InflatableOffice. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Rental](actions/get-rental.md) | GET | Retrieves a rental from InflatableOffice. |
| [Get Rental With Price Details](actions/get-rental-with-price-details.md) | GET | Retrieves a rental with price details from InflatableOffice. |
| [List Rentals](actions/list-rentals.md) | GET | Retrieves rentals from InflatableOffice. |
| [List Rentals By Category](actions/list-rentals-by-category.md) | GET | Retrieves rentals by category from InflatableOffice. |
| [List Rentals With Price Details](actions/list-rentals-with-price-details.md) | GET | Retrieves rentals with price details from InflatableOffice. |

### Journal Entries

| Action | Method | Description |
| --- | --- | --- |
| [Create Journal Entry](actions/create-journal-entry.md) | POST | Creates a new journal entry in InflatableOffice. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in InflatableOffice. |
| [Get Detailed Lead](actions/get-detailed-lead.md) | GET | Retrieves a lead with detailed fields from InflatableOffice. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from InflatableOffice. |
| [List Detailed Leads](actions/list-detailed-leads.md) | GET | Retrieves leads with detailed fields from InflatableOffice. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from InflatableOffice. |
| [List Leads By Saved Filter](actions/list-leads-by-saved-filter.md) | GET | Retrieves leads by saved filter from InflatableOffice. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in InflatableOffice. |

### Mms Message

| Action | Method | Description |
| --- | --- | --- |
| [Send MMS](actions/send-mms.md) | POST | Sends an MMS message from InflatableOffice. |

### Packing List Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Packing List For Lead](actions/get-packing-list-for-lead.md) | GET | Retrieves packing list items for a lead from InflatableOffice. |

### Packing List Item Status History

| Action | Method | Description |
| --- | --- | --- |
| [Get Packing List Item Status History](actions/get-packing-list-item-status-history.md) | GET | Retrieves packing list item status history from InflatableOffice. |

### Packing List Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Packing List Statuses](actions/get-packing-list-statuses.md) | GET | Retrieves packing list statuses from InflatableOffice. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment](actions/create-payment.md) | POST | Creates a payment in InflatableOffice. |

### Rental

| Action | Method | Description |
| --- | --- | --- |
| [List Rentals For Quote Page / Brand](actions/list-rentals-for-quote-page-brand.md) | GET | Retrieves rentals for a quote page brand from InflatableOffice. |

### Sms Message

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS](actions/send-sms.md) | POST | Sends an SMS message from InflatableOffice. |

### Sms Message Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Update SMS Callback Tracking Variant](actions/update-sms-callback-tracking-variant.md) | POST | Sends a text message with callback tracking from InflatableOffice. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in InflatableOffice. |

### Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [List Vehicles](actions/list-vehicles.md) | GET | Retrieves vehicles from InflatableOffice. |

### Worker

| Action | Method | Description |
| --- | --- | --- |
| [Get Worker](actions/get-worker.md) | GET | Retrieves a worker from InflatableOffice. |
| [List Workers](actions/list-workers.md) | GET | Retrieves workers from InflatableOffice. |

