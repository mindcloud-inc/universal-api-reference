# Universe: Native API Reference

A consolidated summary of Universe's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://developers.universe.com/
- **API base URL:** `https://www.universe.com`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.universe.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://www.universe.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `public`.

[Official authentication documentation](https://developers.universe.com/docs/authorizing-with-oauth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check In Order Item](actions/check-in-order-item.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [Check Out Order Item](actions/check-out-order-item.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [Get Default Email Template](actions/get-default-email-template.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [Get Discount](actions/get-discount.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [Get Event](actions/get-event.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [Get Event Report](actions/get-event-report.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [Get Host](actions/get-host.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [Get Host Report](actions/get-host-report.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [Get Membership](actions/get-membership.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [Get Order](actions/get-order.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [Get Order Item](actions/get-order-item.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [Get Profile](actions/get-profile.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [Get Viewer](actions/get-viewer.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [List Available Permissions](actions/list-available-permissions.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [List Calendar Widgets](actions/list-calendar-widgets.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [List Categories](actions/list-categories.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [List Email Templates](actions/list-email-templates.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [List Event Access Keys](actions/list-event-access-keys.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [List Event Attendees](actions/list-event-attendees.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [List Event Discount Codes](actions/list-event-discount-codes.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [List Event Orders](actions/list-event-orders.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [List Event Questions](actions/list-event-questions.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [List Event Rates](actions/list-event-rates.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [List Event Referral Codes](actions/list-event-referral-codes.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [List Events](actions/list-events.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/getting-a-list-of-your-events) |
| [List Host Attendees](actions/list-host-attendees.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [List Host Events With Tickets](actions/list-host-events-with-tickets.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/getting-a-list-of-your-events) |
| [List Host Orders](actions/list-host-orders.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
| [List Memberships](actions/list-memberships.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [List Stripe Countries](actions/list-stripe-countries.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [List Stripe Currencies](actions/list-stripe-currencies.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [List User External Emails](actions/list-user-external-emails.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [List Whitelisted Countries](actions/list-whitelisted-countries.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/basic-usage-1) |
| [Upsert Event Discounts](actions/upsert-event-discounts.md) | `POST /graphql` | [docs](https://developers.universe.com/docs/what-data-is-available) |
