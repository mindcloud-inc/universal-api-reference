# Get Deposit Details with Stax

Retrieves details for a deposit in Stax.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/depositDetail`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [Get Deposit Details](https://docs.staxpayments.com/reference/get-details-of-specific-deposit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | no | Deposit detail report end date |
| `id` | query | `string` | no | Deposit identifier |
| `startDate` | query | `string` | no | Deposit detail report start date |
| `timespan` | query | `string` | no | Named deposit detail timespan |
