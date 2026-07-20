# Batch Validate Bank Accounts with Loqate

Validates multiple bank accounts with Loqate.

## Endpoint

- **Method:** `GET`
- **Path:** `/BankAccountValidation/Batch/Validate/v1.00/json6.ws`
- **Base URL:** `https://api.addressy.com`
- **Official documentation:** [Batch Validate Bank Accounts](https://docs.loqate.com/api-reference/bank-validation/batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AccountNumbers` | query | `string` | yes | Comma-separated bank account numbers to validate. |
| `SortCodes` | query | `string` | yes | Comma-separated branch sort codes for the account numbers. |
