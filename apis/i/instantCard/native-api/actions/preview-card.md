# Preview Card with InstantCard

Retrieves a card preview from InstantCard.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/cards/:id/preview`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Preview Card](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `id` | path | `number` | yes | ID of the card to preview. |
