# Update Customer Card with OPN

Updates an existing customer card in OPN.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customers/:id/cards/:cardId`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Update Customer Card](https://docs.omise.co/card-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | yes | The card ID to update. |
| `id` | path | `string` | yes | The customer ID that owns the card. |
