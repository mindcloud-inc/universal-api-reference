# Validate Bank Account with Loqate

Validates a bank account with Loqate.

## Endpoint

- **Method:** `GET`
- **Path:** `/BankAccountValidation/Interactive/Validate/v2.00/json6.ws`
- **Base URL:** `https://api.addressy.com`
- **Official documentation:** [Validate Bank Account](https://docs.loqate.com/api-reference/bank-validation/individual)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AccountNumber` | query | `string` | yes | The bank account number to validate. |
| `SortCode` | query | `string` | yes | The branch sort code for the account number. |
