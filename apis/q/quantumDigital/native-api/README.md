# Quantum Digital: Native API Reference

A consolidated summary of Quantum Digital's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://developer.quantumdigital.com/docs
- **API base URL:** `https://api.quantumdigital.com`

## Authentication

### OAuth 2.0

OAuth2 client credentials

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.quantumdigital.com/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://developer.quantumdigital.com/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Dashboard Access](actions/check-dashboard-access.md) | `POST /devplatform/checkdashboardaccess` | [docs](https://developer.quantumdigital.com/docs) |
| [Create Payment Method](actions/create-payment-method.md) | `POST /devplatform/billing/:dashboardAccountId/paymentmethods` | [docs](https://developer.quantumdigital.com/docs) |
| [Delete Payment Method](actions/delete-payment-method.md) | `DELETE /devplatform/billing/:dashboardAccountId/paymentmethods` | [docs](https://developer.quantumdigital.com/docs) |
| [Get Account Extra Data](actions/get-account-extra-data.md) | `GET /devplatform/accounts/:dashboardAccountId` | [docs](https://developer.quantumdigital.com/docs) |
| [List Invoices](actions/list-invoices.md) | `GET /devplatform/billing/:dashboardAccountId/invoices` | [docs](https://developer.quantumdigital.com/docs) |
| [List Orders](actions/list-orders.md) | `GET /v1/orders` | [docs](https://developer.quantumdigital.com/docs) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /devplatform/billing/:dashboardAccountId/paymentmethods` | [docs](https://developer.quantumdigital.com/docs) |
| [List Provinces](actions/list-provinces.md) | `GET /utils/provinces?countryCodes=US,CA&excludeUST=1` | [docs](https://developer.quantumdigital.com/docs) |
| [List User Designs](actions/list-user-designs.md) | `GET /v1/userdesigns` | [docs](https://developer.quantumdigital.com/docs) |
| [List User Lists](actions/list-user-lists.md) | `GET /v1/userlists` | [docs](https://developer.quantumdigital.com/docs) |
| [Sign Up](actions/sign-up.md) | `POST /devplatform/signup` | [docs](https://developer.quantumdigital.com/docs) |
| [Update API Account Mode](actions/update-api-account-mode.md) | `PUT /devplatform/apiaccountmode` | [docs](https://developer.quantumdigital.com/docs) |
| [Update Login Email](actions/update-login-email.md) | `PUT /devplatform/accounts/:dashboardAccountId/email` | [docs](https://developer.quantumdigital.com/docs) |
| [Update Password](actions/update-password.md) | `PUT /devplatform/accounts/:dashboardAccountId/password` | [docs](https://developer.quantumdigital.com/docs) |
| [Update Payment Method](actions/update-payment-method.md) | `PUT /devplatform/billing/:dashboardAccountId/paymentmethods` | [docs](https://developer.quantumdigital.com/docs) |
