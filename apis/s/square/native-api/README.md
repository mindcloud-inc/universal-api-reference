# Square: Native API Reference

A consolidated summary of Square's API configuration, with links to official documentation.

- **Official docs:** https://developer.squareup.com/reference/square
- **OpenAPI specification:** https://raw.githubusercontent.com/square/connect-api-specification/master/api.json
- **API base URL:** `https://connect.squareup.com`

## Authentication

### OAuth2

Connect Square with OAuth2 for merchant-authorized access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://connect.squareup.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://connect.squareup.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `INVENTORY_READ CUSTOMERS_WRITE CUSTOMERS_READ ITEMS_READ MERCHANT_PROFILE_READ ORDERS_READ INVOICES_READ PAYMENTS_WRITE ORDERS_WRITE INVOICES_WRITE ORDERS_WRITE ITEMS_WRITE PAYMENTS_READ PAYMENTS_WRITE DEVICE_CREDENTIAL_MANAGEMENT MERCHANT_PROFILE_WRITE DEVICES_READ BANK_ACCOUNTS_READ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://connect.squareup.com/oauth2/token.

[Official authentication documentation](https://developer.squareup.com/docs/oauth-api/overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `locations`.
