# Create Customer Funding Source with Dwolla

Creates a funding source for a Dwolla customer.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/[:id]/funding-sources`
- **Base URL:** `https://api-sandbox.dwolla.com`
- **Official documentation:** [Create Customer Funding Source](https://developers.dwolla.com/docs/api-reference/funding-sources/create-customer-funding-source)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Dwolla customer ID. |
| `name` | body | `string` | yes | Funding source display name |
| `routingNumber` | body | `string` | yes | Bank routing number |
| `accountNumber` | body | `string` | yes | Bank account number |
| `bankAccountType` | body | `string` | yes | Bank account type |
