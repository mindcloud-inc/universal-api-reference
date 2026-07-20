# <img src="https://images.mindcloud.co/apps/icons/reg-fox_1775251375377.png" alt="RegFox logo" width="28" height="28"> RegFox: Universal API

RegFox is an event registration and ticketing platform for forms, orders, registrants, tickets, subscriptions, customers, memberships, coupons, inventory, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/regFox/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.regfox.com/
- **Vendor API docs:** https://docs.webconnex.io/api/v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ping](actions/ping.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/regFox/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Coupon

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupon](actions/create-coupon.md) | POST | Creates a coupon in the RegFox account. |
| [Delete Coupon](actions/delete-coupon.md) | DELETE | Deletes an existing coupon from the RegFox account. |
| [Get Coupon](actions/get-coupon.md) | GET | Retrieves coupon details from the RegFox account. |
| [List Form Coupons](actions/list-form-coupons.md) | GET | Retrieves coupons for a RegFox form. |
| [List Global Coupons](actions/list-global-coupons.md) | GET | Retrieves global coupons from the RegFox account. |
| [Update Coupon](actions/update-coupon.md) | PUT | Updates an existing coupon in the RegFox account. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves customer details from the RegFox account. |
| [Search Customers](actions/search-customers.md) | GET | Finds matching customers in the RegFox account. |

### Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Ping](actions/ping.md) | GET | Retrieves the RegFox API healthcheck response. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET | Retrieves form details from the RegFox account. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from the RegFox account. |

### Inventory Item

| Action | Method | Description |
| --- | --- | --- |
| [List Form Inventory](actions/list-form-inventory.md) | GET | Retrieves inventory items for a RegFox form. |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [Get Membership](actions/get-membership.md) | GET | Retrieves membership details from the RegFox account. |
| [Search Memberships](actions/search-memberships.md) | GET | Finds matching memberships in the RegFox account. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves order details from the RegFox account. |
| [Search Orders](actions/search-orders.md) | GET | Finds matching orders in the RegFox account. |

### Registrant

| Action | Method | Description |
| --- | --- | --- |
| [Check In Registrant](actions/check-in-registrant.md) | PUT | Checks in a registrant in the RegFox account. |
| [Get Registrant](actions/get-registrant.md) | GET | Retrieves registrant details from the RegFox account. |
| [Search Registrants](actions/search-registrants.md) | GET | Finds matching registrants in the RegFox account. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves subscription details from the RegFox account. |
| [Search Subscriptions](actions/search-subscriptions.md) | GET | Finds matching subscriptions in the RegFox account. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves ticket details from the RegFox account. |
| [Search Tickets](actions/search-tickets.md) | GET | Finds matching tickets in the RegFox account. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves transaction details from the RegFox account. |
| [Search Transactions](actions/search-transactions.md) | GET | Finds matching transactions in the RegFox account. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in the RegFox account. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from the RegFox account. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves webhook details from the RegFox account. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from the RegFox account. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in the RegFox account. |

