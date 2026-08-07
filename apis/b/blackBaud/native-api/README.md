# BlackBaud: Native API Reference

A consolidated summary of BlackBaud's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://developer.blackbaud.com/skyapi/docs/getting-started
- **API base URL:** `https://api.sky.blackbaud.com/`

## Authentication

### OAuth 2.0

### Credentials

- **Client ID:** `clientId` · required · Blackbaud Application ID (OAuth client_id) for this customer connection.
- **Client Secret:** `clientSecret` · required · Blackbaud Application Secret (OAuth client_secret) for this customer connection.
- **Subscription Key:** `subscriptionKey` · required · Blackbaud developer Bb-Api-Subscription-Key required on SKY API requests.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.blackbaud.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.sky.blackbaud.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `altr.r rnxt.r`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.sky.blackbaud.com/token.

[Official authentication documentation](https://developer.blackbaud.com/skyapi/docs/authorization/auth-code-flow/confidential-application/tutorial)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Action](actions/get-action.md) | `GET constituent/v1/actions/{action_id}` | [docs](https://developer.blackbaud.com/skyapi/renxt/constituent/entities) |
| [Get Actions](actions/get-actions.md) | `GET constituent/v1/actions` | [docs](https://developer.blackbaud.com/skyapi/renxt/constituent/entities) |
| [Get Campaign](actions/get-campaign.md) | `GET fundraising/v1/campaigns/{campaign_id}` | [docs](https://developer.blackbaud.com/skyapi/renxt/fundraising/entities) |
| [Get Campaigns](actions/get-campaigns.md) | `GET fundraising/v1/campaigns` | [docs](https://developer.blackbaud.com/skyapi/renxt/fundraising/entities) |
| [Get Constituent](actions/get-constituent.md) | `GET constituent/v1/constituents/{constituent_id}` | [docs](https://developer.blackbaud.com/skyapi/renxt/constituent/entities) |
| [Get Constituent Actions](actions/get-constituent-actions.md) | `GET constituent/v1/constituents/{constituent_id}/actions` | [docs](https://developer.blackbaud.com/skyapi/renxt/constituent/entities) |
| [Get Constituents](actions/get-constituents.md) | `GET constituent/v1/constituents` | [docs](https://developer.blackbaud.com/skyapi/renxt/constituent/entities) |
| [Get Event Categories](actions/get-event-categories.md) | `GET event/v1/eventcategories` | [docs](https://developer.blackbaud.com/skyapi/products/altru) |
| [Get Events](actions/get-events.md) | `GET event/v1/eventlist` | [docs](https://developer.blackbaud.com/skyapi/products/altru) |
| [Get Fund](actions/get-fund.md) | `GET fundraising/v1/funds/{fund_id}` | [docs](https://developer.blackbaud.com/skyapi/renxt/fundraising/entities) |
| [Get Funds](actions/get-funds.md) | `GET fundraising/v1/funds` | [docs](https://developer.blackbaud.com/skyapi/renxt/fundraising/entities) |
| [Get Gift](actions/get-gift.md) | `GET gift/v1/gifts/{gift_id}` | [docs](https://developer.blackbaud.com/skyapi/renxt/gift/entities) |
| [Get Gifts](actions/get-gifts.md) | `GET gift/v1/gifts` | [docs](https://developer.blackbaud.com/skyapi/renxt/gift/entities) |
| [Get Order Delivery Information](actions/get-order-delivery-information.md) | `GET alt-slsmg/orders/{sales_order_id}` | [docs](https://developer.sky.blackbaud.com/api#api=alt-slsmg) |
| [Get Phone Types](actions/get-phone-types.md) | `GET constituent/v1/phonetypes` | [docs](https://developer.blackbaud.com/skyapi/renxt/constituent/entities) |
| [List Currencies](actions/list-currencies.md) | `GET alt-adnmg/currencies/list` | [docs](https://developer.sky.blackbaud.com/api) |
| [List Order Ticket Details](actions/list-order-ticket-details.md) | `GET alt-slsmg/sales/{sales_order_id}/orders` | [docs](https://developer.sky.blackbaud.com/api#api=alt-slsmg) |
| [List Sales Order Tickets Without Refunds](actions/list-sales-order-tickets-without-refunds.md) | `GET alt-slsmg/sales/{sales_order_id}/tickets` | [docs](https://developer.sky.blackbaud.com/api#api=alt-slsmg) |
| [Search Constituents](actions/search-constituents.md) | `GET constituent/v1/constituents/search` | [docs](https://developer.blackbaud.com/skyapi/renxt/constituent/entities) |
| [Search Constituents Duplicate](actions/search-constituents-duplicate.md) | `GET constituent/v1/constituents/duplicatesearch` | [docs](https://developer.blackbaud.com/skyapi/renxt/constituent/entities) |
| [Search For A Constituent](actions/search-for-a-constituent.md) | `GET alt-conmg/constituents/search` | [docs](https://learn.microsoft.com/en-us/connectors/blackbaudaltruconsti/) |
| [View Order Patron](actions/view-order-patron.md) | `GET alt-slsmg/orders/{sales_order_id}/view` | [docs](https://developer.sky.blackbaud.com/api#api=alt-slsmg) |
