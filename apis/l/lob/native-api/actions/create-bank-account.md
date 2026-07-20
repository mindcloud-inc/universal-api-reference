# Create Bank Account with Lob

## Endpoint

- **Method:** `POST`
- **Path:** `/bank_accounts`
- **Base URL:** `https://api.lob.com/v1`
- **Official documentation:** [Create Bank Account](https://docs.lob.com/#tag/Bank-Accounts/operation/bank_account_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional description for the bank account. |
| `routing_number` | body | `string` | yes | Valid US routing number. |
| `account_number` | body | `string` | yes | Bank account number. |
| `signatory` | body | `string` | yes | Signatory printed on checks. |
| `account_type` | body | `string` | yes | Type of entity that holds the account. |
