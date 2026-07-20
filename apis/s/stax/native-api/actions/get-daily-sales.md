# Get Daily Sales with Stax

Retrieves daily sales totals from Stax.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/statement/v3/daily-sales`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [Get Daily Sales](https://docs.staxpayments.com/reference/daily-sales)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | no | Daily sales interval end date |
| `startDate` | query | `string` | no | Daily sales interval start date |
