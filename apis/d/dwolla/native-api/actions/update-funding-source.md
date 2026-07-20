# Update Funding Source with Dwolla

Updates a bank funding source in Dwolla.

## Endpoint

- **Method:** `POST`
- **Path:** `/funding-sources/[:id]`
- **Base URL:** `https://api-sandbox.dwolla.com`
- **Official documentation:** [Update Funding Source](https://developers.dwolla.com/docs/api-reference/funding-sources/update-or-remove-a-funding-source)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Dwolla funding source ID. |
| `name` | body | `string` | yes | Updated funding source display name |
| `routingNumber` | body | `string` | no | Updated bank routing number |
| `accountNumber` | body | `string` | no | Updated bank account number |
| `bankAccountType` | body | `string` | no | Updated bank account type |
