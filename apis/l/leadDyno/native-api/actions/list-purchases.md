# List Purchases with LeadDyno

Retrieves purchases from your LeadDyno account.

## Endpoint

- **Method:** `GET`
- **Path:** `/purchases`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [List Purchases](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/get-purchases)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_line_items` | query | `boolean` | no | Include detailed line items in the response. |
