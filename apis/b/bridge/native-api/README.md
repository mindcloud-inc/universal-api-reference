# Bridge: Native API Reference

A consolidated summary of Bridge's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.bridgeapi.io/reference
- **API base URL:** `https://api.bridgeapi.io/v3`

## Authentication

### Bridge credentials

Use your Bridge client ID and client secret. For authenticated aggregation endpoints, mint a Bridge user access token with the Authorization token action and pass it as an action input.

### Credentials

- **Client ID:** `clientId` · required · Your Bridge application client ID.

Send these headers with each API request:

```http
Client-Id: <clientId>
Client-Secret: <clientSecret>
```

[Official authentication documentation](https://docs.bridgeapi.io/docs/user-creation-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `pagination.next_uri`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–500).

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Collect User Consent for Guidance Services](actions/collect-user-consent-for-guidance-services.md) | `POST /guidance/consents` | [docs](https://docs.bridgeapi.io/reference/createguidanceconsent) |
| [Create Authorization Token](actions/create-authorization-token.md) | `POST /aggregation/authorization/token` | [docs](https://docs.bridgeapi.io/reference/createuserauthtoken) |
| [Create Connect Session](actions/create-connect-session.md) | `POST /aggregation/connect-sessions` | [docs](https://docs.bridgeapi.io/reference/createconnectsession) |
| [Create Payment Consent](actions/create-payment-consent.md) | `POST /payment/consents` | [docs](https://docs.bridgeapi.io/reference/createpaymentconsent) |
| [Create Payment Link](actions/create-payment-link.md) | `POST /payment/payment-links` | [docs](https://docs.bridgeapi.io/reference/createpaymentlink) |
| [Create Payment Request](actions/create-payment-request.md) | `POST /payment/payment-requests` | [docs](https://docs.bridgeapi.io/reference/createpaymentrequest) |
| [Create Payout](actions/create-payout.md) | `POST /payment/payment-account/payouts` | [docs](https://docs.bridgeapi.io/reference/createpayout) |
| [Create Production Applications](actions/create-production-applications.md) | `POST /applications` | [docs](https://docs.bridgeapi.io/reference/createapplications) |
| [Create Refund](actions/create-refund.md) | `POST /payment/payment-account/refunds` | [docs](https://docs.bridgeapi.io/reference/createrefund) |
| [Create User](actions/create-user.md) | `POST /aggregation/users` | [docs](https://docs.bridgeapi.io/reference/createuser) |
| [Create User Management Session](actions/create-user-management-session.md) | `POST /aggregation/user-management-sessions` | [docs](https://docs.bridgeapi.io/reference/createusermanagementsession) |
| [Delete Item](actions/delete-item.md) | `DELETE /aggregation/items/:id` | [docs](https://docs.bridgeapi.io/reference/deleteitem) |
| [Delete User](actions/delete-user.md) | `DELETE /aggregation/users/:uuid` | [docs](https://docs.bridgeapi.io/reference/deleteuser) |
| [Get Account](actions/get-account.md) | `GET /aggregation/accounts/:id` | [docs](https://docs.bridgeapi.io/reference/getaccount) |
| [Get Accounts Information](actions/get-accounts-information.md) | `GET /aggregation/accounts-information` | [docs](https://docs.bridgeapi.io/reference/getaccountsinformation) |
| [Get Category](actions/get-category.md) | `GET /aggregation/categories/:id` | [docs](https://docs.bridgeapi.io/reference/getcategory) |
| [Get Financial Guidance Health for User](actions/get-financial-guidance-health-for-user.md) | `GET /guidance/health/:user_uuid` | [docs](https://docs.bridgeapi.io/reference/getguidancehealth) |
| [Get Insights](actions/get-insights.md) | `GET /aggregation/insights/category` | [docs](https://docs.bridgeapi.io/reference/getinsights) |
| [Get Item](actions/get-item.md) | `GET /aggregation/items/:id` | [docs](https://docs.bridgeapi.io/reference/getitem) |
| [Get Payment Link](actions/get-payment-link.md) | `GET /payment/payment-links/:id` | [docs](https://docs.bridgeapi.io/reference/getpaymentlink) |
| [Get Payment Request](actions/get-payment-request.md) | `GET /payment/payment-requests/:id` | [docs](https://docs.bridgeapi.io/reference/getpaymentrequest) |
| [Get Payout](actions/get-payout.md) | `GET /payment/payment-account/payouts/:id` | [docs](https://docs.bridgeapi.io/reference/getpayout) |
| [Get Provider](actions/get-provider.md) | `GET /providers/:id` | [docs](https://docs.bridgeapi.io/reference/getprovider) |
| [Get Refund](actions/get-refund.md) | `GET /payment/payment-account/refunds/:id` | [docs](https://docs.bridgeapi.io/reference/getrefund) |
| [Get Stock](actions/get-stock.md) | `GET /aggregation/stocks/:id` | [docs](https://docs.bridgeapi.io/reference/getstock) |
| [Get Transaction](actions/get-transaction.md) | `GET /aggregation/transactions/:id` | [docs](https://docs.bridgeapi.io/reference/gettransaction) |
| [Get User](actions/get-user.md) | `GET /aggregation/users/:uuid` | [docs](https://docs.bridgeapi.io/reference/getuser) |
| [List Accounts](actions/list-accounts.md) | `GET /aggregation/accounts` | [docs](https://docs.bridgeapi.io/reference/getaccounts) |
| [List Beneficiaries](actions/list-beneficiaries.md) | `GET /payment/payment-account/beneficiaries` | [docs](https://docs.bridgeapi.io/reference/listbeneficiaries) |
| [List Categories](actions/list-categories.md) | `GET /aggregation/categories` | [docs](https://docs.bridgeapi.io/reference/getcategories) |
| [List Items](actions/list-items.md) | `GET /aggregation/items` | [docs](https://docs.bridgeapi.io/reference/getitems) |
| [List Payment Links](actions/list-payment-links.md) | `GET /payment/payment-links` | [docs](https://docs.bridgeapi.io/reference/listpaymentlinks) |
| [List Payment Requests](actions/list-payment-requests.md) | `GET /payment/payment-requests` | [docs](https://docs.bridgeapi.io/reference/getpaymentrequests) |
| [List Payouts](actions/list-payouts.md) | `GET /payment/payment-account/payouts` | [docs](https://docs.bridgeapi.io/reference/listpayouts) |
| [List Providers](actions/list-providers.md) | `GET /providers` | [docs](https://docs.bridgeapi.io/reference/getproviders) |
| [List Refunds](actions/list-refunds.md) | `GET /payment/payment-account/refunds` | [docs](https://docs.bridgeapi.io/reference/listrefunds) |
| [List Stocks](actions/list-stocks.md) | `GET /aggregation/stocks` | [docs](https://docs.bridgeapi.io/reference/getstocks) |
| [List Transactions](actions/list-transactions.md) | `GET /aggregation/transactions` | [docs](https://docs.bridgeapi.io/reference/gettransactions) |
| [List Users](actions/list-users.md) | `GET /aggregation/users` | [docs](https://docs.bridgeapi.io/reference/listusers) |
| [Revoke payment link](actions/revoke-payment-link.md) | `POST /payment/payment-links/:id/revoke` | [docs](https://docs.bridgeapi.io/reference/revokepaymentlink) |
