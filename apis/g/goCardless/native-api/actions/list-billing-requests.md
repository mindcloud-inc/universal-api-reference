# List Billing Requests with GoCardless

Finds billing requests in your GoCardless account.

## Endpoint

- **Method:** `GET`
- **Path:** `/billing_requests`
- **Base URL:** `https://api-sandbox.gocardless.com`
- **Official documentation:** [List Billing Requests](https://developer.gocardless.com/api-reference/#billing-requests-list-billing-requests)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | query | `string` | no | ID of the customer. If specified, this endpoint returns billing requests for that customer. |
| `status` | query | `list<string>` | no | Status of the billing request. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `created_at` | query | `date` | no | Fixed timestamp recording when this resource was created. |
