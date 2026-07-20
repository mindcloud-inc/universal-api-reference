# Validate Bank Account with Data8

Validates a bank account with Data8.

## Endpoint

- **Method:** `POST`
- **Path:** `/BankAccountValidation/IsValid.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Validate Bank Account](https://docs.data-8.co.uk/web-services/bankaccountvalidation/isvalid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sortCode` | body | `string` | yes | The sort code to validate. |
| `bankAccountNumber` | body | `string` | no | The optional account number to validate. |
| `options` | body | `object` | no | Optional settings that control bank validation behavior. |
