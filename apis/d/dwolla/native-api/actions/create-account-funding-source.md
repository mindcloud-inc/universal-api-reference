# Create Account Funding Source with Dwolla

Creates a funding source for a Dwolla account.

## Endpoint

- **Method:** `POST`
- **Path:** `/funding-sources`
- **Base URL:** `https://api-sandbox.dwolla.com`
- **Official documentation:** [Create Account Funding Source](https://developers.dwolla.com/docs/api-reference/accounts/create-a-funding-source-for-an-account)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Funding source display name |
| `routingNumber` | body | `string` | yes | Bank routing number |
| `accountNumber` | body | `string` | yes | Bank account number |
| `bankAccountType` | body | `string` | yes | Bank account type |
