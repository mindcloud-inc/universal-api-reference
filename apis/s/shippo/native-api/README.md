# Shippo - Legacy: Native API Reference

A consolidated summary of Shippo - Legacy's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://docs.goshippo.com/shippoapi/public-api/
- **API base URL:** `https://api.goshippo.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.goshippo.com/docs/guides_general/authentication/)

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://goshippo.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://goshippo.com/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `*`.

Refresh expired access tokens with a POST request to https://goshippo.com/oauth/refresh_token.

[Official authentication documentation](https://docs.goshippo.com/docs/integrations/partner_authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Response data is read from `results`. The next-page cursor is read from `next`. The current page number is read from `next`.

## Pagination

Use `page` in the query string to set the page size (default 200; accepted range 1–200). Use `page` in the query string as the pagination cursor; numbering starts at 1. Follow the complete next-page URL returned by the API.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Insta Label](actions/create-insta-label.md) | `POST /transactions/` | [docs](https://docs.goshippo.com/docs/guides_general/single_call/) |
| [Create Label with Rate ID](actions/create-label-with-rate-id.md) | `POST /transactions` | [docs](https://docs.goshippo.com/shippoapi/public-api/transactions) |
| [Create Refund](actions/create-refund.md) | `POST /refunds` | [docs](https://docs.goshippo.com/shippoapi/public-api/refunds) |
| [Create Shipment](actions/create-shipment.md) | `POST /shipments` | [docs](https://docs.goshippo.com/shippoapi/public-api/#operation/CreateShipment) |
| [List Addresses](actions/list-addresses.md) | `GET /addresses` | [docs](https://docs.goshippo.com/shippoapi/public-api/addresses) |
| [List All Carrier Parcel Templates](actions/list-all-carrier-parcel-templates.md) | `GET /parcel-templates` | [docs](https://docs.goshippo.com/shippoapi/public-api/parcel-templates) |
| [List Carrier Accounts](actions/list-carrier-accounts.md) | `GET /carrier_accounts` | [docs](https://docs.goshippo.com/docs/carriers/spec/carrier_acc/operation/ListCarrierAccounts/) |
| [List Transactions](actions/list-transactions.md) | `GET /transactions` | [docs](https://docs.goshippo.com/shippoapi/public-api/transactions) |
