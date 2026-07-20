# List Card Print History with InstantCard

Retrieves print history for a card in InstantCard.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/cards/:id/print_history`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [List Card Print History](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `id` | path | `number` | yes | ID of the card whose print history to fetch. |
