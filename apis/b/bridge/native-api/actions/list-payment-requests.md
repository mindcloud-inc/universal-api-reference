# List Payment Requests with Bridge

Retrieves payment requests from Bridge.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment/payment-requests`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [List Payment Requests](https://docs.bridgeapi.io/reference/getpaymentrequests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Cursor pointing to the start of the desired set |
| `since` | query | `date` | no | Limit to payment requests created after the specified date. Format example: 2024-09-21T22:00:00.000Z |
| `until` | query | `date` | no | Limit to payment payment requests created before the specified date. Format example: 2024-09-21T22:00:00.000Z |
| `status` | query | `string` | no | You can filter payment payment requests by status |
| `payment_link_id` | query | `string` | no | You can filter payment requests linked to a payment link by setting a payment link id here |
