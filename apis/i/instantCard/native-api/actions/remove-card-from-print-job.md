# Remove Card From Print Job with InstantCard

Updates an existing print job in InstantCard by removing a card.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/organizations/:organizationId/print_jobs/:id/remove_cards/:cardId`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Remove Card From Print Job](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `id` | path | `number` | yes | ID of the print job to update. |
| `cardId` | path | `number` | yes | ID of the card to remove from the print job. |
