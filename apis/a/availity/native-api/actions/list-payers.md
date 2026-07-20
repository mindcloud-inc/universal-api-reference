# List Payers with Availity

Retrieves payers and supported transactions from Availity.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/availity-payer-list`
- **Base URL:** `https://api.availity.com`
- **Official documentation:** [List Payers](https://developer.availity.com/blog/2025/3/25/hipaa-transactions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payerId` | query | `string` | no | Availity-specific payer identifier to narrow the payer list. |
| `transactionType` | query | `string<string>` | no | EDI/HIPAA transaction type code, such as 270, 276, 837P, 837I, or 837D. Send multiple values as a array. |
