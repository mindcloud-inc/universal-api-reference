# Cancel Number with Fluents

Cancels an existing phone number from Fluents.

## Endpoint

- **Method:** `POST`
- **Path:** `/numbers/cancel`
- **Base URL:** `https://api.fluents.ai/v1`
- **Official documentation:** [Cancel Number](https://docs.fluents.ai/api-reference/numbers/cancel-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Fluents phone number ID to cancel. |
