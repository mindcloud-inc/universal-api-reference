# Get Card with InstantCard

Retrieves a card from InstantCard by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/cards/:id`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Get Card](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `id` | path | `number` | yes | ID of the card to fetch. |
