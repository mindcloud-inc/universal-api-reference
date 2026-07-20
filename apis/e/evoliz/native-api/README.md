# Evoliz: Native API Reference

A consolidated summary of Evoliz's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://evoliz.io/documentation
- **OpenAPI specification:** https://evoliz.io/api-docs/api-docs.yaml
- **API base URL:** `https://www.evoliz.io`

## Authentication

### API Keys

Use your Evoliz public key and secret key.

### Credentials

- **Public Key:** `publicKey` · required · The public API key generated in Evoliz.
- **Secret Key:** `secretKey` · required · The secret API key generated in Evoliz.

Send these headers with each API request:

```http
Authorization: Bearer <custom.token>
```

[Official authentication documentation](https://evoliz.io/documentation)

## API conventions

Response data is read from `data`. The total page count is read from `meta.last_page`. The current page number is read from `meta.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 15; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /api/v1/clients` | [docs](https://evoliz.io/documentation#tag/Client/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1clients/post) |
| [Create Client Contact](actions/create-client-contact.md) | `POST /api/v1/contacts-clients` | [docs](https://evoliz.io/documentation#tag/Contact%20client/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1contacts-clients/post) |
| [Create Invoice](actions/create-invoice.md) | `POST /api/v1/invoices` | [docs](https://evoliz.io/documentation#tag/Invoice/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1invoices/post) |
| [Create Quote](actions/create-quote.md) | `POST /api/v1/quotes` | [docs](https://evoliz.io/documentation#tag/Quote/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1quotes/post) |
| [Create Sale Order](actions/create-sale-order.md) | `POST /api/v1/sale-orders` | [docs](https://evoliz.io/documentation#tag/Sale%20order/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1sale-orders/post) |
| [Get Article](actions/get-article.md) | `GET /api/v1/articles/:articleid` | [docs](https://evoliz.io/documentation#tag/Article/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1articles~1%7Barticleid%7D/get) |
| [Get Client](actions/get-client.md) | `GET /api/v1/clients/:clientid` | [docs](https://evoliz.io/documentation#tag/Client/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1clients~1%7Bclientid%7D/get) |
| [Get Invoice](actions/get-invoice.md) | `GET /api/v1/invoices/:invoiceid` | [docs](https://evoliz.io/documentation#tag/Invoice/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1invoices~1%7Binvoiceid%7D/get) |
| [Get Quote](actions/get-quote.md) | `GET /api/v1/quotes/:quoteid` | [docs](https://evoliz.io/documentation#tag/Quote/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1quotes~1%7Bquoteid%7D/get) |
| [Get Sale Order](actions/get-sale-order.md) | `GET /api/v1/sale-orders/:orderid` | [docs](https://evoliz.io/documentation#tag/Sale%20order/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1sale-orders~1%7Borderid%7D/get) |
| [List Articles](actions/list-articles.md) | `GET /api/v1/articles` | [docs](https://evoliz.io/documentation#tag/Article/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1articles/get) |
| [List Client Contacts](actions/list-client-contacts.md) | `GET /api/v1/contacts-clients` | [docs](https://evoliz.io/documentation#tag/Contact%20client/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1contacts-clients/get) |
| [List Clients](actions/list-clients.md) | `GET /api/v1/clients` | [docs](https://evoliz.io/documentation#tag/Client/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1clients/get) |
| [List Invoices](actions/list-invoices.md) | `GET /api/v1/invoices` | [docs](https://evoliz.io/documentation#tag/Invoice/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1invoices/get) |
| [List Quotes](actions/list-quotes.md) | `GET /api/v1/quotes` | [docs](https://evoliz.io/documentation#tag/Quote/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1quotes/get) |
| [List Sale Orders](actions/list-sale-orders.md) | `GET /api/v1/sale-orders` | [docs](https://evoliz.io/documentation#tag/Sale%20order/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1sale-orders/get) |
| [Send Quote](actions/send-quote.md) | `POST /api/v1/quotes/:quoteid/send` | [docs](https://evoliz.io/documentation#tag/Quote/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1quotes~1%7Bquoteid%7D~1send/post) |
| [Update Article](actions/update-article.md) | `PATCH /api/v1/articles/:articleid` | [docs](https://evoliz.io/documentation#tag/Article/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1articles~1%7Barticleid%7D/patch) |
| [Update Client](actions/update-client.md) | `PATCH /api/v1/clients/:clientid` | [docs](https://evoliz.io/documentation#tag/Client/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1clients~1%7Bclientid%7D/patch) |
| [Update Invoice](actions/update-invoice.md) | `PUT /api/v1/invoices/:invoiceid` | [docs](https://evoliz.io/documentation#tag/Invoice/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1invoices~1%7Binvoiceid%7D/put) |
| [Update Quote](actions/update-quote.md) | `PUT /api/v1/quotes/:quoteid` | [docs](https://evoliz.io/documentation#tag/Quote/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1quotes~1%7Bquoteid%7D/put) |
| [Update Sale Order](actions/update-sale-order.md) | `PUT /api/v1/sale-orders/:orderid` | [docs](https://evoliz.io/documentation#tag/Sale%20order/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1sale-orders~1%7Borderid%7D/put) |
