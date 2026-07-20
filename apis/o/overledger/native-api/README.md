# Overledger: Native API Reference

A consolidated summary of Overledger's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docs.overledger.dev/
- **API base URL:** `https://api.overledger.dev`

## Authentication

### OAuth2 Client Credentials

Authenticate with Overledger using OAuth2 machine-to-machine client credentials.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://auth.overledger.dev/oauth2/token to approve access.
2. Exchange the returned authorization code with a POST request to https://auth.overledger.dev/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.overledger.dev/docs/api-keys)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Smart Contract Webhook](actions/create-smart-contract-webhook.md) | `POST /api/webhooks/smart-contract-events` | [docs](https://docs.overledger.dev/docs/smart-contract) |
| [Get Address Sequence](actions/get-address-sequence.md) | `POST /v2/autoexecution/search/address/sequence/:addressId` | [docs](https://docs.overledger.dev/docs/address-sequence) |
| [Get UTXO State](actions/get-utxo-state.md) | `POST /v2/autoexecution/search/utxo/:utxoId` | [docs](https://docs.overledger.dev/docs/utxo) |
| [List Supported Fungible Tokens](actions/list-supported-fungible-tokens.md) | `GET /v2/tokens/fungible` | [docs](https://docs.overledger.dev/docs/supported-tokens-1) |
| [Read Smart Contract Function](actions/read-smart-contract-function.md) | `POST /api/smart-contracts/read` | [docs](https://docs.overledger.dev/docs/read) |
| [Update Account Webhook Callback URL](actions/update-account-webhook-callback-url.md) | `PATCH /api/webhooks/accounts/:webhookId` | [docs](https://docs.overledger.dev/docs/update-the-callback-url-for-an-account-webhook) |
