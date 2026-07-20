# Open Letter Connect: Native API Reference

A consolidated summary of Open Letter Connect's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.openletterconnect.com/
- **API base URL:** `https://api.openletterconnect.com/api/v1`

## Authentication

### API Key

Use an Open Letter Connect API key as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://api-docs.openletterconnect.com/getting-started/)

## API conventions

The total page count is read from `data.lastPage`. The current page number is read from `data.currentPage`.

## Pagination

Use `pageSize` in the query string to set the page size (default 25; maximum 100). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://api-docs.openletterconnect.com/contacts/create-contact/) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /custom-fields` | [docs](https://api-docs.openletterconnect.com/custom-fields/create-custom-field/) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://api-docs.openletterconnect.com/orders/place-order/) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://api-docs.openletterconnect.com/_templates/create-template/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://api-docs.openletterconnect.com/contacts/delete-contact/) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE /custom-fields/:id` | [docs](https://api-docs.openletterconnect.com/custom-fields/delete-custom-field/) |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/:id` | [docs](https://api-docs.openletterconnect.com/_templates/delete-template/) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://api-docs.openletterconnect.com/contacts/get-one-contact/) |
| [Get Custom Field](actions/get-custom-field.md) | `GET /custom-fields/:id` | [docs](https://api-docs.openletterconnect.com/custom-fields/get-one-custom-field/) |
| [Get Order](actions/get-order.md) | `GET /orders/:id` | [docs](https://api-docs.openletterconnect.com/orders/get-one-order/) |
| [Get Order Details](actions/get-order-details.md) | `GET /orders/detail/:id` | [docs](https://api-docs.openletterconnect.com/orders/items/order-details/) |
| [Get Product Details](actions/get-product-details.md) | `POST /products/details` | [docs](https://api-docs.openletterconnect.com/products/product-details/) |
| [Get Product Types](actions/get-product-types.md) | `GET /products/types` | [docs](https://api-docs.openletterconnect.com/products/get-product-types/) |
| [Get Template](actions/get-template.md) | `GET /templates/:id` | [docs](https://api-docs.openletterconnect.com/_templates/get-one-template/) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://api-docs.openletterconnect.com/contacts/get-all-contacts/) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom-fields` | [docs](https://api-docs.openletterconnect.com/custom-fields/get-all-custom-fields/) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://api-docs.openletterconnect.com/orders/get-order-history/) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://api-docs.openletterconnect.com/products/get-all-products/) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://api-docs.openletterconnect.com/_templates/get-all-templates/) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://api-docs.openletterconnect.com/contacts/update-contact/) |
| [Update Custom Field](actions/update-custom-field.md) | `PUT /custom-fields/:id` | [docs](https://api-docs.openletterconnect.com/custom-fields/update-custom-field/) |
| [Update Template](actions/update-template.md) | `PATCH /templates/:id` | [docs](https://api-docs.openletterconnect.com/_templates/update-template/) |
| [Upload Template](actions/upload-template.md) | `POST /templates/upload` | [docs](https://api-docs.openletterconnect.com/_templates/upload-template/) |
| [View Order Proof](actions/view-order-proof.md) | `POST /orders/view-proof` | [docs](https://api-docs.openletterconnect.com/orders/view-proof/) |
