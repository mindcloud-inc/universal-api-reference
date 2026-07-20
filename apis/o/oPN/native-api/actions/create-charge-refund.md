# Create Charge Refund with OPN

Creates a new refund for a charge in OPN.

## Endpoint

- **Method:** `POST`
- **Path:** `/charges/:id/refunds`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Create Charge Refund](https://docs.omise.co/refunds-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | The refund amount in the smallest currency unit. |
| `id` | path | `string` | yes | The charge ID to refund. |
| `void` | body | `boolean` | no | Whether to void the charge instead of issuing a partial refund. |
