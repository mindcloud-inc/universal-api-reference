# List Deposits with Stax

Retrieves deposits from Stax.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/deposit`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [List Deposits](https://docs.staxpayments.com/reference/get-list-of-deposits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | no | Deposit report end date |
| `startDate` | query | `string` | no | Deposit report start date |
| `timespan` | query | `string` | no | Named deposit report timespan |
