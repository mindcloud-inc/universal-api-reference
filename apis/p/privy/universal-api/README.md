# <img src="https://images.mindcloud.co/apps/icons/0x0_1776713651449.png" alt="Privy logo" width="28" height="28"> Privy: Universal API

Privy provides authentication, embedded wallet, wallet management, user management, policy control, transaction, and account APIs for apps built on crypto rails.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/privy/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.privy.io/
- **Vendor API docs:** https://docs.privy.io/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Condition Set

| Action | Method | Description |
| --- | --- | --- |
| [Create Condition Set](actions/create-condition-set.md) | POST | Creates a new condition set in Privy. |
| [Get Condition Set](actions/get-condition-set.md) | GET | Retrieves a condition set from Privy. |
| [Update Condition Set](actions/update-condition-set.md) | PUT | Updates an existing condition set in Privy. |

### Condition Set Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Condition Set Items](actions/create-condition-set-items.md) | POST | Creates items in a Privy condition set. |
| [List Condition Set Items](actions/list-condition-set-items.md) | GET | Retrieves items from a Privy condition set. |

### Embedded Wallet

| Action | Method | Description |
| --- | --- | --- |
| [Create User Embedded Wallet](actions/create-user-embedded-wallet.md) | POST | Creates an embedded wallet for a Privy user. |

### Intent

| Action | Method | Description |
| --- | --- | --- |
| [Get Intent](actions/get-intent.md) | GET | Retrieves an intent from Privy by ID. |
| [List Intents](actions/list-intents.md) | GET | Retrieves a list of intents from Privy. |

### Key Quorum

| Action | Method | Description |
| --- | --- | --- |
| [Create Key Quorum](actions/create-key-quorum.md) | POST | Creates a new key quorum in Privy. |
| [Get Key Quorum](actions/get-key-quorum.md) | GET | Retrieves a key quorum from Privy. |
| [Update Key Quorum](actions/update-key-quorum.md) | PUT | Updates an existing key quorum in Privy. |

### Linked Account

| Action | Method | Description |
| --- | --- | --- |
| [Unlink User Account](actions/unlink-user-account.md) | DELETE | Unlinks a linked account from a Privy user. |

### Policy

| Action | Method | Description |
| --- | --- | --- |
| [Create Policy](actions/create-policy.md) | POST | Creates a new policy in Privy. |
| [Delete Policy](actions/delete-policy.md) | DELETE | Deletes an existing policy from Privy. |
| [Get Policy](actions/get-policy.md) | GET | Retrieves a policy from Privy by ID. |
| [Update Policy](actions/update-policy.md) | PUT | Updates an existing policy in Privy. |

### Policy Rule

| Action | Method | Description |
| --- | --- | --- |
| [Create Policy Rule](actions/create-policy-rule.md) | POST | Creates a new rule for a Privy policy. |
| [Delete Policy Rule](actions/delete-policy-rule.md) | DELETE | Deletes a rule from a Privy policy. |
| [Get Policy Rule](actions/get-policy-rule.md) | GET | Retrieves a rule from a Privy policy. |
| [Update Policy Rule](actions/update-policy-rule.md) | PUT | Updates a rule in a Privy policy. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Privy by ID. |
| [Get Transaction By Reference ID](actions/get-transaction-by-reference-id.md) | GET | Finds transactions in Privy by reference ID. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Privy. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Privy by ID. |
| [Get User By Custom Auth ID](actions/get-user-by-custom-auth-id.md) | GET | Finds a user in Privy by custom auth ID. |
| [Get User By Email](actions/get-user-by-email.md) | GET | Finds a user in Privy by email address. |
| [Get User By Phone Number](actions/get-user-by-phone-number.md) | GET | Finds a user in Privy by phone number. |
| [Get User By Wallet Address](actions/get-user-by-wallet-address.md) | GET | Finds a user in Privy by wallet address. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from Privy. |
| [Search Users](actions/search-users.md) | GET | Finds users in Privy by search term. |
| [Set User Custom Metadata](actions/set-user-custom-metadata.md) | PUT | Updates custom metadata for a user in Privy. |

### Wallet

| Action | Method | Description |
| --- | --- | --- |
| [Create Wallet](actions/create-wallet.md) | POST | Creates a new wallet in Privy. |
| [Create Wallets In Batch](actions/create-wallets-in-batch.md) | POST | Creates multiple new wallets in Privy. |
| [Get Wallet](actions/get-wallet.md) | GET | Retrieves a wallet from Privy by ID. |
| [Get Wallet By Address](actions/get-wallet-by-address.md) | GET | Finds a wallet in Privy by address. |
| [List Wallets](actions/list-wallets.md) | GET | Retrieves a list of wallets from Privy. |
| [Update Wallet](actions/update-wallet.md) | PUT | Updates an existing wallet in Privy. |

### Wallet Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet Balance](actions/get-wallet-balance.md) | GET | Retrieves a wallet balance from Privy. |

### Wallet Session Key

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate Wallet](actions/authenticate-wallet.md) | POST | Authenticates a wallet session in Privy. |

### Wallet Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Wallet Transactions](actions/list-wallet-transactions.md) | GET | Retrieves transactions for a wallet from Privy. |

