# Validate International Bank Account with Loqate

Validates an international bank account with Loqate.

## Endpoint

- **Method:** `GET`
- **Path:** `/InternationalBankValidation/Interactive/Validate/v1.00/json6.ws`
- **Base URL:** `https://api.addressy.com`
- **Official documentation:** [Validate International Bank Account](https://docs.loqate.com/api-reference/bank-validation/international)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `IBAN` | query | `string` | yes | The international bank account number to validate. |
