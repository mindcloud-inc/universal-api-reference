# Monta: Native API Reference

A consolidated summary of Monta's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://docs.public-api.monta.com/reference/home
- **API base URL:** `https://public-api.monta.com/api/v1`

## Authentication

### OAuth2 Client Credentials

Monta uses per-connection client credentials from CPMS. Use the connection's clientId/clientSecret to request tokens from /auth/token; access tokens expire after about one hour.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://public-api.monta.com/api/v1/auth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `charge-points charge-transactions wallet-transactions control-charging`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://public-api.monta.com/api/v1/auth/refresh. A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.public-api.monta.com/reference/get-access-token-with-client-credentials)

## API conventions

Responses from this API use JSON. The total page count is read from `meta.totalPageCount`. The current page number is read from `meta.currentPage`.

## Pagination

Use `perPage` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Retry behavior

Retry responses with status codes `429`. Wait 60000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 1 after each failed attempt.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Detect Location](actions/detect-location.md) | `GET /signup/detect-location` | [docs](https://docs.public-api.monta.com/reference/detect-location) |
| [Get Charge](actions/get-charge.md) | `GET /charges/{chargeId}` | [docs](https://docs.public-api.monta.com/reference/get-charge) |
| [Get Charge KWh Consumption](actions/get-charge-kwh-consumption.md) | `GET /charges/{chargeId}/kwh-consumption` | [docs](https://docs.public-api.monta.com/reference/get-charge-kwh-consumption) |
| [Get Charge Point](actions/get-charge-point.md) | `GET /charge-points/{chargePointId}` | [docs](https://docs.public-api.monta.com/reference/get-charge-point) |
| [Get Current Application](actions/get-current-application.md) | `GET /auth/me` | [docs](https://docs.public-api.monta.com/reference/get-auth-information) |
| [Get EVSE Status](actions/get-evse-status.md) | `GET /afir/charge-points/{evseId}/status` | [docs](https://docs.public-api.monta.com/reference/get-afir-evse-status) |
| [Get Personal Wallet](actions/get-personal-wallet.md) | `GET /wallets/personal` | [docs](https://docs.public-api.monta.com/reference/get-personal-wallet) |
| [Get Wallet Transaction](actions/get-wallet-transaction.md) | `GET /wallet-transactions/{transactionId}` | [docs](https://docs.public-api.monta.com/reference/get-wallet-transaction) |
| [List AFIR Charge Points](actions/list-afir-charge-points.md) | `GET /afir/charge-points` | [docs](https://docs.public-api.monta.com/reference/get-afir-charge-points) |
| [List Charge Points](actions/list-charge-points.md) | `GET /charge-points` | [docs](https://docs.public-api.monta.com/reference/get-charge-points) |
| [List Charges](actions/list-charges.md) | `GET /charges` | [docs](https://docs.public-api.monta.com/reference/get-charges) |
| [List Wallet Transactions](actions/list-wallet-transactions.md) | `GET /wallet-transactions` | [docs](https://docs.public-api.monta.com/reference/get-wallet-transactions) |
| [Start Charge](actions/start-charge.md) | `POST /charges` | [docs](https://docs.public-api.monta.com/reference/start-charge) |
| [Stop Charge](actions/stop-charge.md) | `POST /charges/{chargeId}/stop` | [docs](https://docs.public-api.monta.com/reference/stop-charge) |
