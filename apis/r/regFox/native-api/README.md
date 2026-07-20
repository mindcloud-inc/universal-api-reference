# RegFox: Native API Reference

A consolidated summary of RegFox's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.webconnex.io/api/v2/
- **API base URL:** `https://api.webconnex.com/v2/public`

## Authentication

### API Key

Use a RegFox REST API key. RegFox documents API access for Premium and Professional plans.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apiKey: <apiKey>
```

[Official authentication documentation](https://help.regfox.com/en/articles/2340089-rest-api)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check In Registrant](actions/check-in-registrant.md) | `POST registrant/check-in` | [docs](https://docs.webconnex.io/api/v2/#check-in-by-id) |
| [Create Coupon](actions/create-coupon.md) | `POST coupons` | [docs](https://docs.webconnex.io/api/v2/#create-coupon) |
| [Create Webhook](actions/create-webhook.md) | `POST webhooks` | [docs](https://docs.webconnex.io/api/v2/#create) |
| [Delete Coupon](actions/delete-coupon.md) | `DELETE coupons/{id}` | [docs](https://docs.webconnex.io/api/v2/#delete-coupon) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE webhooks/{id}` | [docs](https://docs.webconnex.io/api/v2/#delete) |
| [Get Coupon](actions/get-coupon.md) | `GET coupons/{id}` | [docs](https://docs.webconnex.io/api/v2/#view-coupon-by-id) |
| [Get Customer](actions/get-customer.md) | `GET search/customers/{id}` | [docs](https://docs.webconnex.io/api/v2/#view-customer-by-id) |
| [Get Form](actions/get-form.md) | `GET forms/{id}` | [docs](https://docs.webconnex.io/api/v2/#view-form) |
| [Get Membership](actions/get-membership.md) | `GET search/memberships/{id}` | [docs](https://docs.webconnex.io/api/v2/#view-membership-by-id) |
| [Get Order](actions/get-order.md) | `GET search/orders/{id}` | [docs](https://docs.webconnex.io/api/v2/#view-order-by-id) |
| [Get Registrant](actions/get-registrant.md) | `GET search/registrants/{id}` | [docs](https://docs.webconnex.io/api/v2/#view-registrant-by-id) |
| [Get Subscription](actions/get-subscription.md) | `GET search/subscriptions/{id}` | [docs](https://docs.webconnex.io/api/v2/#view-subscription-by-id) |
| [Get Ticket](actions/get-ticket.md) | `GET search/tickets/{id}` | [docs](https://docs.webconnex.io/api/v2/#view-ticket-by-id) |
| [Get Transaction](actions/get-transaction.md) | `GET search/transactions/{id}` | [docs](https://docs.webconnex.io/api/v2/#view-transaction-by-id) |
| [Get Webhook](actions/get-webhook.md) | `GET webhooks/{id}` | [docs](https://docs.webconnex.io/api/v2/#view) |
| [List Form Coupons](actions/list-form-coupons.md) | `GET coupons/forms/{formId}` | [docs](https://docs.webconnex.io/api/v2/#list-form-coupons) |
| [List Form Inventory](actions/list-form-inventory.md) | `GET forms/{formId}/inventory` | [docs](https://docs.webconnex.io/api/v2/#view-for-form) |
| [List Forms](actions/list-forms.md) | `GET forms` | [docs](https://docs.webconnex.io/api/v2/#list-forms) |
| [List Global Coupons](actions/list-global-coupons.md) | `GET coupons/global` | [docs](https://docs.webconnex.io/api/v2/#list-global-coupons) |
| [List Webhooks](actions/list-webhooks.md) | `GET webhooks` | [docs](https://docs.webconnex.io/api/v2/#list) |
| [Ping](actions/ping.md) | `GET ping` | [docs](https://docs.webconnex.io/api/v2/#ping-healthcheck) |
| [Search Customers](actions/search-customers.md) | `GET search/customers` | [docs](https://docs.webconnex.io/api/v2/#search-customers) |
| [Search Memberships](actions/search-memberships.md) | `GET search/memberships` | [docs](https://docs.webconnex.io/api/v2/#search-memberships) |
| [Search Orders](actions/search-orders.md) | `GET search/orders` | [docs](https://docs.webconnex.io/api/v2/#search-orders) |
| [Search Registrants](actions/search-registrants.md) | `GET search/registrants` | [docs](https://docs.webconnex.io/api/v2/#search-registrants) |
| [Search Subscriptions](actions/search-subscriptions.md) | `GET search/subscriptions` | [docs](https://docs.webconnex.io/api/v2/#search-subscriptions) |
| [Search Tickets](actions/search-tickets.md) | `GET search/tickets` | [docs](https://docs.webconnex.io/api/v2/#search-tickets) |
| [Search Transactions](actions/search-transactions.md) | `GET search/transactions` | [docs](https://docs.webconnex.io/api/v2/#search-transactions) |
| [Update Coupon](actions/update-coupon.md) | `PUT coupons/{id}` | [docs](https://docs.webconnex.io/api/v2/#edit-coupon) |
| [Update Webhook](actions/update-webhook.md) | `PUT webhooks/{id}` | [docs](https://docs.webconnex.io/api/v2/#update) |
