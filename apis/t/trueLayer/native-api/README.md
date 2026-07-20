# TrueLayer: Native API Reference

A consolidated summary of TrueLayer's API configuration and 63 documented operations, with links to official documentation.

- **Official docs:** https://docs.truelayer.com
- **OpenAPI specification:** https://docs.truelayer.com/reference/welcome-api-reference
- **API base URL:** `https://api.truelayer-sandbox.com`

## Authentication

### TrueLayer OAuth2

OAuth2 authentication for TrueLayer sandbox APIs. Payments uses client credentials with the payments scope; Data API and Verification use user-authorized access tokens for data/verification scopes.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://auth.truelayer.com/ to approve access.
2. Exchange the returned authorization code with a POST request to https://auth.truelayer-sandbox.com/connect/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `payments`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.truelayer.com/docs/generate-a-payments-access-token)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json; charset=UTF-8` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–50). Use `cursor` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (63 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bank Lookup](actions/bank-lookup.md) | `POST /v3/bank-lookup` | [docs](https://docs.truelayer.com/reference/get-account-holder-verification) |
| [Cancel Payment](actions/cancel-payment.md) | `POST /v3/payments/:id/actions/cancel` | [docs](https://docs.truelayer.com/reference/cancel-payment) |
| [Confirm Mandate Funds](actions/confirm-mandate-funds.md) | `GET /v3/mandates/:id/funds` | [docs](https://docs.truelayer.com/reference/confirm-mandate-funds) |
| [Create Account Holder Verification](actions/create-account-holder-verification.md) | `POST /v3/account-holder-verifications/requests` | [docs](https://docs.truelayer.com/reference/get-account-holder-verification) |
| [Create Mandate](actions/create-mandate.md) | `POST /v3/mandates` | [docs](https://docs.truelayer.com/reference/create-mandate) |
| [Create Payment](actions/create-payment.md) | `POST /v3/payments` | [docs](https://docs.truelayer.com/reference/create-payment) |
| [Create Payment Link](actions/create-payment-link.md) | `POST /v3/payment-links` | [docs](https://docs.truelayer.com/reference/create-payment-link) |
| [Create Payment Refund](actions/create-payment-refund.md) | `POST /v3/payments/:id/refunds` | [docs](https://docs.truelayer.com/reference/create-payment-refund) |
| [Create Payout](actions/create-payout.md) | `POST /v3/payouts` | [docs](https://docs.truelayer.com/reference/create-payout) |
| [Disable Merchant Account Sweeping](actions/disable-merchant-account-sweeping.md) | `DELETE /v3/merchant-accounts/:id/sweeping` | [docs](https://docs.truelayer.com/reference/merchant-account-disable-sweeping) |
| [Get Account Holder Verification](actions/get-account-holder-verification.md) | `GET /v3/account-holder-verifications/requests/:id` | [docs](https://docs.truelayer.com/reference/get-account-holder-verification) |
| [Get Data Account](actions/get-data-account.md) | `GET /data/v1/accounts/:account_id` | [docs](https://docs.truelayer.com/docs/account-and-card-data) |
| [Get Data Account Balance](actions/get-data-account-balance.md) | `GET /data/v1/accounts/:account_id/balance` | [docs](https://docs.truelayer.com/docs/account-and-card-data) |
| [Get Data Account Direct Debits](actions/get-data-account-direct-debits.md) | `GET /data/v1/accounts/:account_id/direct_debits` | [docs](https://docs.truelayer.com/docs/data-api-basics) |
| [Get Data Account Standing Orders](actions/get-data-account-standing-orders.md) | `GET /data/v1/accounts/:account_id/standing_orders` | [docs](https://docs.truelayer.com/docs/data-api-basics) |
| [Get Data Account Transactions](actions/get-data-account-transactions.md) | `GET /data/v1/accounts/:account_id/transactions` | [docs](https://docs.truelayer.com/docs/account-and-card-data) |
| [Get Data Card](actions/get-data-card.md) | `GET /data/v1/cards/:card_id` | [docs](https://docs.truelayer.com/docs/account-and-card-data) |
| [Get Data Card Balance](actions/get-data-card-balance.md) | `GET /data/v1/cards/:card_id/balance` | [docs](https://docs.truelayer.com/docs/account-and-card-data) |
| [Get Data Card Transactions](actions/get-data-card-transactions.md) | `GET /data/v1/cards/:card_id/transactions` | [docs](https://docs.truelayer.com/docs/account-and-card-data) |
| [Get Data Info](actions/get-data-info.md) | `GET /data/v1/info` | [docs](https://docs.truelayer.com/docs/data-api-basics) |
| [Get Data Providers](actions/get-data-providers.md) | `GET /api/providers` | [docs](https://docs.truelayer.com/docs/data-api-basics) |
| [Get Mandate](actions/get-mandate.md) | `GET /v3/mandates/:id` | [docs](https://docs.truelayer.com/reference/get-mandate) |
| [Get Mandate Constraints](actions/get-mandate-constraints.md) | `GET /v3/mandates/:id/constraints` | [docs](https://docs.truelayer.com/reference/get-constraints) |
| [Get Merchant Account](actions/get-merchant-account.md) | `GET /v3/merchant-accounts/:id` | [docs](https://docs.truelayer.com/reference/get-operating-account) |
| [Get Merchant Account Payment Sources](actions/get-merchant-account-payment-sources.md) | `GET /v3/merchant-accounts/:id/payment-sources` | [docs](https://docs.truelayer.com/reference/get-merchant-account-payment-sources) |
| [Get Merchant Account Sweeping](actions/get-merchant-account-sweeping.md) | `GET /v3/merchant-accounts/:id/sweeping` | [docs](https://docs.truelayer.com/reference/merchant-account-get-sweeping) |
| [Get Merchant Account Transactions](actions/get-merchant-account-transactions.md) | `GET /v3/merchant-accounts/:id/transactions` | [docs](https://docs.truelayer.com/docs/get-your-merchant-account-transactions-or-payment-sources) |
| [Get Payment](actions/get-payment.md) | `GET /v3/payments/:id` | [docs](https://docs.truelayer.com/reference/get-payment-1) |
| [Get Payment Link](actions/get-payment-link.md) | `GET /v3/payment-links/:id` | [docs](https://docs.truelayer.com/reference/get-payment-link) |
| [Get Payment Link Payments](actions/get-payment-link-payments.md) | `GET /v3/payment-links/:id/payments` | [docs](https://docs.truelayer.com/reference/get-payment-link-payments) |
| [Get Payment Provider](actions/get-payment-provider.md) | `GET /v3/payments-providers/:id` | [docs](https://docs.truelayer.com/reference/get-payment-provider) |
| [Get Payment Refund](actions/get-payment-refund.md) | `GET /v3/payments/:payment_id/refunds/:refund_id` | [docs](https://docs.truelayer.com/reference/get-payment-refund) |
| [Get Payment Refunds](actions/get-payment-refunds.md) | `GET /v3/payments/:id/refunds` | [docs](https://docs.truelayer.com/reference/get-payment-refunds) |
| [Get Payout](actions/get-payout.md) | `GET /v3/payouts/:id` | [docs](https://docs.truelayer.com/reference/get-payout) |
| [Get Payout Authorization Flow](actions/get-payout-authorization-flow.md) | `GET /v3/payouts/:id/authorization-flow` | [docs](https://docs.truelayer.com/reference/get-payout-authorization-flow) |
| [Get Signup Plus Accounts](actions/get-signup-plus-accounts.md) | `GET /signup-plus/accounts` | [docs](https://docs.truelayer.com/docs/data-only-integration) |
| [Get Signup Plus Mandate Data](actions/get-signup-plus-mandate-data.md) | `GET /signup-plus/mandates` | [docs](https://docs.truelayer.com/docs/variable-recurring-payments-integration) |
| [Legacy Get Payment](actions/legacy-get-payment.md) | `GET /v2/single-immediate-payment-initiation-requests/:id` | [docs](https://docs.truelayer.com/reference/get-providers) |
| [Legacy Initiate Payment](actions/legacy-initiate-payment.md) | `POST /v2/single-immediate-payment-initiation-requests` | [docs](https://docs.truelayer.com/reference/get-providers) |
| [Legacy List Payment Providers](actions/legacy-list-payment-providers.md) | `GET /v2/single-immediate-payments-providers` | [docs](https://docs.truelayer.com/reference/get-providers) |
| [Legacy Submit Embedded Payment Step](actions/legacy-submit-embedded-payment-step.md) | `POST /v2/single-immediate-payment-initiation-requests/:id/authorization-flow/actions` | [docs](https://docs.truelayer.com/reference/get-providers) |
| [List Data Accounts](actions/list-data-accounts.md) | `GET /data/v1/accounts` | [docs](https://docs.truelayer.com/docs/account-and-card-data) |
| [List Data Cards](actions/list-data-cards.md) | `GET /data/v1/cards` | [docs](https://docs.truelayer.com/docs/account-and-card-data) |
| [List Mandates](actions/list-mandates.md) | `GET /v3/mandates` | [docs](https://docs.truelayer.com/reference/list-mandate) |
| [List Merchant Accounts](actions/list-merchant-accounts.md) | `GET /v3/merchant-accounts` | [docs](https://docs.truelayer.com/reference/list-operating-accounts) |
| [Revoke Mandate](actions/revoke-mandate.md) | `POST /v3/mandates/:id/revoke` | [docs](https://docs.truelayer.com/reference/revoke-mandate) |
| [Save Payment User Account](actions/save-payment-user-account.md) | `POST /v3/payments/:id/actions/save-user-account` | [docs](https://docs.truelayer.com/reference/save-user-account-payment) |
| [Search Payment Providers](actions/search-payment-providers.md) | `POST /v3/payments-providers/search` | [docs](https://docs.truelayer.com/reference/search-payment-providers) |
| [Set Merchant Account Sweeping](actions/set-merchant-account-sweeping.md) | `POST /v3/merchant-accounts/:id/sweeping` | [docs](https://docs.truelayer.com/reference/merchant-account-setup-sweeping) |
| [Start Mandate Authorization Flow](actions/start-mandate-authorization-flow.md) | `POST /v3/mandates/:id/authorization-flow` | [docs](https://docs.truelayer.com/reference/start-mandate-authorization-flow) |
| [Start Payment Authorization Flow](actions/start-payment-authorization-flow.md) | `POST /v3/payments/:id/authorization-flow` | [docs](https://docs.truelayer.com/reference/start-payment-authorization-flow) |
| [Start Payout Authorization Flow](actions/start-payout-authorization-flow.md) | `POST /v3/payouts/:id/authorization-flow` | [docs](https://docs.truelayer.com/reference/start-payout-authorization-flow) |
| [Submit Mandate Consent](actions/submit-mandate-consent.md) | `POST /v3/mandates/:id/authorization-flow/actions/consent` | [docs](https://docs.truelayer.com/reference/submit-consent-mandate) |
| [Submit Mandate Provider Selection](actions/submit-mandate-provider-selection.md) | `POST /v3/mandates/:id/authorization-flow/actions/provider-selection` | [docs](https://docs.truelayer.com/reference/submit-mandate-provider-selection) |
| [Submit Payment Branch Selection](actions/submit-payment-branch-selection.md) | `POST /v3/payments/:id/authorization-flow/actions/branch-selection` | [docs](https://docs.truelayer.com/reference/submit-branch-selection) |
| [Submit Payment Consent](actions/submit-payment-consent.md) | `POST /v3/payments/:id/authorization-flow/actions/consent` | [docs](https://docs.truelayer.com/reference/submit-consent) |
| [Submit Payment Form](actions/submit-payment-form.md) | `POST /v3/payments/:id/authorization-flow/actions/form` | [docs](https://docs.truelayer.com/reference/submit-form) |
| [Submit Payment Provider Selection](actions/submit-payment-provider-selection.md) | `POST /v3/payments/:id/authorization-flow/actions/provider-selection` | [docs](https://docs.truelayer.com/reference/submit-provider-selection) |
| [Submit Payment Scheme Selection](actions/submit-payment-scheme-selection.md) | `POST /v3/payments/:id/authorization-flow/actions/scheme-selection` | [docs](https://docs.truelayer.com/reference/submit-scheme-selection) |
| [Submit Payment User Account Selection](actions/submit-payment-user-account-selection.md) | `POST /v3/payments/:id/authorization-flow/actions/user-account-selection` | [docs](https://docs.truelayer.com/reference/submit-user-account-selection) |
| [Submit Payments Provider Return Parameters](actions/submit-payments-provider-return-parameters.md) | `POST /v3/payments-provider-return` | [docs](https://docs.truelayer.com/reference/submit-payments-provider-return-parameters) |
| [Verify Account Holder Name](actions/verify-account-holder-name.md) | `POST /verification/v1/verify` | [docs](https://docs.truelayer.com/reference/get-account-holder-verification) |
| [Verify France Account Details](actions/verify-france-account-details.md) | `POST /v3/verification/fr/verify-account-details` | [docs](https://docs.truelayer.com/reference/get-account-holder-verification) |
