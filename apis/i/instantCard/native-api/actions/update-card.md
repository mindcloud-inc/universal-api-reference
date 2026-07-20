# Update Card with InstantCard

Updates an existing card in InstantCard.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/organizations/:organizationId/cards/:id`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Update Card](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `id` | path | `number` | yes | ID of the card to update. |
| `card.data[]` | body | `array<object>` | yes | Array of updated card field objects, including text and image values. |
