# Delete Card with InstantCard

Deletes an existing card from InstantCard.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/organizations/:organizationId/cards/:id`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Delete Card](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `id` | path | `number` | yes | ID of the card to delete. |
