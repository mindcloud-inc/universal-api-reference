# pretix: Native API Reference

A consolidated summary of pretix's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.pretix.eu/dev/api/index.html
- **API base URL:** `https://pretix.eu/api/v1`

## Authentication

### OAuth2

Connect a pretix account with OAuth2 authorization code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://pretix.eu/api/v1/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://pretix.eu/api/v1/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read write profile`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://pretix.eu/api/v1/oauth/token.

[Official authentication documentation](https://docs.pretix.eu/dev/api/oauth.html)

### API Token

Connect a pretix organizer team API token for server-side access without OAuth.

### Credentials

- **API Token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.pretix.eu/dev/api/tokenauth.html)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `results`.

## Pagination

Use `page_size` in the query string to set the page size (default 50; accepted range 1–50). Use `page` in the query string to choose the page; numbering starts at 1. Follow the complete next-page URL returned by the API.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Download Invoice](actions/download-invoice.md) | `GET /organizers/:organizer/events/:event/invoices/:invoice/download/` | [docs](https://docs.pretix.eu/dev/api/resources/invoices.html) |
| [Download Order Ticket PDF](actions/download-order-ticket-pdf.md) | `GET /organizers/:organizer/events/:event/orders/:code/download/pdf/` | [docs](https://docs.pretix.eu/dev/api/resources/orders.html) |
| [Get Check In List](actions/get-check-in-list.md) | `GET /organizers/:organizer/events/:event/checkinlists/:list/` | [docs](https://docs.pretix.eu/dev/api/resources/checkinlists.html) |
| [Get Event](actions/get-event.md) | `GET /organizers/:organizer/events/:event/` | [docs](https://docs.pretix.eu/dev/api/resources/events.html) |
| [Get Event Settings](actions/get-event-settings.md) | `GET /organizers/:organizer/events/:event/settings/` | [docs](https://docs.pretix.eu/dev/api/resources/events.html) |
| [Get Invoice](actions/get-invoice.md) | `GET /organizers/:organizer/events/:event/invoices/:invoice/` | [docs](https://docs.pretix.eu/dev/api/resources/invoices.html) |
| [Get Item](actions/get-item.md) | `GET /organizers/:organizer/events/:event/items/:item/` | [docs](https://docs.pretix.eu/dev/api/resources/items.html) |
| [Get Item Variation](actions/get-item-variation.md) | `GET /organizers/:organizer/events/:event/items/:item/variations/:variation/` | [docs](https://docs.pretix.eu/dev/api/resources/item_variations.html) |
| [Get Order](actions/get-order.md) | `GET /organizers/:organizer/events/:event/orders/:code/` | [docs](https://docs.pretix.eu/dev/api/resources/orders.html) |
| [Get Order Position](actions/get-order-position.md) | `GET /organizers/:organizer/events/:event/orderpositions/:position/` | [docs](https://docs.pretix.eu/dev/api/resources/orders.html) |
| [Get Organizer](actions/get-organizer.md) | `GET /organizers/:organizer/` | [docs](https://docs.pretix.eu/dev/api/resources/organizers.html) |
| [Get Organizer Settings](actions/get-organizer-settings.md) | `GET /organizers/:organizer/settings/` | [docs](https://docs.pretix.eu/dev/api/resources/organizers.html) |
| [Get Quota](actions/get-quota.md) | `GET /organizers/:organizer/events/:event/quotas/:quota/` | [docs](https://docs.pretix.eu/dev/api/resources/quotas.html) |
| [Get Quota Availability](actions/get-quota-availability.md) | `GET /organizers/:organizer/events/:event/quotas/:quota/availability/` | [docs](https://docs.pretix.eu/dev/api/resources/quotas.html) |
| [Get Sub Event](actions/get-sub-event.md) | `GET /organizers/:organizer/events/:event/subevents/:subevent/` | [docs](https://docs.pretix.eu/dev/api/resources/subevents.html) |
| [Get User Profile](actions/get-user-profile.md) | `GET /me` | [docs](https://docs.pretix.eu/dev/api/oauth.html) |
| [Get Voucher](actions/get-voucher.md) | `GET /organizers/:organizer/events/:event/vouchers/:voucher/` | [docs](https://docs.pretix.eu/dev/api/resources/vouchers.html) |
| [List Check In Lists](actions/list-check-in-lists.md) | `GET /organizers/:organizer/events/:event/checkinlists/` | [docs](https://docs.pretix.eu/dev/api/resources/checkinlists.html) |
| [List Events](actions/list-events.md) | `GET /organizers/:organizer/events/` | [docs](https://docs.pretix.eu/dev/api/resources/events.html) |
| [List Invoices](actions/list-invoices.md) | `GET /organizers/:organizer/events/:event/invoices/` | [docs](https://docs.pretix.eu/dev/api/resources/invoices.html) |
| [List Item Variations](actions/list-item-variations.md) | `GET /organizers/:organizer/events/:event/items/:item/variations/` | [docs](https://docs.pretix.eu/dev/api/resources/item_variations.html) |
| [List Items](actions/list-items.md) | `GET /organizers/:organizer/events/:event/items/` | [docs](https://docs.pretix.eu/dev/api/resources/items.html) |
| [List Order Positions](actions/list-order-positions.md) | `GET /organizers/:organizer/events/:event/orderpositions/` | [docs](https://docs.pretix.eu/dev/api/resources/orders.html) |
| [List Orders](actions/list-orders.md) | `GET /organizers/:organizer/events/:event/orders/` | [docs](https://docs.pretix.eu/dev/api/resources/orders.html) |
| [List Organizers](actions/list-organizers.md) | `GET /organizers/` | [docs](https://docs.pretix.eu/dev/api/resources/organizers.html) |
| [List Quotas](actions/list-quotas.md) | `GET /organizers/:organizer/events/:event/quotas/` | [docs](https://docs.pretix.eu/dev/api/resources/quotas.html) |
| [List Sub Events](actions/list-sub-events.md) | `GET /organizers/:organizer/events/:event/subevents/` | [docs](https://docs.pretix.eu/dev/api/resources/subevents.html) |
| [List Vouchers](actions/list-vouchers.md) | `GET /organizers/:organizer/events/:event/vouchers/` | [docs](https://docs.pretix.eu/dev/api/resources/vouchers.html) |
| [Search Check In Tickets](actions/search-check-in-tickets.md) | `GET /organizers/:organizer/checkinrpc/search/` | [docs](https://docs.pretix.eu/dev/api/resources/checkin.html) |
| [Search Organizer Orders](actions/search-organizer-orders.md) | `GET /organizers/:organizer/orders/` | [docs](https://docs.pretix.eu/dev/api/resources/orders.html) |
