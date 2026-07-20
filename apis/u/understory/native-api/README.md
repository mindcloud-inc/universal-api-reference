# Understory: Native API Reference

A consolidated summary of Understory's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.understory.io/apis
- **OpenAPI specification:** https://developer.understory.io/_bundle/apis/index.json
- **API base URL:** `https://api.understory.io`

## Authentication

### OAuth 2.0

Understory internal integration keys using OAuth 2.0 client_credentials.

### Credentials

- **Client ID:** `clientId` · required · Understory OAuth 2.0 client ID for the internal integration key.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.auth.understory.io/oauth2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://api.auth.understory.io/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `booking.read booking.write event.read experience.read marketing.read order.read webhook.read webhook.write`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://developer.understory.io/docs/usage/authentication/integration-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Sorting

Set the sort field with `sort` in the query string. Use `+` for ascending order and `-` for descending order. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | `POST /v1/bookings` | [docs](https://developer.understory.io/apis/booking/createbooking.md) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /v1/webhook-subscriptions` | [docs](https://developer.understory.io/apis/webhook/createwebhooksubscription.md) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /v1/webhook-subscriptions/{{subscriptionId}}` | [docs](https://developer.understory.io/apis/webhook/deletewebhooksubscription.md) |
| [Get Booking](actions/get-booking.md) | `GET /v1/bookings/{{bookingId}}` | [docs](https://developer.understory.io/apis/booking/getbooking.md) |
| [Get Current User](actions/get-current-user.md) | `GET /v1/me` | [docs](https://developer.understory.io/apis/test/getme.md) |
| [Get Event](actions/get-event.md) | `GET /v1/events/{{eventId}}` | [docs](https://developer.understory.io/apis/event/getevent.md) |
| [Get Event Availability](actions/get-event-availability.md) | `GET /v1/event-availabilities/{{eventId}}` | [docs](https://developer.understory.io/apis/event-availability/geteventavailability.md) |
| [Get Experience](actions/get-experience.md) | `GET /v1/experiences/{{experienceId}}` | [docs](https://developer.understory.io/apis/experience/getexperiencebyid.md) |
| [Get Order](actions/get-order.md) | `GET /v1/orders/{{orderId}}` | [docs](https://developer.understory.io/apis/order/getorder.md) |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | `GET /v1/webhook-subscriptions/{{subscriptionId}}` | [docs](https://developer.understory.io/apis/webhook/getwebhooksubscription.md) |
| [List Booking Tickets](actions/list-booking-tickets.md) | `GET /v1/bookings/{{bookingId}}/tickets` | [docs](https://developer.understory.io/apis/booking/gettickets.md) |
| [List Bookings](actions/list-bookings.md) | `GET /v1/bookings` | [docs](https://developer.understory.io/apis/booking/getbookings.md) |
| [List Event Availability](actions/list-event-availability.md) | `GET /v1/event-availabilities` | [docs](https://developer.understory.io/apis/event-availability/listeventavailability.md) |
| [List Events](actions/list-events.md) | `GET /v1/events` | [docs](https://developer.understory.io/apis/event/getevents.md) |
| [List Experiences](actions/list-experiences.md) | `GET /v1/experiences` | [docs](https://developer.understory.io/apis/experience/getexperiences.md) |
| [List Information Requests](actions/list-information-requests.md) | `GET /v1/experiences/{{experienceId}}/information-requests` | [docs](https://developer.understory.io/apis/experience/getinformationrequestsforexperience.md) |
| [List Marketing Consents](actions/list-marketing-consents.md) | `GET /v1/marketing-consents` | [docs](https://developer.understory.io/apis/marketing/getmarketingconsents.md) |
| [List Order Line Items](actions/list-order-line-items.md) | `GET /v1/orders/{{orderId}}/line-items` | [docs](https://developer.understory.io/apis/order/getlineitems.md) |
| [List Order Refunds](actions/list-order-refunds.md) | `GET /v1/orders/{{orderId}}/refunds` | [docs](https://developer.understory.io/apis/order/getrefunds.md) |
| [List Order Transactions](actions/list-order-transactions.md) | `GET /v1/orders/{{orderId}}/transactions` | [docs](https://developer.understory.io/apis/order/gettransactions.md) |
| [List Orders](actions/list-orders.md) | `GET /v1/orders` | [docs](https://developer.understory.io/apis/order/getorders.md) |
| [List Ticket Variants](actions/list-ticket-variants.md) | `GET /v1/experiences/{{experienceId}}/ticket-variants` | [docs](https://developer.understory.io/apis/experience/getticketvariantsforexperience.md) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /v1/webhook-subscriptions` | [docs](https://developer.understory.io/apis/webhook/listwebhooksubscriptions.md) |
| [Update Webhook Subscription](actions/update-webhook-subscription.md) | `PUT /v1/webhook-subscriptions/{{subscriptionId}}` | [docs](https://developer.understory.io/apis/webhook/updatewebhooksubscription.md) |
