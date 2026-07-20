# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-17-as-17_1776457183785.png" alt="SalesapCRM logo" width="28" height="28"> SalesapCRM: Universal API

SalesapCRM is a CRM API for managing contacts, companies, deals, orders, tasks, events, products, invoices, and related sales operations through Salesap's JSON:API REST interface.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/salesapCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://salesap.ru/
- **Vendor API docs:** https://api.salesap.ru/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Token](actions/get-current-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesapCRM/latest/actions/get-current-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a company in SalesapCRM. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes a company from SalesapCRM. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from SalesapCRM. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from SalesapCRM. |
| [Update Company](actions/update-company.md) | PUT | Updates a company in SalesapCRM. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in SalesapCRM. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from SalesapCRM. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from SalesapCRM. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from SalesapCRM. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in SalesapCRM. |

### Current Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Token](actions/get-current-token.md) | GET | Retrieves the current token details from SalesapCRM. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a deal in SalesapCRM. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes a deal from SalesapCRM. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a deal from SalesapCRM. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deals from SalesapCRM. |
| [Update Deal](actions/update-deal.md) | PUT | Updates a deal in SalesapCRM. |

### Diary Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Diary Event](actions/create-diary-event.md) | POST | Creates a diary event in SalesapCRM. |
| [Delete Diary Event](actions/delete-diary-event.md) | DELETE | Deletes a diary event from SalesapCRM. |
| [Get Diary Event](actions/get-diary-event.md) | GET | Retrieves a diary event from SalesapCRM. |
| [List Diary Events](actions/list-diary-events.md) | GET | Retrieves diary events from SalesapCRM. |
| [Update Diary Event](actions/update-diary-event.md) | PUT | Updates a diary event in SalesapCRM. |

### Diary Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Diary Task](actions/create-diary-task.md) | POST | Creates a diary task in SalesapCRM. |
| [Delete Diary Task](actions/delete-diary-task.md) | DELETE | Deletes a diary task from SalesapCRM. |
| [Get Diary Task](actions/get-diary-task.md) | GET | Retrieves a diary task from SalesapCRM. |
| [List Diary Tasks](actions/list-diary-tasks.md) | GET | Retrieves diary tasks from SalesapCRM. |
| [Update Diary Task](actions/update-diary-task.md) | PUT | Updates a diary task in SalesapCRM. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates an invoice in SalesapCRM. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from SalesapCRM. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from SalesapCRM. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an invoice in SalesapCRM. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates an order in SalesapCRM. |
| [Delete Order](actions/delete-order.md) | DELETE | Deletes an order from SalesapCRM. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from SalesapCRM. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from SalesapCRM. |
| [Update Order](actions/update-order.md) | PUT | Updates an order in SalesapCRM. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a product in SalesapCRM. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes a product from SalesapCRM. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from SalesapCRM. |
| [List Products](actions/list-products.md) | GET | Retrieves products from SalesapCRM. |
| [Update Product](actions/update-product.md) | PUT | Updates a product in SalesapCRM. |

