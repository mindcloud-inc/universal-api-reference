# Create Customer Bank Account with GoCardless

Creates a new customer bank account in GoCardless.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer_bank_accounts`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [Create Customer Bank Account](https://developer.gocardless.com/api-reference/#customer-bank-accounts-create-a-customer-bank-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_holder_name` | body | `string` | no | — |
| `account_number` | body | `string` | no | — |
| `account_type` | body | `string` | no | — |
| `bank_code` | body | `string` | no | — |
| `branch_code` | body | `string` | no | — |
| `country_code` | body | `string` | no | — |
| `currency` | body | `list` | no | Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `iban` | body | `string` | no | — |
| `metadata` | body | `object` | no | — |
| `links` | body | `object` | no | — |
| `links.customer` | body | `string` | yes | — |
| `links.customer_bank_account_token` | body | `string` | no | — |
