# Get Statement Fees with Stax

Retrieves statement fee details from Stax.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/statement/v3/fees`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [Get Statement Fees](https://docs.staxpayments.com/reference/get-statement-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | no | Statement interval end date |
| `startDate` | query | `string` | no | Statement interval start date |
