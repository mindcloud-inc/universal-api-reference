# <img src="https://images.mindcloud.co/apps/icons/checkout-page_1774025017166.png" alt="Checkout Page logo" width="28" height="28"> Checkout Page: Universal API

Manage checkout pages, forms, events, customers, payments, subscriptions, coupons, products, and ticket operations in Checkout Page.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/checkoutPage/latest
- **Category:** Commerce
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://checkoutpage.com
- **Vendor API docs:** https://checkoutpage.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Checkout Pages](actions/list-checkout-pages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-checkout-pages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Bookings

| Action | Method | Description |
| --- | --- | --- |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from Checkout Page. |

### Checkout Pages

| Action | Method | Description |
| --- | --- | --- |
| [Archive Checkout Page](actions/archive-checkout-page.md) | DELETE | Archives a checkout page in Checkout Page. |
| [Create Checkout Page](actions/create-checkout-page.md) | POST | Creates a checkout page in Checkout Page. |
| [Create Field For Checkout Page](actions/create-field-for-checkout-page.md) | POST | Creates a field for a checkout page in Checkout Page. |
| [Get Checkout Page](actions/get-checkout-page.md) | GET | Retrieves a checkout page from Checkout Page. |
| [List Checkout Pages](actions/list-checkout-pages.md) | GET | Retrieves checkout pages from Checkout Page. |
| [List Fields For Checkout Page](actions/list-fields-for-checkout-page.md) | GET | Retrieves fields for a checkout page in Checkout Page. |
| [Update Checkout Page](actions/update-checkout-page.md) | PUT | Updates a checkout page in Checkout Page. |
| [Update Field For Checkout Page](actions/update-field-for-checkout-page.md) | PUT | Updates a field for a checkout page in Checkout Page. |

### Coupons

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupon](actions/create-coupon.md) | POST | Creates a coupon in Checkout Page. |
| [List Coupons](actions/list-coupons.md) | GET | Retrieves coupons from Checkout Page. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Details](actions/get-customer-details.md) | GET | Retrieves customer details from Checkout Page. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Checkout Page. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a event in Checkout Page. |
| [Create Field For Event](actions/create-field-for-event.md) | POST | Creates a field for an event in Checkout Page. |
| [Get Event](actions/get-event.md) | GET | Retrieves a event from Checkout Page. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Checkout Page. |
| [List Fields For Event](actions/list-fields-for-event.md) | GET | Retrieves fields for an event in Checkout Page. |
| [Update Event](actions/update-event.md) | PUT | Updates a event in Checkout Page. |
| [Update Field For Event](actions/update-field-for-event.md) | PUT | Updates a field for an event in Checkout Page. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Field For Form](actions/create-field-for-form.md) | POST | Creates a field for a form in Checkout Page. |
| [Create Form](actions/create-form.md) | POST | Creates a form in Checkout Page. |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from Checkout Page. |
| [List Fields For Form](actions/list-fields-for-form.md) | GET | Retrieves fields for a form in Checkout Page. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from Checkout Page. |
| [Update Field For Form](actions/update-field-for-form.md) | PUT | Updates a field for a form in Checkout Page. |
| [Update Form](actions/update-form.md) | PUT | Updates a form in Checkout Page. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET | Retrieves payments from Checkout Page. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Checkout Page. |
| [Update Product](actions/update-product.md) | PUT | Updates a product in Checkout Page. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Checkout Page. |

### Ticket Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket Group](actions/create-ticket-group.md) | POST | Creates a ticket group in Checkout Page. |
| [Get Ticket Group](actions/get-ticket-group.md) | GET | Retrieves a ticket group from Checkout Page. |
| [List Ticket Groups](actions/list-ticket-groups.md) | GET | Retrieves ticket groups from Checkout Page. |
| [Update Ticket Group](actions/update-ticket-group.md) | PUT | Updates a ticket group in Checkout Page. |

### Ticket Types

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket Type](actions/create-ticket-type.md) | POST | Creates a ticket type in Checkout Page. |
| [Get Ticket Type](actions/get-ticket-type.md) | GET | Retrieves a ticket type from Checkout Page. |
| [List Ticket Types](actions/list-ticket-types.md) | GET | Retrieves ticket types from Checkout Page. |
| [Update Ticket Type](actions/update-ticket-type.md) | PUT | Updates a ticket type in Checkout Page. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Validate Ticket](actions/validate-ticket.md) | GET | Validates a ticket in Checkout Page by QR code. |

