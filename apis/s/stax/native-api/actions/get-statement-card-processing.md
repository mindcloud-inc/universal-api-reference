# Get Statement Card Processing with Stax

Retrieves statement card processing totals from Stax.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/statement/v3/volumes/card-processing`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [Get Statement Card Processing](https://docs.staxpayments.com/reference/card-processing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | no | Report interval end date |
| `startDate` | query | `string` | no | Report interval start date |
