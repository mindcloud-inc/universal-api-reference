# Retrieve Bank Branch By Sort Code with Loqate

Retrieves a bank branch from Loqate by sort code.

## Endpoint

- **Method:** `GET`
- **Path:** `/BankAccountValidation/Interactive/RetrieveBySortcode/v1.00/json6.ws`
- **Base URL:** `https://api.addressy.com`
- **Official documentation:** [Retrieve Bank Branch By Sort Code](https://docs.loqate.com/api-reference/bank-validation/retrievebysortcode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SortCode` | query | `string` | yes | The branch sort code. |
