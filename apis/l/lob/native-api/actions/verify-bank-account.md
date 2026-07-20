# Verify Bank Account with Lob

## Endpoint

- **Method:** `POST`
- **Path:** `/bank_accounts/:bank_id/verify`
- **Base URL:** `https://api.lob.com/v1`
- **Official documentation:** [Verify Bank Account](https://docs.lob.com/#tag/Bank-Accounts/operation/bank_account_verify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bank_id` | path | `string` | yes | Bank account ID. |
| `amounts[]` | body | `array<number>` | yes | Two micro-deposit amounts in cents. |
