# Airwallex: Native API Reference

A consolidated summary of Airwallex's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://www.airwallex.com/docs/developer-tools/api
- **API base URL:** `https://api-demo.airwallex.com`

## Authentication

### Custom Header Auth

Authenticate to Airwallex by exchanging API credentials for an access token via explicit request headers.

### Credentials

- **API Key:** `apiKey` · required · Airwallex API key.
- **Login As:** `loginAs` · optional · Optional Airwallex account OpenID when authenticating on behalf of a specific account.
- **Client ID:** `clientId` · required · Airwallex Client ID paired with the API key.
- **Access Token:** `accessToken` · optional · Bearer token returned by the Airwallex login endpoint.

Send these headers with each API request:

```http
x-api-key: <apiKey>
x-client-id: <clientId>
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://www.airwallex.com/docs/api/authentication/api_access/login)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size. Use `page_num` in the query string to choose the page; numbering starts at 0.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Transfer](actions/create-transfer.md) | `POST /api/v1/transfers/create` | [docs](https://www.airwallex.com/docs/payouts/transfers/create-a-transfer) |
| [Get Beneficiary by ID](actions/get-beneficiary-by-id.md) | `GET /api/v1/beneficiaries/{{beneficiaryId}}` | [docs](https://www.airwallex.com/docs/payouts/beneficiaries/retrieve-beneficiaries) |
| [Get Current Balances](actions/get-current-balances.md) | `GET /api/v1/balances/current` | [docs](https://www.airwallex.com/docs/payments-for-platforms/compliance-support/strong-customer-authentication-(sca)/sca-for-transaction-data-retrieval) |
| [Get Global Account by ID](actions/get-global-account-by-id.md) | `GET /api/v1/global_accounts/{{globalAccountId}}` | [docs](https://www.airwallex.com/docs/accounts/get-started/global-accounts) |
| [Get Transfer by ID](actions/get-transfer-by-id.md) | `GET /api/v1/transfers/{{transferId}}` | [docs](https://www.airwallex.com/docs/payouts/transfers/create-a-transfer) |
| [List Beneficiaries](actions/list-beneficiaries.md) | `GET /api/v1/beneficiaries` | [docs](https://www.airwallex.com/docs/payouts/beneficiaries/retrieve-beneficiaries) |
| [List Global Accounts](actions/list-global-accounts.md) | `GET /api/v1/global_accounts` | [docs](https://www.airwallex.com/docs/accounts/get-started/global-accounts) |
| [List Supported Beneficiary Banks](actions/list-supported-beneficiary-banks.md) | `GET /api/v1/beneficiary_form_schemas/supported_financial_institutions` | [docs](https://www.airwallex.com/docs/payouts/beneficiaries/retrieve-supported-beneficiary-banks) |
| [List Transfers](actions/list-transfers.md) | `GET /api/v1/transfers` | [docs](https://www.airwallex.com/docs/payouts/transfers/create-a-transfer) |
| [Obtain Access Token](actions/obtain-access-token.md) | `POST /api/v1/authentication/login` | [docs](https://www.airwallex.com/docs/developer-tools/api/manage-api-keys) |
| [Validate Transfer](actions/validate-transfer.md) | `POST /api/v1/transfers/validate` | [docs](https://www.airwallex.com/docs/payouts/transfers/validate-a-transfer) |
