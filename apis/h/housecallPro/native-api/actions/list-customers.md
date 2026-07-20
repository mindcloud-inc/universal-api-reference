# List Customers with Housecall Pro

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [List Customers](https://docs.housecallpro.com/docs/housecall-public-api/042bd3bf861ae-get-customers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search customers by name, email, mobile number, or address. |
| `location_ids[]` | query | `array<string>` | no | IDs of locations to pull customers from. Send multiple values as a array. |
| `expand[]` | query | `array<string>` | no | Fields to expand in the response body. Send multiple values as a array. |
