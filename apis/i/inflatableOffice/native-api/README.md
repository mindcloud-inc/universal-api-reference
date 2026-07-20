# InflatableOffice: Native API Reference

A consolidated summary of InflatableOffice's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://rental.software/support/knowledge-base/articles/api
- **API base URL:** `https://rental.software/api6`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://rental.software/support/knowledge-base/article/api-setup-access)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `items`.

## Pagination

Use `limit` in the query string to set the page size (default 25). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://rental.software/support/knowledge-base/article/api-customers) |
| [Create Journal Entry](actions/create-journal-entry.md) | `POST /journals` | [docs](https://rental.software/support/knowledge-base/article/api-journal-create) |
| [Create Lead](actions/create-lead.md) | `POST /leads` | [docs](https://rental.software/support/knowledge-base/article/api-leads) |
| [Create Payment](actions/create-payment.md) | `POST /handle_payment` | [docs](https://rental.software/support/knowledge-base/article/api-payments-create) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://rental.software/support/knowledge-base/article/api-tasks-create) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:customerId` | [docs](https://rental.software/support/knowledge-base/article/api-customers-retrieve-details) |
| [Get Detailed Lead](actions/get-detailed-lead.md) | `GET /leads/:leadId` | [docs](https://rental.software/support/knowledge-base/article/api-leads-retrieve-lead) |
| [Get Lead](actions/get-lead.md) | `GET /leads/:leadId` | [docs](https://rental.software/support/knowledge-base/article/api-leads-retrieve-lead) |
| [Get Packing List For Lead](actions/get-packing-list-for-lead.md) | `GET /packinglists` | [docs](https://rental.software/support/knowledge-base/article/api-packing-lists-retrieve-details-or-update) |
| [Get Packing List Item Status History](actions/get-packing-list-item-status-history.md) | `GET /packinglists` | [docs](https://rental.software/support/knowledge-base/article/api-packing-lists-retrieve-details-or-update) |
| [Get Packing List Statuses](actions/get-packing-list-statuses.md) | `GET /packinglists` | [docs](https://rental.software/support/knowledge-base/article/api-packing-lists-retrieve-details-or-update) |
| [Get Rental](actions/get-rental.md) | `GET /rentals/:rentalId` | [docs](https://rental.software/support/knowledge-base/article/api-rentals-retrieve-details) |
| [Get Rental With Price Details](actions/get-rental-with-price-details.md) | `GET /rentals/:rentalId` | [docs](https://rental.software/support/knowledge-base/article/api-rentals-retrieve-details) |
| [Get Worker](actions/get-worker.md) | `GET /workers/:workerId` | [docs](https://rental.software/support/knowledge-base/article/api-workers-retrieve-details) |
| [List Categories](actions/list-categories.md) | `GET /categories_list` | [docs](https://rental.software/support/knowledge-base/article/api-categories-list) |
| [List Categories By Location](actions/list-categories-by-location.md) | `GET /categories_list` | [docs](https://rental.software/support/knowledge-base/article/api-categories-list) |
| [List Categories By WordPress Sync](actions/list-categories-by-word-press-sync.md) | `GET /categories_list` | [docs](https://rental.software/support/knowledge-base/article/api-categories-list) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://rental.software/support/knowledge-base/article/api-customers-retrieve-list) |
| [List Detailed Customers](actions/list-detailed-customers.md) | `GET /customers` | [docs](https://rental.software/support/knowledge-base/article/api-customers-retrieve-list) |
| [List Detailed Leads](actions/list-detailed-leads.md) | `GET /leads` | [docs](https://rental.software/support/knowledge-base/article/api-leads-list) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://rental.software/support/knowledge-base/article/api-leads-list) |
| [List Leads By Saved Filter](actions/list-leads-by-saved-filter.md) | `GET /leads` | [docs](https://rental.software/support/knowledge-base/article/api-leads-list) |
| [List Rentals](actions/list-rentals.md) | `GET /rentals` | [docs](https://rental.software/support/knowledge-base/article/api-rentals-list) |
| [List Rentals By Category](actions/list-rentals-by-category.md) | `GET /rentals` | [docs](https://rental.software/support/knowledge-base/article/api-rentals-list) |
| [List Rentals For Quote Page / Brand](actions/list-rentals-for-quote-page-brand.md) | `GET /rentals` | [docs](https://rental.software/support/knowledge-base/article/api-rentals-list) |
| [List Rentals With Price Details](actions/list-rentals-with-price-details.md) | `GET /rentals` | [docs](https://rental.software/support/knowledge-base/article/api-rentals-list) |
| [List Vehicles](actions/list-vehicles.md) | `GET /workers` | [docs](https://rental.software/support/knowledge-base/article/api-workers-retrieve-list) |
| [List Workers](actions/list-workers.md) | `GET /workers` | [docs](https://rental.software/support/knowledge-base/article/api-workers-retrieve-list) |
| [Send MMS](actions/send-mms.md) | `POST /text` | [docs](https://rental.software/support/knowledge-base/article/api-sms-text-message-sending-and-recieving) |
| [Send SMS](actions/send-sms.md) | `POST /text` | [docs](https://rental.software/support/knowledge-base/article/api-sms-text-message-sending-and-recieving) |
| [Update Customer](actions/update-customer.md) | `POST /customers/:customerId` | [docs](https://rental.software/support/knowledge-base/article/api-customers) |
| [Update Lead](actions/update-lead.md) | `POST /leads/:leadId` | [docs](https://rental.software/support/knowledge-base/article/api-leads) |
| [Update SMS Callback Tracking Variant](actions/update-sms-callback-tracking-variant.md) | `POST /text` | [docs](https://rental.software/support/knowledge-base/article/api-sms-text-message-sending-and-recieving) |
