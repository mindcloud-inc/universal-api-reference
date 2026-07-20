# List Customer Cards with OPN

Retrieves a list of cards for a customer from OPN.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/:id/cards`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [List Customer Cards](https://docs.omise.co/card-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The customer ID whose cards to list. |
