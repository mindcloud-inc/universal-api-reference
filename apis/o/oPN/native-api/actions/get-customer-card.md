# Get Customer Card with OPN

Retrieves details for a customer card from OPN.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/:id/cards/:cardId`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Get Customer Card](https://docs.omise.co/card-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | yes | The card ID to retrieve. |
| `id` | path | `string` | yes | The customer ID that owns the card. |
