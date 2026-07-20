# Get Statement ACH Rejections with Stax

Retrieves statement ACH rejections from Stax.

## Endpoint

- **Method:** `GET`
- **Path:** `/query/statement/v3/ach-rejects`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [Get Statement ACH Rejections](https://docs.staxpayments.com/reference/ach-rejections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | no | Report interval end date |
| `startDate` | query | `string` | no | Report interval start date |
