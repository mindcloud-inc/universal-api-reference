# EenvoudigFactureren: Native API Reference

A consolidated summary of EenvoudigFactureren's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://help.eenvoudigfactureren.be/support/solutions/101000176283
- **API base URL:** `https://eenvoudigfactureren.be/api/v1`

## Authentication

### API Key

Authenticate with an EenvoudigFactureren API key. Requests send the key in the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381584-api-authenticatie)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `take` in the query string to set the page size (default 50; accepted range 1–100). Use `skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381976-api-klanten) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381977-api-facturen) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381990-api-bestelbonnen) |
| [Create Quote](actions/create-quote.md) | `POST /quotes` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381985-api-offertes) |
| [Get Client](actions/get-client.md) | `GET /clients/:client_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381976-api-klanten) |
| [Get Current Account](actions/get-current-account.md) | `GET /accounts/current` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000502769-api-accounts) |
| [Get Custom Document](actions/get-custom-document.md) | `GET /customdocuments/:customdocument_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000448910-api-vrije-documenten) |
| [Get Delivery](actions/get-delivery.md) | `GET /deliveries/:delivery_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381991-api-leveringsbonnen) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:invoice_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381977-api-facturen) |
| [Get Order](actions/get-order.md) | `GET /orders/:order_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381990-api-bestelbonnen) |
| [Get Payment Request](actions/get-payment-request.md) | `GET /paymentrequests/:paymentrequest_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000448907-api-betaalverzoeken) |
| [Get Project](actions/get-project.md) | `GET /projects/:project_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000507047-api-projecten) |
| [Get Quote](actions/get-quote.md) | `GET /quotes/:quote_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381985-api-offertes) |
| [Get Receipt](actions/get-receipt.md) | `GET /receipts/:receipt_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381980-api-kasticketten) |
| [Get Stock Item](actions/get-stock-item.md) | `GET /stockitems/:stockitem_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381994-api-artikelen) |
| [Get Subscription](actions/get-subscription.md) | `GET /subscriptions/:subscription_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381992-api-abonnementen) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000502769-api-accounts) |
| [List Client Contacts](actions/list-client-contacts.md) | `GET /clients/:client_id/contacts` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381976-api-klanten) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381976-api-klanten) |
| [List Custom Documents](actions/list-custom-documents.md) | `GET /customdocuments` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000448910-api-vrije-documenten) |
| [List Deliveries](actions/list-deliveries.md) | `GET /deliveries` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381991-api-leveringsbonnen) |
| [List Invoice Items](actions/list-invoice-items.md) | `GET /invoices/:invoice_id/items` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381977-api-facturen) |
| [List Invoice Payments](actions/list-invoice-payments.md) | `GET /invoices/:invoice_id/payments` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381977-api-facturen) |
| [List Invoice Remarks](actions/list-invoice-remarks.md) | `GET /invoices/:invoice_id/remarks` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381977-api-facturen) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381977-api-facturen) |
| [List Order Items](actions/list-order-items.md) | `GET /orders/:order_id/items` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381990-api-bestelbonnen) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381990-api-bestelbonnen) |
| [List Payment Requests](actions/list-payment-requests.md) | `GET /paymentrequests` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000448907-api-betaalverzoeken) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000507047-api-projecten) |
| [List Purchases](actions/list-purchases.md) | `GET /purchases` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000532894-api-aankoopdocumenten) |
| [List Quote Items](actions/list-quote-items.md) | `GET /quotes/:quote_id/items` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381985-api-offertes) |
| [List Quotes](actions/list-quotes.md) | `GET /quotes` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381985-api-offertes) |
| [List Receipts](actions/list-receipts.md) | `GET /receipts` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381980-api-kasticketten) |
| [List Stock Items](actions/list-stock-items.md) | `GET /stockitems` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381994-api-artikelen) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /subscriptions` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381992-api-abonnementen) |
| [List Suppliers](actions/list-suppliers.md) | `GET /suppliers` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000532901-api-leveranciers) |
| [Update Client](actions/update-client.md) | `PUT /clients/:client_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381976-api-klanten) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:invoice_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381977-api-facturen) |
| [Update Order](actions/update-order.md) | `PUT /orders/:order_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381990-api-bestelbonnen) |
| [Update Quote](actions/update-quote.md) | `PUT /quotes/:quote_id` | [docs](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381985-api-offertes) |
