# List Payment Links with Bridge

Retrieves payment links from Bridge.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment/payment-links`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [List Payment Links](https://docs.bridgeapi.io/reference/listpaymentlinks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Cursor pointing to the start of the desired set |
| `since` | query | `date` | no | Limit to payment links created after the specified date. Format example: 2024-09-21T22:00:00.000Z |
| `until` | query | `date` | no | Limit to payment links created before the specified date. Format example: 2024-09-21T22:00:00.000Z |
| `status` | query | `string` | no | You can filter payment links by status |
