# <img src="https://images.mindcloud.co/apps/icons/eenvoudig-factureren_1776086488331.png" alt="EenvoudigFactureren logo" width="28" height="28"> EenvoudigFactureren: Universal API

EenvoudigFactureren provides invoicing, quotes, orders, customer, supplier, project, payment, and accounting document operations for Belgian billing workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eenvoudigFactureren/latest
- **Category:** Commerce / Accounting
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://eenvoudigfactureren.be
- **Vendor API docs:** https://help.eenvoudigfactureren.be/support/solutions/101000176283

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Account](actions/get-current-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account](actions/get-current-account.md) | GET | Retrieves the current account from EenvoudigFactureren. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from EenvoudigFactureren. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in EenvoudigFactureren. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from EenvoudigFactureren. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from EenvoudigFactureren. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in EenvoudigFactureren. |

### Client Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Client Contacts](actions/list-client-contacts.md) | GET | Retrieves client contacts from EenvoudigFactureren. |

### Custom Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Document](actions/get-custom-document.md) | GET | Retrieves a custom document from EenvoudigFactureren. |
| [List Custom Documents](actions/list-custom-documents.md) | GET | Retrieves custom documents from EenvoudigFactureren. |

### Delivery

| Action | Method | Description |
| --- | --- | --- |
| [Get Delivery](actions/get-delivery.md) | GET | Retrieves a delivery from EenvoudigFactureren. |
| [List Deliveries](actions/list-deliveries.md) | GET | Retrieves deliveries from EenvoudigFactureren. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in EenvoudigFactureren. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from EenvoudigFactureren. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from EenvoudigFactureren. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in EenvoudigFactureren. |

### Invoice Item

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Items](actions/list-invoice-items.md) | GET | Retrieves invoice items from EenvoudigFactureren. |

### Invoice Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Payments](actions/list-invoice-payments.md) | GET | Retrieves invoice payments from EenvoudigFactureren. |

### Invoice Remark

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Remarks](actions/list-invoice-remarks.md) | GET | Retrieves invoice remarks from EenvoudigFactureren. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in EenvoudigFactureren. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from EenvoudigFactureren. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from EenvoudigFactureren. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in EenvoudigFactureren. |

### Order Item

| Action | Method | Description |
| --- | --- | --- |
| [List Order Items](actions/list-order-items.md) | GET | Retrieves order items from EenvoudigFactureren. |

### Payment Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment Request](actions/get-payment-request.md) | GET | Retrieves a payment request from EenvoudigFactureren. |
| [List Payment Requests](actions/list-payment-requests.md) | GET | Retrieves payment requests from EenvoudigFactureren. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from EenvoudigFactureren. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from EenvoudigFactureren. |

### Purchase

| Action | Method | Description |
| --- | --- | --- |
| [List Purchases](actions/list-purchases.md) | GET | Retrieves purchases from EenvoudigFactureren. |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Create Quote](actions/create-quote.md) | POST | Creates a new quote in EenvoudigFactureren. |
| [Get Quote](actions/get-quote.md) | GET | Retrieves a quote from EenvoudigFactureren. |
| [List Quotes](actions/list-quotes.md) | GET | Retrieves quotes from EenvoudigFactureren. |
| [Update Quote](actions/update-quote.md) | PUT | Updates an existing quote in EenvoudigFactureren. |

### Quote Item

| Action | Method | Description |
| --- | --- | --- |
| [List Quote Items](actions/list-quote-items.md) | GET | Retrieves quote items from EenvoudigFactureren. |

### Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Get Receipt](actions/get-receipt.md) | GET | Retrieves a receipt from EenvoudigFactureren. |
| [List Receipts](actions/list-receipts.md) | GET | Retrieves receipts from EenvoudigFactureren. |

### Stock Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Stock Item](actions/get-stock-item.md) | GET | Retrieves a stock item from EenvoudigFactureren. |
| [List Stock Items](actions/list-stock-items.md) | GET | Retrieves stock items from EenvoudigFactureren. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from EenvoudigFactureren. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from EenvoudigFactureren. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from EenvoudigFactureren. |

