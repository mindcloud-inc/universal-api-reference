# Delete Address with InstantCard

Deletes an existing address from InstantCard.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/organizations/:organizationId/addresses/:id`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [Delete Address](https://instantcard.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Address ID from InstantCard. |
| `organizationId` | path | `number` | yes | Organization ID from InstantCard. |
