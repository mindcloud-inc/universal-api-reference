# Privy: Native API Reference

A consolidated summary of Privy's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.privy.io/api-reference/introduction
- **OpenAPI specification:** https://api.privy.io/v1/openapi.json
- **API base URL:** `https://api.privy.io`

## Authentication

### Basic Auth

Authenticate to the Privy REST API with the Privy app ID as the Basic Auth username and the app secret as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.privy.io/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `cursor` in the query string as the pagination cursor; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate Wallet](actions/authenticate-wallet.md) | `POST /v1/wallets/authenticate` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets~1authenticate/post) |
| [Create Condition Set](actions/create-condition-set.md) | `POST /v1/condition_sets` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1condition_sets/post) |
| [Create Condition Set Items](actions/create-condition-set-items.md) | `POST /v1/condition_sets/{{conditionSetId}}/condition_set_items` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1condition_sets~1{condition_set_id}~1condition_set_items/post) |
| [Create Key Quorum](actions/create-key-quorum.md) | `POST /v1/key_quorums` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1key_quorums/post) |
| [Create Policy](actions/create-policy.md) | `POST /v1/policies` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies/post) |
| [Create Policy Rule](actions/create-policy-rule.md) | `POST /v1/policies/{{policyId}}/rules` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies~1{policy_id}~1rules/post) |
| [Create User](actions/create-user.md) | `POST /v1/users` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users/post) |
| [Create User Embedded Wallet](actions/create-user-embedded-wallet.md) | `POST /v1/users/{{userId}}/wallets` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users~1{user_id}~1wallets/post) |
| [Create Wallet](actions/create-wallet.md) | `POST /v1/wallets` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets/post) |
| [Create Wallets In Batch](actions/create-wallets-in-batch.md) | `POST /v1/wallets/batch` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets~1batch/post) |
| [Delete Policy](actions/delete-policy.md) | `DELETE /v1/policies/{{policyId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies~1{policy_id}/delete) |
| [Delete Policy Rule](actions/delete-policy-rule.md) | `DELETE /v1/policies/{{policyId}}/rules/{{ruleId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies~1{policy_id}~1rules~1{rule_id}/delete) |
| [Get Condition Set](actions/get-condition-set.md) | `GET /v1/condition_sets/{{conditionSetId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1condition_sets~1{condition_set_id}/get) |
| [Get Intent](actions/get-intent.md) | `GET /v1/intents/{{intentId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1intents~1{intent_id}/get) |
| [Get Key Quorum](actions/get-key-quorum.md) | `GET /v1/key_quorums/{{keyQuorumId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1key_quorums~1{key_quorum_id}/get) |
| [Get Policy](actions/get-policy.md) | `GET /v1/policies/{{policyId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies~1{policy_id}/get) |
| [Get Policy Rule](actions/get-policy-rule.md) | `GET /v1/policies/{{policyId}}/rules/{{ruleId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies~1{policy_id}~1rules~1{rule_id}/get) |
| [Get Transaction](actions/get-transaction.md) | `GET /v1/transactions/{{transactionId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1transactions~1{transaction_id}/get) |
| [Get Transaction By Reference ID](actions/get-transaction-by-reference-id.md) | `GET /v1/transactions` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1transactions/get) |
| [Get User](actions/get-user.md) | `GET /v1/users/{{userId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users~1{user_id}/get) |
| [Get User By Custom Auth ID](actions/get-user-by-custom-auth-id.md) | `POST /v1/users/custom_auth/id` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users~1custom_auth~1id/post) |
| [Get User By Email](actions/get-user-by-email.md) | `POST /v1/users/email/address` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users~1email~1address/post) |
| [Get User By Phone Number](actions/get-user-by-phone-number.md) | `POST /v1/users/phone/number` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users~1phone~1number/post) |
| [Get User By Wallet Address](actions/get-user-by-wallet-address.md) | `POST /v1/users/wallet/address` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users~1wallet~1address/post) |
| [Get Wallet](actions/get-wallet.md) | `GET /v1/wallets/{{walletId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets~1{wallet_id}/get) |
| [Get Wallet Balance](actions/get-wallet-balance.md) | `GET /v1/wallets/{{walletId}}/balance` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets~1{wallet_id}~1balance/get) |
| [Get Wallet By Address](actions/get-wallet-by-address.md) | `POST /v1/wallets/address` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets~1address/post) |
| [List Condition Set Items](actions/list-condition-set-items.md) | `GET /v1/condition_sets/{{conditionSetId}}/condition_set_items` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1condition_sets~1{condition_set_id}~1condition_set_items/get) |
| [List Intents](actions/list-intents.md) | `GET /v1/intents` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1intents/get) |
| [List Users](actions/list-users.md) | `GET /v1/users` | [docs](https://docs.privy.io/api-reference/users/get-all) |
| [List Wallet Transactions](actions/list-wallet-transactions.md) | `GET /v1/wallets/{{walletId}}/transactions` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets~1{wallet_id}~1transactions/get) |
| [List Wallets](actions/list-wallets.md) | `GET /v1/wallets` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets/get) |
| [Search Users](actions/search-users.md) | `POST /v1/users/search` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users~1search/post) |
| [Set User Custom Metadata](actions/set-user-custom-metadata.md) | `POST /v1/users/{{userId}}/custom_metadata` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users~1{user_id}~1custom_metadata/post) |
| [Unlink User Account](actions/unlink-user-account.md) | `POST /v1/users/{{userId}}/accounts/unlink` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users~1{user_id}~1accounts~1unlink/post) |
| [Update Condition Set](actions/update-condition-set.md) | `PATCH /v1/condition_sets/{{conditionSetId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1condition_sets~1{condition_set_id}/patch) |
| [Update Key Quorum](actions/update-key-quorum.md) | `PATCH /v1/key_quorums/{{keyQuorumId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1key_quorums~1{key_quorum_id}/patch) |
| [Update Policy](actions/update-policy.md) | `PATCH /v1/policies/{{policyId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies~1{policy_id}/patch) |
| [Update Policy Rule](actions/update-policy-rule.md) | `PATCH /v1/policies/{{policyId}}/rules/{{ruleId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1policies~1{policy_id}~1rules~1{rule_id}/patch) |
| [Update Wallet](actions/update-wallet.md) | `PATCH /v1/wallets/{{walletId}}` | [docs](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets~1{wallet_id}/patch) |
