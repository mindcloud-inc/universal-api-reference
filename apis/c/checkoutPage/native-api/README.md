# Checkout Page: Native API Reference

A consolidated summary of Checkout Page's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://checkoutpage.com/docs/api
- **OpenAPI specification:** https://api.checkoutpage.com/docs/seller-api/v1/swagger.json
- **API base URL:** `https://api.checkoutpage.com`

## Authentication

### API Key

Connect Checkout Page with a seller API key sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://checkoutpage.com/docs/api/authentication)

## API conventions

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `starting_after` in the query string as the pagination cursor; numbering starts at 0.

## Filtering

Send filters in the query string.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Checkout Page](actions/archive-checkout-page.md) | `DELETE /v1/checkout-pages/:pageId` | [docs](https://checkoutpage.com/docs/api/v1/checkout-pages/delete) |
| [Create Checkout Page](actions/create-checkout-page.md) | `POST /v1/checkout-pages/` | [docs](https://checkoutpage.com/docs/api/v1/checkout-pages/create) |
| [Create Coupon](actions/create-coupon.md) | `POST /v1/coupons/` | [docs](https://checkoutpage.com/docs/api/v1/coupons/create) |
| [Create Event](actions/create-event.md) | `POST /v1/events/` | [docs](https://checkoutpage.com/docs/api/v1/events/create) |
| [Create Field For Checkout Page](actions/create-field-for-checkout-page.md) | `POST /v1/checkout-pages/:pageId/fields` | [docs](https://checkoutpage.com/docs/api/v1/checkout-pages/fields/create) |
| [Create Field For Event](actions/create-field-for-event.md) | `POST /v1/events/:pageId/fields` | [docs](https://checkoutpage.com/docs/api/v1/events/fields/create) |
| [Create Field For Form](actions/create-field-for-form.md) | `POST /v1/forms/:pageId/fields` | [docs](https://checkoutpage.com/docs/api/v1/forms/fields/create) |
| [Create Form](actions/create-form.md) | `POST /v1/forms/` | [docs](https://checkoutpage.com/docs/api/v1/forms/create) |
| [Create Ticket Group](actions/create-ticket-group.md) | `POST /v1/events/:pageId/ticket-groups` | [docs](https://checkoutpage.com/docs/api/v1/events/ticket-groups/create) |
| [Create Ticket Type](actions/create-ticket-type.md) | `POST /v1/events/:pageId/ticket-groups/:ticketGroupId/ticket-types` | [docs](https://checkoutpage.com/docs/api/v1/events/ticket-groups/ticket-types/create) |
| [Get Checkout Page](actions/get-checkout-page.md) | `GET /v1/checkout-pages/:pageId` | [docs](https://checkoutpage.com/docs/api/v1/checkout-pages/get) |
| [Get Customer Details](actions/get-customer-details.md) | `GET /v1/customers/:customerId` | [docs](https://checkoutpage.com/docs/api/v1/customers/get) |
| [Get Event](actions/get-event.md) | `GET /v1/events/:pageId` | [docs](https://checkoutpage.com/docs/api/v1/events/get) |
| [Get Form](actions/get-form.md) | `GET /v1/forms/:pageId` | [docs](https://checkoutpage.com/docs/api/v1/forms/get) |
| [Get Product](actions/get-product.md) | `GET /v1/products/:productId` | [docs](https://checkoutpage.com/docs/api/v1/products/get) |
| [Get Ticket Group](actions/get-ticket-group.md) | `GET /v1/events/:pageId/ticket-groups/:ticketGroupId` | [docs](https://checkoutpage.com/docs/api/v1/events/ticket-groups/get) |
| [Get Ticket Type](actions/get-ticket-type.md) | `GET /v1/events/:pageId/ticket-groups/:ticketGroupId/ticket-types/:ticketTypeId` | [docs](https://checkoutpage.com/docs/api/v1/events/ticket-groups/ticket-types/get) |
| [List Bookings](actions/list-bookings.md) | `GET /v1/bookings/` | [docs](https://checkoutpage.com/docs/api/v1/bookings/list) |
| [List Checkout Pages](actions/list-checkout-pages.md) | `GET /v1/checkout-pages/` | [docs](https://checkoutpage.com/docs/api/v1/checkout-pages/list) |
| [List Coupons](actions/list-coupons.md) | `GET /v1/coupons/` | [docs](https://checkoutpage.com/docs/api/v1/coupons/list) |
| [List Customers](actions/list-customers.md) | `GET /v1/customers/` | [docs](https://checkoutpage.com/docs/api/v1/customers/list) |
| [List Events](actions/list-events.md) | `GET /v1/events/` | [docs](https://checkoutpage.com/docs/api/v1/events/list) |
| [List Fields For Checkout Page](actions/list-fields-for-checkout-page.md) | `GET /v1/checkout-pages/:pageId/fields` | [docs](https://checkoutpage.com/docs/api/v1/checkout-pages/fields/list) |
| [List Fields For Event](actions/list-fields-for-event.md) | `GET /v1/events/:pageId/fields` | [docs](https://checkoutpage.com/docs/api/v1/events/fields/list) |
| [List Fields For Form](actions/list-fields-for-form.md) | `GET /v1/forms/:pageId/fields` | [docs](https://checkoutpage.com/docs/api/v1/forms/fields/list) |
| [List Forms](actions/list-forms.md) | `GET /v1/forms/` | [docs](https://checkoutpage.com/docs/api/v1/forms/list) |
| [List Payments](actions/list-payments.md) | `GET /v1/payments/` | [docs](https://checkoutpage.com/docs/api/v1/payments/list) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /v1/subscriptions/` | [docs](https://checkoutpage.com/docs/api/v1/subscriptions/list) |
| [List Ticket Groups](actions/list-ticket-groups.md) | `GET /v1/events/:pageId/ticket-groups` | [docs](https://checkoutpage.com/docs/api/v1/events/ticket-groups/list) |
| [List Ticket Types](actions/list-ticket-types.md) | `GET /v1/events/:pageId/ticket-groups/:ticketGroupId/ticket-types` | [docs](https://checkoutpage.com/docs/api/v1/events/ticket-groups/ticket-types/list) |
| [Update Checkout Page](actions/update-checkout-page.md) | `PATCH /v1/checkout-pages/:pageId` | [docs](https://checkoutpage.com/docs/api/v1/checkout-pages/update) |
| [Update Event](actions/update-event.md) | `PATCH /v1/events/:pageId` | [docs](https://checkoutpage.com/docs/api/v1/events/update) |
| [Update Field For Checkout Page](actions/update-field-for-checkout-page.md) | `PATCH /v1/checkout-pages/:pageId/fields/:fieldId` | [docs](https://checkoutpage.com/docs/api/v1/checkout-pages/fields/update) |
| [Update Field For Event](actions/update-field-for-event.md) | `PATCH /v1/events/:pageId/fields/:fieldId` | [docs](https://checkoutpage.com/docs/api/v1/events/fields/update) |
| [Update Field For Form](actions/update-field-for-form.md) | `PATCH /v1/forms/:pageId/fields/:fieldId` | [docs](https://checkoutpage.com/docs/api/v1/forms/fields/update) |
| [Update Form](actions/update-form.md) | `PATCH /v1/forms/:pageId` | [docs](https://checkoutpage.com/docs/api/v1/forms/update) |
| [Update Product](actions/update-product.md) | `PATCH /v1/products/:productId` | [docs](https://checkoutpage.com/docs/api/v1/products/update) |
| [Update Ticket Group](actions/update-ticket-group.md) | `PATCH /v1/events/:pageId/ticket-groups/:ticketGroupId` | [docs](https://checkoutpage.com/docs/api/v1/events/ticket-groups/update) |
| [Update Ticket Type](actions/update-ticket-type.md) | `PATCH /v1/events/:pageId/ticket-groups/:ticketGroupId/ticket-types/:ticketTypeId` | [docs](https://checkoutpage.com/docs/api/v1/events/ticket-groups/ticket-types/update) |
| [Validate Ticket](actions/validate-ticket.md) | `POST /v1/tickets/validate/:qrCode` | [docs](https://checkoutpage.com/docs/api/v1/tickets/validate) |
